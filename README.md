This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.


ER-daigram

| **User**             | **Contact**                    | **PasswordResetToken**       |
|----------------------|--------------------------------|------------------------------|
| user_id (PK)         | contact_id (PK)               | token_id (PK)                |
| name                 | user_id (FK)                  | user_id (FK)                 |
| email (UNIQUE)       | name                          | token                        |
| password_hash        | email (UNIQUE)                | expires_at                   |
| is_verified          | phone_number                  |                              |
| created_at           | address                       |                              |
| updated_at           | timezone                      |                              |
|                      | created_at                    |                              |
|                      | updated_at                    |                              |
|                      | is_deleted                    |                              |


1.User Authentication

JWT-based registration and login
Email verification upon registration
Password reset functionality using a one-time code


2.Contact Management

Add, update, and delete (soft delete) contacts
Retrieve contacts with filtering (by name, email, timezone) and sorting options
Batch processing for adding/updating multiple contacts in a single request


3.Data Validation

Validation of inputs using libraries (e.g., Joi, yup)
Unique constraints on emails for users and contacts


4.Date-Time and Timezone Management

UTC storage for creation and update timestamps
Convert timestamps to the user's specified timezone on retrieval
Filter contacts based on date range


5.File Handling

CSV/Excel file uploads for bulk creation and updating of contacts
Download endpoint for exporting contacts in CSV/Excel format


6.Security

Rate limiting on sensitive endpoints
Secure password hashing and storage


Installation
To set up the project locally:

1.Clone the repository:

git clone (https://github.com/SunnySaiPavan/contact-management.git)
cd contact-management


2.Install dependencies:
npm install

3.Configure environment variables (see Environment Variables).

4.Run the backend server:
npm run dev

Environment Variables
Create a .env file in the root directory with the following variables:
```
supabaseUrl = "";
supabaseAnonKey = ""

```


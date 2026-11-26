# PFMS — Personal Financial Management System

A personal and family financial management application designed to manage household finances, track transactions and provide secure cloud synchronization.

## 🚀 Overview

PFMS (Personal Financial Management System) is a personal project developed to simplify family financial tracking and management. The application integrates browser-based storage with optional cloud authentication and synchronization using Supabase.

The project combines a static web application hosted through GitHub Pages with Supabase for cloud storage, authentication and database security.

## ✨ Features

- Personal and household financial management
- Transaction management
- Household onboarding
- User authentication with Supabase Auth
- Optional cloud storage and synchronization
- Local browser storage with `localStorage`
- Version-checked synchronization
- Household membership and role-based access
- Admin and entry-level access roles
- JSON backup and import support

## 🔐 Access & Security

- **Admin:** Manage household data and application settings.
- **Entry:** Append transactions with server-side restrictions.
- PostgreSQL Row Level Security (RLS)
- Database policies and secure RPC functions
- Supabase authentication
- Client-side configuration uses the public anon/publishable key
- Sensitive service-role keys are not exposed in browser code

## 🛠️ Technologies Used

- HTML
- JavaScript
- Supabase
- PostgreSQL
- Supabase Auth
- Row Level Security (RLS)
- GitHub Pages
- Browser localStorage

## 🏗️ Architecture

- **Frontend:** Static web application
- **Hosting:** GitHub Pages
- **Local storage:** Browser localStorage
- **Authentication:** Supabase Auth
- **Cloud database:** Supabase / PostgreSQL
- **Security:** RLS policies and database-level authorization

## 📂 Project Structure

| File / Folder | Description |
|---|---|
| `index.html` | Main PFMS application |
| `supabase-config.js` | Supabase client configuration template |
| `supabase/schema.sql` | Database schema, RLS policies and secure RPC functions |
| `supabase/README.md` | Supabase configuration and onboarding instructions |

## ☁️ Cloud Setup

Cloud functionality requires a Supabase project.

1. Create a Supabase project.
2. Configure the Project URL and public anon/publishable key.
3. Execute the database schema.
4. Configure authentication and household onboarding.
5. Configure the application and deploy through GitHub Pages.

Refer to the project's `supabase/README.md` for setup instructions.

## 📌 Project

This is a personal application development project focused on family financial management, cloud integration, authentication, database security and synchronization.

Repository: [ADAA-Family-Finance](https://github.com/abhijith4m/ADAA-Family-Finance)

---

*Developed as a personal project exploring web application development, cloud integration and secure data management.*

# PFMS Security Design

## Overview

PFMS uses Supabase authentication and PostgreSQL security features to protect centralized family financial data.

Security controls are designed to restrict data access, manage user permissions and support secure data handling.

## Security Controls

### 1. Authentication

- Authentication is managed through Supabase.
- Access to central application data is intended to require authenticated sessions.
- Session and access management are handled through the authentication integration.

### 2. Row Level Security (RLS)

- PostgreSQL Row Level Security is used to enforce data access restrictions.
- Policies are intended to restrict records to authorized household members.
- Access restrictions are enforced at the database level rather than relying only on the frontend.

### 3. User Permissions

The application design separates administrative and entry-level permissions.

- **Admin:** Management of permitted household settings and financial records.
- **Entry user:** Restricted transaction-entry permissions.

Actual permissions are enforced through database policies and backend controls, not merely through frontend visibility.

### 4. Credential Management

- Supabase public client credentials may be used by the frontend where appropriate.
- Privileged service-role credentials must never be exposed in browser code or public repositories.
- Sensitive credentials should be maintained outside source control.

### 5. Backup and Recovery

- JSON backup and restore functionality.
- Exportable financial records.
- Independent backups for recovery.
- Users are encouraged to retain backups in multiple locations.

### 6. Browser Security

- Application inactivity locking is available as a browser-side feature.
- Browser-side controls supplement, but do not replace, backend access restrictions.

## Security Recommendations

- Verify RLS policies for every sensitive table.
- Never expose service-role keys in frontend code.
- Restrict database privileges.
- Validate permissions through direct database/API testing.
- Keep Supabase and application configuration updated.
- Maintain regular backups.
- Avoid storing real financial or personal data in public demonstrations.

## Security Responsibility

Frontend controls are not a security boundary. Authentication, database policies, grants and server-side validation must independently enforce the intended permissions.


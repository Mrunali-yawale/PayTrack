Task: Implement Spring Security Login and Organisation-Based Data Isolation
Objective: Enable secure login for seeded users and ensure each user can access only their own organisation's data.

Implementation:

1. Add Spring Security, Spring Data JPA, MySQL and Flyway dependencies in pom.xml.

2. Create database entities:
- Organisation
- UserAuth
- Invoice
3. Configure Spring Security using SecurityFilterChain, UserDetailsService and BCryptPasswordEncoder.

4. Create a login API:
- POST /api/v1/auth/login
- Authenticate users using email and password.
- Return successful login response.
5. Create Flyway migration scripts:
- V1__create_tables.sql
- V2__seed_organisations_and_users.sql
- Seed one organisation and one user with a BCrypt-hashed password.
6. Implement organisation-based data filtering:
- Get organisation_id from the authenticated user.
- Apply organisation filtering in repository queries.
- Prevent access to other organisations' records.
7. Test using curl or Bruno:
- Verify successful login.
- Verify incorrect password rejection.
- Verify organisation A cannot access organisation B's data.
- Verify passwords are stored as BCrypt hashes.
Expected Result:
- Seeded user can log in successfully.
- Users can access only their organisation's data.
- Passwords are securely stored as hashes.
- Login and data isolation work on the staging URL.

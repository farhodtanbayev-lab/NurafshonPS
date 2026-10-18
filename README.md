# Nurafshon Ps

School management site (students, teachers, admin).

## Run on your computer
```bash
npm install
npm run dev          # open http://localhost:5173
```
On the very first start the terminal prints the admin ID and a one-time password.
To choose your own: `ADMIN_ID=MYID ADMIN_PASSWORD=MyPassw0rd npm run dev` (PowerShell: `$env:ADMIN_PASSWORD="MyPassw0rd"; npm run dev`).

## Put it online (Render)
See the steps in the chat; `render.yaml` already describes the service and the data disk.
Env vars: `ADMIN_ID`, `ADMIN_PASSWORD` (always resets that admin's password), `DATA_DIR` (where db.json and uploads live),
`ALLOW_STUDENT_SELF_REGISTER=true` (optional: let unknown students create themselves).

Data: `DATA_DIR/db.json` and `DATA_DIR/uploads/`. Back them up.

## Admin sign-in
By default admins sign in with the Admin ID only. To also require a password set `REQUIRE_ADMIN_PASSWORD=true`
(recommended for a site on the internet) together with `ADMIN_PASSWORD`.

## Desktop app (Windows installer)
See `desktop/README.md`.

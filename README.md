# WASH Facility Monitoring System

A full-stack MERN (MongoDB, Express, React, Node.js) application for monitoring, reporting, and managing WASH (Water, Sanitation, and Hygiene) facilities.

## Features

- **Role-Based Access Control:** Admin, Manager, and Staff roles
- **Facility Management:** Add, edit, delete, and view facilities
- **Report Management:** Submit, view, and update reports with file uploads
- **Audit Logs:** Track all critical actions for security and compliance
- **Email Notifications:** Receive alerts on new reports
- **Responsive UI:** Modern, mobile-friendly design with Tailwind CSS
- **Authentication:** JWT-based login and registration

## Project Structure

```
MERN Final Project/
  client/      # React frontend
  server/      # Node.js/Express backend
```

### Client (React)

- `src/`
  - `App.jsx` - Main app component
  - `main.jsx` - Routing setup
  - `Login.jsx`, `Register.jsx` - Auth pages
  - `AdminDashboard.jsx`, `ManagerDashboard.jsx`, `StaffDashboard.jsx` - Dashboards
  - `ManageFacilities.jsx`, `ManagerFacilities.jsx` - Facility management
  - `ViewReports.jsx`, `ManagerReports.jsx`, `MyReports.jsx`, `SubmitReport.jsx` - Report management
  - `AuditLogs.jsx` - Audit log viewer (admin)
  - `api.js` - Axios instance

### Server (Node.js/Express)

- `models/` - Mongoose schemas (User, Facility, Report, AuditLog)
- `routes/` - API endpoints (auth, users, facilities, reports, audit logs)
- `controllers/` - Business logic for each resource
- `middleware/` - Auth and role checks
- `utils/` - Email sending, etc.

## Setup Instructions

### Prerequisites

- Node.js (v16+ recommended)
- pnpm (or npm/yarn)
- MongoDB Atlas account (or local MongoDB)

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd "MERN Final Project"
```

### 2. Install Dependencies

#### Client

```bash
cd client
pnpm install
```

#### Server

```bash
cd ../server
pnpm install
```

### 3. Environment Variables

Create a `.env` file in the `server/` directory with:

```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
ADMIN_EMAIL=admin_notification_email@example.com
```

### 4. Start the Development Servers

#### Server (from `server/`):

```bash
pnpm start
```

#### Client (from `client/`):

```bash
pnpm run dev
```

- Client: http://localhost:5173
- Server: http://localhost:5000

## Usage

- Register as a user or login as admin/manager/staff
- Admins can manage users, facilities, and view audit logs
- Managers can manage facilities and reports
- Staff can submit and view their own reports
- All actions are logged in the audit log (admin view)

## Screenshots

_Add screenshots of dashboards, forms, and audit logs here._

## License

MIT

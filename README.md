# Ticket Management System (TMS) Frontend

## 📌 Overview

This is the **React frontend** for the Smart Ticket Assignment System. It includes user authentication (login/signup), ticket creation and listing, detailed ticket views, and an **admin panel** for managing users and their roles/skills.

The app uses:

- ⚡️ [Vite](https://vitejs.dev/) for fast build and development
- 🎨 [DaisyUI](https://daisyui.com/) (based on Tailwind CSS) for UI components
- 📡 `fetch` for API calls
- 🛠️ Simple client-side auth via `localStorage`

---

## 🧾 Pages Overview

| Route          | Description                                                   |
| -------------- | ------------------------------------------------------------- |
| `/`            | Shows all tickets or Redirects to `/login` if unauthenticated |
| `/login`       | User login page                                               |
| `/signup`      | User signup page                                              |
| `/tickets/:id` | Shows detailed view of a ticket (fields vary by role)         |
| `/admin`       | Admin panel to manage users, roles, and skill assignments     |

---

## 🔧 Setup Instructions

1. **Clone the repo**:

   ```bash
   git clone https://github.com/wajeshubham/ai-ticket-assistant-fe.git
   cd ai-ticket-assistant-fe
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Create `.env`** file:

   ```env
   VITE_SERVER_URL=http://localhost:3000/api
   ```

4. **Run the dev server**:
   ```bash
   npm run dev
   ```

---

### ✅ Markdown Rendering

Helpful Notes (markdown) are rendered using:

```bash
npm i react-markdown
```

In `TicketDetail.jsx`:

```jsx
import ReactMarkdown from "react-markdown";

<ReactMarkdown>{ticket.helpfulNotes}</ReactMarkdown>;
```

---

## 👑 Admin Panel (`/admin`)

- Lists all users with their:
  - Name, Email, Role, Skills
- Admin can:
  - Change user `role` via dropdown
  - Assign comma-separated skills → submitted as `array of strings`
- Live email-based search bar

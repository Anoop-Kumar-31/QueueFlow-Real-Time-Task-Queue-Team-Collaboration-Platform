<!-- =========================== -->
<!--           HERO             -->
<!-- =========================== -->

<p align="center">
  <img src="./Image.png" alt="QueueFlow Banner">
</p>

<h1 align="center">
QueueFlow
</h1>

<h3 align="center">
Real-Time Workflow Intelligence for Engineering Teams
</h3>

<p align="center">
Plan, collaborate, monitor, and deliver — all in real time.<br/>
A full-stack SPA built from scratch with WebSocket-first architecture.
</p>

<p align="center">

<img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white&style=for-the-badge">

<img src="https://img.shields.io/badge/Node.js-Express_5-339933?logo=node.js&logoColor=white&style=for-the-badge">

<img src="https://img.shields.io/badge/Socket.io-4.8-010101?logo=socket.io&logoColor=white&style=for-the-badge">

<img src="https://img.shields.io/badge/PostgreSQL-Supabase-4169E1?logo=postgresql&logoColor=white&style=for-the-badge">

<img src="https://img.shields.io/badge/Prisma-ORM-2D3748?logo=prisma&logoColor=white&style=for-the-badge">

</p>

<p align="center">

<img src="https://img.shields.io/github/license/Anoop-Kumar-31/QueueFlow?style=for-the-badge">

<img src="https://img.shields.io/github/stars/Anoop-Kumar-31/QueueFlow?style=for-the-badge">

<img src="https://img.shields.io/github/last-commit/Anoop-Kumar-31/QueueFlow?style=for-the-badge">

<img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge">

</p>

---

## 🔗 Quick Links

| Resource | Link |
|----------|------|
| 🌐 **Live Demo** | [queue-flow-rho.vercel.app](https://queue-flow-rho.vercel.app) |
| 🎨 **Frontend Repo** | [github.com/Anoop-Kumar-31/QueueFlow_Frontend](https://github.com/Anoop-Kumar-31/QueueFlow_Frontend) |
| ⚙️ **Backend Repo** | [github.com/Anoop-Kumar-31/QueueFlow_Backend](https://github.com/Anoop-Kumar-31/QueueFlow_Backend) |

> [!NOTE]
> This repository serves as the **central documentation hub** for QueueFlow.
> The complete frontend and backend implementations are maintained in their own repositories linked above.

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Why QueueFlow?](#-why-queueflow)
- [Screenshots](#-screenshots)
- [Core Features](#-core-features)
- [System Architecture](#-system-architecture)
- [Tech Stack & Rationale](#-tech-stack--rationale)
- [Database Schema](#-database-schema)
- [Real-Time Engine](#-real-time-engine)
- [Frontend Architecture](#-frontend-architecture)
- [API Reference](#-api-reference)
- [Security Model](#-security-model)
- [Key Engineering Decisions](#-key-engineering-decisions)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [Deployment](#-deployment)
- [Future Roadmap](#-future-roadmap)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 Overview

QueueFlow is a **real-time workflow intelligence platform** designed to help software teams collaborate more efficiently.

Unlike traditional project management tools that rely on constant page refreshes and delayed synchronization, QueueFlow uses **persistent WebSocket connections (Socket.IO)** to synchronize every action — task moves, note posts, member joins, status updates — instantly across all connected clients within milliseconds.

The platform combines:
- 🗂️ **Kanban Board** task management with drag-and-drop
- 📊 **Workflow Intelligence** analytics with bottleneck detection
- 👥 **Live collaboration** with real-time activity feeds
- 🔐 **Role-based access control** enforced at both API and UI layers
- 📝 **Sticky Notes** for client feedback and team discussions
- 🟢 **Online presence** tracking across all users

The application is architected as **two independently deployable services**:

| Service | Stack | Hosted On |
|---------|-------|-----------|
| **Frontend** | React 19 · Vite 8 · Redux Toolkit · TailwindCSS v4 | Vercel |
| **Backend** | Node.js · Express 5 · Socket.IO · Prisma · PostgreSQL | Render |

---

## 🚀 Why QueueFlow?

> **Keep every team member synchronized in real time while providing actionable workflow insights.**

Most project management tools are **polling-based** — your browser quietly asks "did anything change?" every few seconds. QueueFlow flips this model:

| Traditional Tools | QueueFlow |
|---|---|
| Polling-based updates (2–5 second delays) | Push-based via WebSocket (< 50ms) |
| Analytics locked behind enterprise tiers | Built-in bottleneck detection & workload analysis |
| Manual email-based invitations | Self-serve join via time-limited invite codes |
| Page refresh required to see changes | Zero-refresh, live-synced across all connected clients |
| Session-based auth requiring DB lookups | Stateless JWT auth — no session store needed |

---

## 📸 Screenshots

<details>
<summary><b>🔐 Authentication</b></summary>
<br/>

**Login Page**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/Login.png" alt="Login" width="100%" style="border-radius: 8px;" />

**Registration**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/SignUp.png" alt="Sign Up" width="100%" style="border-radius: 8px;" />

</details>

<details>
<summary><b>📋 Dashboard & Project Board</b></summary>
<br/>

**Overview Dashboard — Project Cards**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/OverviewDashboard.png" alt="Dashboard" width="100%" style="border-radius: 8px;" />

**Kanban Board with Live Activity Timeline**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/ProjectDashboard.png" alt="Project Board" width="100%" style="border-radius: 8px;" />

</details>

<details>
<summary><b>📝 Task Management</b></summary>
<br/>

**My Task Queue — Drag-and-Drop Reorder**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/MyTask.png" alt="My Tasks" width="100%" style="border-radius: 8px;" />

**Task Details Modal with Sticky Notes**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/TaskDetails.png" alt="Task Details" width="100%" style="border-radius: 8px;" />

</details>

<details>
<summary><b>👥 Collaboration & Access</b></summary>
<br/>

**Join via Invite Code**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/JoinWithProjectCode.png" alt="Join Project" width="100%" style="border-radius: 8px;" />

**Generated Invite Code with Expiry**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/CodeGenerated.png" alt="Invite Code" width="100%" style="border-radius: 8px;" />

**Manage Access (PM Only)**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/ManageAccess(PM).png" alt="Manage Access" width="100%" style="border-radius: 8px;" />

</details>

<details>
<summary><b>📊 Analytics Dashboard</b></summary>
<br/>

**Workflow Intelligence — Bottleneck Detection, Workload, Trends**

<img src="https://raw.githubusercontent.com/Anoop-Kumar-31/QueueFlow_Frontend/main/screenshots/AnalyticalOverview.png" alt="Analytics" width="100%" style="border-radius: 8px;" />

</details>

---

## ⭐ Core Features

### 📋 Kanban Project Board

Visualize and manage tasks across four status columns: `PENDING` → `IN_PROGRESS` → `REVIEW` → `DONE`.

- Real-time task cards with priority indicators (🔴 High, 🟡 Medium, 🟢 Low)
- Online presence dots on assignee badges
- Sticky note count badges per task
- Live activity timeline sidebar
- PM-only controls: create tasks, invite members, manage access, view analytics

### 📝 Personal Task Queue

Every developer gets their own prioritized task queue — a unified view of all tasks assigned to them across every project.

- **Drag-and-drop reordering** via `@hello-pangea/dnd`
- **Optimistic UI updates** — the board reorders instantly, then syncs with the server
- **Inline status change** dropdown per task
- Tasks are **grouped by project** for context

### 📊 Workflow Intelligence Analytics

The analytics dashboard runs **6 parallel server-side queries** and calculates:

| Metric | How It's Computed |
|---|---|
| Completion Rate | `done / total × 100` |
| Avg Completion Time | Mean of `completed_at − started_at` per completed task |
| Bottleneck Detection | Flagged when `REVIEW` count ≥ 25% of total tasks |
| Workload Imbalance | Flagged when max−min task count across devs > 2 |
| Daily Burn Rate | `completed_today − created_today` |
| Trend Data | Day-by-day created vs completed, from task timestamps |
| Priority Breakdown | Count of High, Medium, Low priority tasks |
| Oldest Unfinished | The non-DONE task with the earliest `created_at` |

Rendered with **Recharts** — Pie charts, bar charts, and trend line charts — all React-native with `ResponsiveContainer`.

### 🔐 Authentication & Profile Management

- JWT-based stateless authentication with `Authorization: Bearer` header
- Registration with role selection
- **Profile page** with editable name/email
- **Two-step password change**: verify current password → set new password
- Session persistence via `redux-persist` (only auth state is persisted to localStorage)
- Animated boot screen with server wake-up notice (Render free tier)

### 👥 Team Collaboration

- **Invite Code System**: PMs generate time-limited 6-character alphanumeric codes
- **Self-serve join**: Developers/Clients enter the code to join a project with their chosen role
- **Manage Access**: PMs can view members and remove them; non-PMs can self-remove
- **Sticky Notes** on tasks: CRUD operations with real-time sync — perfect for code reviews, sprint notes, and client feedback

### 🔔 Real-Time Notification System

- Activity events broadcast via Socket.IO to all project room members
- Bell icon with unread count badge
- Notifications auto-ignore the current user's own actions
- Stored in component state (persists across page navigations within the session)
- Capped at 40 notifications in the feed

### 🔍 Instant Search

- Client-side search powered by `useMemo` — filters across projects and tasks in memory
- Zero API calls, instant results as you type
- Keyboard shortcut: `Escape` to close
- Search results link directly to project boards or task views

### 🌗 Dark Mode

- Class-based dark mode via Tailwind CSS v4's `@custom-variant dark`
- `ThemeToggle` component with `localStorage` persistence
- Defaults to dark mode for QueueFlow's premium aesthetic
- Respects system preference via `prefers-color-scheme`

---

## 🏗️ System Architecture

```
┌───────────────────────────────────────────────────────────┐
│                 BROWSER (React 19 SPA)                    │
│  Redux Store ◄──► Socket.IO Client ◄──► REST via fetch    │
│  (auth, projects, tasks)     │        (fetchAPI wrapper)  │
└──────────────────────────────┬────────────────────────────┘
                               │ HTTPS + WSS
┌──────────────────────────────▼────────────────────────────┐
│               Express 5 + Socket.IO SERVER                │
│  JWT Middleware → Project Role Middleware → Controllers   │
│                         ↓                                 │
│                    Prisma ORM                             │
└──────────────────────────────┬────────────────────────────┘
                               │
┌──────────────────────────────▼────────────────────────────┐
│            PostgreSQL (hosted on Supabase)                │
│  Users · Projects · Tasks · Members · Activities · Notes  │
│              + Keep-Alive Cron (every 5 days)             │
└───────────────────────────────────────────────────────────┘
```

**Key Principle:** The backend is the **single source of truth**. Socket events only fire *after* the database write succeeds. The frontend never applies an update that wasn't persisted.

---

## 🛠️ Tech Stack & Rationale

### Backend

| Technology | Chosen Over | Why |
|---|---|---|
| **Node.js + Express 5** | Django, Spring Boot | Non-blocking I/O is critical for a WebSocket-heavy app. Every task move is both a DB write AND a socket broadcast — Node handles both on a single thread efficiently. |
| **Socket.IO 4.8** | Raw WebSockets, SSE | Automatic fallback (long-polling), room-based broadcasting (`io.to(projectId).emit()`), reconnection logic, and namespace support out of the box. |
| **Prisma ORM** | Sequelize, TypeORM | Type-safe queries, schema-first migrations, first-class Supabase support with `directUrl` for connection pooling. |
| **PostgreSQL (Supabase)** | MongoDB, MySQL | Relational integrity is essential — tasks belong to projects, members span users and projects, activities reference tasks with `onDelete: SetNull` to preserve audit history. |
| **JWT (jsonwebtoken)** | Sessions, OAuth | Stateless auth that works for separate frontend/backend deployments. No session store needed. |
| **node-cron** | setInterval | Supabase free-tier keep-alive cron (`SELECT 1` every 5 days) — cleaner than raw intervals. |

### Frontend

| Technology | Chosen Over | Why |
|---|---|---|
| **React 19 + Vite 8** | Next.js, CRA | QueueFlow is a fully authenticated SPA — no SEO benefit to SSR. Vite's dev server is 10–20× faster than CRA's Webpack. |
| **Redux Toolkit** | Context API, Zustand | Three intersecting real-time data sources (auth, projects, tasks). Redux enforces a single unidirectional store with immutable updates, making WebSocket-driven state mutations predictable. `useSelector` with shallow equality prevents unnecessary re-renders. |
| **TailwindCSS v4** | CSS Modules, Chakra UI | Utility-first CSS with `dark:` variants, responsive breakpoints, and custom tokens inline in JSX. No design-system lock-in. |
| **Recharts** | Chart.js, D3 | React-native composable API (`<PieChart><Pie/></PieChart>`) — no imperative DOM manipulation via `useEffect`. |
| **@hello-pangea/dnd** | react-beautiful-dnd | Maintained fork of `react-beautiful-dnd` with React 19 support and active development. |
| **redux-persist** | Manual localStorage | Only the `auth` slice is whitelisted for persistence — projects and tasks are always fetched fresh or pushed via WebSocket. |

---

## 🗃️ Database Schema

> Six models connected through relational foreign keys with strategic `onDelete` behaviors.

<img src="https://github.com/Anoop-Kumar-31/QueueFlow_Backend/blob/main/screenshots/ER_NEW.png" alt="Sign Up" width="100%" style="border-radius: 8px;" />

### Key Design Decisions

| Model | Decision | Reasoning |
|---|---|---|
| **ProjectMember** | `@@unique([user_id, project_id])` | Database-level prevention of duplicate memberships, even under race conditions |
| **Task** | `started_at` / `completed_at` timestamps | Backbone of the analytics engine — enables avg completion time, trend charts, and daily burn rate |
| **ActivityEvent** | `task_id` with `onDelete: SetNull` | Activity log entries survive task deletion — `details` stores the full human-readable string for the timeline |
| **StickyNote** | `onDelete: Cascade` via task | Notes are contextual to a task — deleting a task removes its notes |
| **ProjectInvite** | `expires_at` checked server-side | Prevents stale invite codes from being reused indefinitely |

---

## ⚡ Real-Time Engine

### Room Architecture

Every project gets its own Socket.IO room: `project_${projectId}`.

```javascript
// Client: Join/leave on navigation
socket.emit('join_project', projectId);
socket.emit('leave_project', projectId);

// Server: Broadcast after DB write
io.to(projectId).emit('task_updated', updatedTask);
// → Only members viewing THIS project receive the event
```

### Socket Events

| Event | Trigger | Recipients | Redux Action |
|---|---|---|---|
| `task_created` | PM creates task | Project room | `socketTaskCreated` |
| `task_updated` | Status change / edit | Project room | `socketTaskUpdated` |
| `task_deleted` | PM deletes task | Project room | `socketTaskDeleted` |
| `queue_reordered` | Drag-and-drop save | Project room | `socketQueueReordered` |
| `new_sticky_note` | Note posted | Project room | `socketNewStickyNote` |
| `note_updated` | Note edited | Project room | `socketNoteUpdated` |
| `note_deleted` | Note deleted | Project room | `socketNoteDeleted` |
| `new_activity` | Any state change | Project room | Notification feed |
| `online_users` | Connect / disconnect | Global broadcast | `setOnlineUsers` |

### Online Presence

```javascript
// Server: Map<userId, Set<socketId>> — handles multiple tabs
onlineUsers.set(userId, new Set());
onlineUsers.get(userId).add(socket.id);

// On disconnect: remove socketId, if Set empty → user is offline
io.emit('online_users', Array.from(onlineUsers.keys()));
```

A `Map<userId, Set<socketId>>` is used because a single user can have multiple browser tabs open. Only when all of a user's sockets disconnect is the user considered offline.

---

## 🧩 Frontend Architecture

### Component Tree

```
App.jsx
├── Loading.jsx                 (animated boot screen with progress bar)
├── Login.jsx / Register.jsx    (auth forms)
└── AppLayout.jsx               (socket init, notification state, layout shell)
    ├── layout/AppSidebar.jsx   (collapsible nav — Dashboard, My Tasks, Profile)
    ├── layout/SearchBar.jsx    (live client-side search across projects & tasks)
    ├── layout/NotificationBell.jsx  (real-time notification feed)
    ├── layout/ThemeToggle.jsx  (dark/light mode)
    └── <Outlet /> (page content)
        ├── Dashboard.jsx           (project grid with skeleton loading)
        ├── TasksBoard.jsx          (personal drag-and-drop queue)
        ├── ProjectBoard.jsx        (Kanban board + activity timeline)
        │   ├── ManageAccessModal
        │   ├── ActivityTimeline
        │   ├── TaskDetailsModal
        │   │   └── Sticky Notes CRUD
        │   ├── CreateTaskModal
        │   └── GenerateInviteModal
        ├── AnalyticsDashboard.jsx   (charts, insights, trend analysis)
        └── Profile.jsx             (edit info + two-step password change)
```

### State Management (Redux Toolkit)

| Slice | State | Key Patterns |
|---|---|---|
| `authSlice` | `user`, `token`, `isAuthenticated`, `onlineUsers` | Persisted via `redux-persist`, socket-driven `setOnlineUsers` |
| `projectSlice` | `items[]`, `loading` | REST-fetched, immutable updates |
| `tasksSlice` | `items[]`, `loading` | Hybrid REST + Socket. 7 socket reducers for live updates. Optimistic reorder for drag-and-drop. |

### API Abstraction

All HTTP calls go through a single `fetchAPI()` wrapper that:
1. Reads `VITE_API_URL` from environment
2. Injects `Authorization: Bearer <token>` from the Redux store
3. Handles JSON parsing and error extraction consistently

No component makes a raw `fetch()` call.

---

## 📡 API Reference

### Auth Routes (`/api/auth`)

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| `POST` | `/register` | — | Create account |
| `POST` | `/login` | — | Login, receive JWT |
| `GET` | `/me` | Token | Get current user |
| `POST` | `/verify-password` | Token | Verify current password (for password change flow) |
| `PUT` | `/profile` | Token | Update name/email |
| `PUT` | `/change-password` | Token | Change password |

### Project Routes (`/api/projects`)

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| `POST` | `/` | Token | Create project (creator becomes PM) |
| `GET` | `/` | Token | List user's projects |
| `GET` | `/:id` | Token | Project details |
| `GET` | `/:id/members` | Token | List project members |
| `GET` | `/:id/activities` | Token | Activity timeline |
| `GET` | `/:id/analytics` | Token | Workflow intelligence data |
| `POST` | `/:id/generate-invite` | Token + PM | Generate time-limited invite code |
| `POST` | `/join` | Token | Join project via invite code |
| `DELETE` | `/:id/members/:userId` | Token | Remove member (PM) or self-leave |

### Task Routes (`/api/tasks`)

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| `POST` | `/project/:projectId` | Token + PM | Create & assign task |
| `GET` | `/project/:projectId` | Token | Get all project tasks |
| `GET` | `/queue/:userId` | Token | Get user's personal task queue |
| `PUT` | `/:taskId` | Token | Update task (status, title, etc.) |
| `DELETE` | `/:taskId` | Token | Delete task |
| `PUT` | `/reorder` | Token | Batch reorder task positions (atomic transaction) |
| `POST` | `/:taskId/notes` | Token | Add sticky note |
| `PUT` | `/notes/:noteId` | Token | Edit sticky note |
| `DELETE` | `/notes/:noteId` | Token | Delete sticky note |

---

## 🔐 Security Model

| Layer | Mechanism |
|---|---|
| **Authentication** | JWT signed with `JWT_SECRET`, sent as `Authorization: Bearer` header |
| **Route Protection** | `verifyToken` middleware validates JWT on every protected endpoint |
| **Project-Level RBAC** | `checkProjectRole(['PM'])` middleware queries `ProjectMember` table — per-project role enforcement |
| **Sticky Note Ownership** | `author_id === req.user.id` checked before edit/delete |
| **Member Removal** | PM can remove any member; non-PMs can only self-remove |
| **Invite Expiry** | `expires_at` checked server-side before allowing join |
| **Password Storage** | bcrypt with default salt rounds |
| **Frontend Guards** | `ProtectedRoute` / `AuthRoute` wrappers redirect unauthenticated users |

---

## 🧠 Key Engineering Decisions

### 1. Preventing Duplicate Task Entries (REST + Socket Race)

**Problem:** When a PM creates a task, the Redux thunk receives it from the REST `201` response AND the socket broadcast fires `task_created` — causing duplicates.

**Solution:** Idempotency guard in the reducer:
```javascript
socketTaskCreated: (state, action) => {
  if (!state.items.find(t => t.id === action.payload.id)) {
    state.items.push(action.payload);
  }
}
```

### 2. Task Flicker on Project Navigation

**Problem:** Navigating between projects briefly showed stale tasks from the previous project.

**Solution:** `fetchProjectTasks.pending` clears `state.items = []` immediately before new data arrives.

### 3. Optimistic Drag-and-Drop Reorder

**Problem:** 200–400ms delay between drag-release and visual confirmation.

**Solution:** `optimisticReorder` updates the Redux store immediately. The backend reorder uses a Prisma `$transaction` to atomically update all positions. If the API fails, the state could be reverted.

### 4. Multi-Tab Online Presence

**Problem:** A user with 3 browser tabs has 3 socket IDs. Disconnecting one tab shouldn't show them as offline.

**Solution:** Server-side `Map<userId, Set<socketId>>`. A user is only marked offline when their entire Set is empty.

### 5. Activity Audit Trail Preservation

**Problem:** Deleting a task would cascade-delete its activity events, destroying the audit trail.

**Solution:** `ActivityEvent.task_id` uses `onDelete: SetNull`. The log entry survives with `task_id = null`. The `details` string stores the full human-readable context (e.g., *"Priya deleted 'Setup OAuth'"*).

### 6. Supabase Free-Tier Keep-Alive

**Problem:** Supabase pauses free-tier databases after 7 days of inactivity.

**Solution:** A `node-cron` job runs `SELECT 1` every 5 days to keep the connection alive.

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** v18+
- **npm** v9+
- **PostgreSQL** database (or a free [Supabase](https://supabase.com) instance)

### 1. Clone the Repositories

```bash
# Frontend
git clone https://github.com/Anoop-Kumar-31/QueueFlow_Frontend.git
cd QueueFlow_Frontend && npm install

# Backend
git clone https://github.com/Anoop-Kumar-31/QueueFlow_Backend.git
cd QueueFlow_Backend && npm install
```

### 2. Configure Environment Variables

See the [Environment Variables](#-environment-variables) section below.

### 3. Initialize the Database

```bash
cd QueueFlow_Backend
npx prisma generate
npx prisma db push
```

### 4. Start Development Servers

```bash
# Terminal 1 — Backend
cd QueueFlow_Backend
npm run dev          # → http://localhost:5000

# Terminal 2 — Frontend
cd QueueFlow_Frontend
npm run dev          # → http://localhost:5173
```

---

## 🔑 Environment Variables

### Frontend (`.env`)

```env
VITE_API_URL=http://localhost:5000/api
```

### Backend (`.env`)

```env
PORT=5000
DATABASE_URL=postgresql://user:password@host:5432/dbname?pgbouncer=true
DIRECT_URL=postgresql://user:password@host:5432/dbname
JWT_SECRET=your-secret-key
CLIENT_URL=http://localhost:5173
```

> [!IMPORTANT]
> Supabase users: Use the **connection pooler** URL for `DATABASE_URL` and the **direct** connection URL for `DIRECT_URL`. Prisma needs both for migrations and runtime queries.

---

## ☁️ Deployment

| Service | Platform | Configuration |
|---|---|---|
| **Frontend** | [Vercel](https://vercel.com) | Auto-deploys from `main` branch. Set `VITE_API_URL` in Vercel Environment Variables. |
| **Backend** | [Render](https://render.com) | Web Service with Build Command: `npm install && npx prisma generate`, Start Command: `node src/server.js`. Set all backend env vars. |
| **Database** | [Supabase](https://supabase.com) | Free-tier PostgreSQL with connection pooling enabled. |

> [!TIP]
> The backend includes a Render free-tier wake-up flow: the frontend pings `/api/health` on startup and shows an animated loading screen while the server boots (typically 10–20 seconds on first load after sleep).

---

## 🗺️ Future Roadmap

- [ ] 📋 **Drag-and-drop between Kanban columns** — move tasks across status groups directly on the board
- [ ] 💬 **Task Comments** — threaded discussion per task (separate from sticky notes)
- [ ] 📎 **File Attachments** — upload docs, images, and designs to tasks
- [ ] 📧 **Email Notifications** — digest emails for offline team members
- [ ] 📱 **Mobile-Responsive Kanban** — touch-optimized drag-and-drop for mobile devices
- [ ] 🔔 **Push Notifications** — browser push for critical events (via Service Workers)
- [ ] 📊 **Cross-Project Analytics** — unified metrics dashboard across all projects
- [ ] 🧪 **E2E Testing** — Cypress/Playwright test suite for critical workflows

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the relevant repository ([Frontend](https://github.com/Anoop-Kumar-31/QueueFlow_Frontend) or [Backend](https://github.com/Anoop-Kumar-31/QueueFlow_Backend))
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add: your feature description'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a **Pull Request** with a clear description of the changes

---

## 📄 License

This project is licensed under the [GPL-3.0 License](LICENSE).

---

<p align="center">
  <b>Built by <a href="https://github.com/Anoop-Kumar-31">Anoop Kumar</a></b> · Full Stack Developer
  <br/><br/>
  <sub>⭐ If you find this project useful, consider giving it a star!</sub>
</p>

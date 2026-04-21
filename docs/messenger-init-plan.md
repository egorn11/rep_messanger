## Messenger Initialization Plan (Central University)

### 1) Product Framing
- Goal: build a modern university messenger for students, teachers, and admin teams.
- Value: fast communication, official announcements, study-group collaboration, and secure identity.
- Initial platforms: Web first, then iOS/Android wrappers.

### 2) Core Roles and MVP Scope
- Student: personal and group chats, course channels, notifications.
- Teacher: class chats, announcements, file sharing.
- Admin: organization channels, moderation, user lifecycle management.
- MVP features:
  - Auth (email/phone + university identity binding)
  - 1:1 chats
  - Group chats
  - Channel announcements
  - File/image attachments
  - Push/in-app notifications
  - Read receipts and typing indicators

### 3) Technical Initialization
- Create architecture baseline:
  - Frontend: React + TypeScript
  - Backend API: Node.js + TypeScript
  - Realtime: WebSocket gateway
  - Database: PostgreSQL
  - Cache/presence: Redis
- Set shared standards:
  - mono-repo layout
  - linting, formatting, commit checks
  - env templates and secrets policy
  - CI skeleton (build, test, lint)

### 4) Decomposition Into Small Tasks

#### Track A - Product and Design
1. Define user stories for Student/Teacher/Admin.
2. Build information architecture for chat, channels, profile, settings.
3. Create design tokens (color, spacing, typography).
4. Create clickable low-fidelity prototype.

#### Track B - Frontend Foundation
1. Initialize app shell (routing, layout, auth guard).
2. Build message list UI and chat input UI.
3. Add channel list and unread badge components.
4. Implement API client and WebSocket client layers.

#### Track C - Backend Foundation
1. Initialize API service with module boundaries.
2. Implement auth module (signup/signin/session).
3. Implement chat module (dialogs, groups, channels).
4. Implement message module (send/edit/delete/read state).
5. Add realtime event broadcasting over WebSocket.

#### Track D - Data and Infra
1. Define PostgreSQL schema and migrations.
2. Add Redis for online presence and pub/sub.
3. Configure object storage for attachments.
4. Add Docker compose for local full-stack run.

#### Track E - Quality and Security
1. Add unit/integration test baseline.
2. Add authorization matrix for role checks.
3. Add audit logs for moderation/admin actions.
4. Add observability: logs + metrics + error tracking.

### 5) Delivery Milestones
- Milestone 0: foundation bootstrapped, CI green.
- Milestone 1: authenticated 1:1 chat works end-to-end.
- Milestone 2: group chats and channels with notifications.
- Milestone 3: moderation/admin console and beta release.

### 6) Branding Decision For First Icon
- Source checked: official website `https://cu.ru`.
- Extracted element: monochrome vector symbol from CU favicon asset (`/assets/kit/favicon/safari-pinned-tab.svg`).
- App icon strategy:
  - square shape for app stores
  - dark blue corporate background (`#0B1F3A`)
  - white university symbol centered
  - rounded corners to fit mobile launcher style

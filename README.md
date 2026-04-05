# 🚀 Docmost - Open-Source Collaboration Platform

[![Docmost](https://img.shields.io/badge/Docmost-Open--Source-blue?style=for-the-badge&logo=docmost)](https://docmost.com)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-AGPL%203.0-brightgreen.svg?style=for-the-badge)](LICENSE)

**Docmost** is a self-hosted, open-source collaborative wiki and documentation platform. It provides a real-time collaborative editor, allowing multiple users to edit pages simultaneously, similar to Confluence or Notion.

---

## ✨ Features

- **Real-Time Collaboration:** Fast and seamless editing with multiple users.
- **Spaces & Nested Pages:** Organize your documentation using spaces and structured hierarchies.
- **Rich Media Support:** Integrate diagrams (**Draw.io**, **Excalidraw**, **Mermaid**), tables, math (KaTeX), and more.
- **Powerful Permissions:** Robust access control for workspaces and spaces.
- **Search:** Instant discovery via PostgreSQL full-text search.
- **Version Control:** Comprehensive history for tracking changes and reverting if needed.

---

## 🛠️ Quick Start with Docker

To get Docmost up and running locally, follow these steps:

### 1. Prerequisites
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 2. Configure Environment Variables
Copy the `.env.example` to `.env` and update the values as needed.

```bash
cp .env.example .env
```

Make sure to set a secure `APP_SECRET` and `POSTGRES_PASSWORD`.

### 3. Start the Services
Run the following command in the root directory:

```bash
docker-compose up -d
```

Docmost will be accessible at `http://localhost:3000`.

---

## 🚀 Deploy to Render

You can easily deploy Docmost to **Render** using the provided `render.yaml` Blueprint. This file automatically handles:
- **Managed PostgreSQL** for content storage.
- **Managed Redis** for caching.
- **Persistent Disk** for storing your uploads and documentation data.

### How to Deploy:
1.  **Push your code** to a GitHub or GitLab repository.
2.  Log in to your **[Render Dashboard](https://dashboard.render.com/)**.
3.  Click **New +** and select **Blueprint**.
4.  Connect your repository.
5.  Render will auto-detect the `render.yaml` and prompt you to create the services. Wait for the initial build and deployment to complete.

---

## 🏗️ Services Included

| Service | Image | Description |
|---------|-------|-------------|
| **Docmost** | `docmost/docmost:latest` | The core application service. |
| **Database** | `postgres:16` | PostgreSQL database for content and metadata storage. |
| **Redis** | `redis:8` | Redis for caching and messaging. |

---

## 🐳 Docker Volumes

- `docmost`: Local storage for application data.
- `db_data`: Persistent storage for the PostgreSQL database.
- `redis_data`: Cache persistence for Redis.

---

## 📝 License

Docmost is licensed under the **AGPL-3.0**. See the [official documentation](https://docmost.com) for more details.

---

*Enjoy collaborative documentation with Docmost!* ⭐

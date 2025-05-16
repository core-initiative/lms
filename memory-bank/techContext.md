# Tech Context: Frappe Learning (Frappe LMS)

## Technologies Used
- **Backend:**
  - Frappe Framework (Python)
  - Python 3.10+
  - RESTful APIs, WebSockets
  - Integrations: Zoom, Unsplash, Razorpay
- **Frontend:**
  - Vue 3
  - Pinia (state management)
  - TailwindCSS (utility-first CSS)
  - Frappe UI (Vue component library)
  - Vite (build tool)
  - Cypress (E2E testing)
- **DevOps:**
  - Docker, Docker Compose
  - Frappe Cloud (optional managed hosting)
  - Pre-commit hooks, linting, and formatting

## Development Setup
- **Backend:**
  - Install via Frappe bench or Docker Compose
  - Python dependencies managed via `pyproject.toml` and `requirements.txt`
  - Custom app structure under `lms/`
- **Frontend:**
  - Standalone Vue app in `frontend/`
  - Run with `yarn dev` (Vite server, port 8080)
  - Proxy to backend (usually on port 8000)
  - CSRF handling for local development
- **Testing:**
  - Cypress for frontend E2E tests
  - Python unittest for backend logic
  - Pre-commit hooks for code quality

## Technical Constraints
- Requires Python 3.10+
- Frappe Framework compatibility (version alignment required)
- Docker recommended for local and production deployments
- SPA frontend expects API endpoints and CSRF configuration

## Dependencies
- **Backend:**
  - `websocket_client`, `markdown`, `beautifulsoup4`, `lxml`, `cairocffi`, `razorpay`, `fuzzywuzzy`, and others
- **Frontend:**
  - Vue 3, Pinia, TailwindCSS, Frappe UI, Chart.js, ApexCharts, Editor.js plugins, socket.io-client, and more

---

This document provides the technical context for Frappe Learning, supporting development, setup, and maintenance. 
# System Patterns: Frappe Learning (Frappe LMS)

## System Architecture
- **Backend:** Built on Frappe Framework (Python), leveraging its event-driven architecture, hooks, and extensibility.
- **Frontend:** SPA built with Vue 3, Pinia, TailwindCSS, and Frappe UI, communicating with the backend via RESTful APIs and WebSockets.
- **Deployment:** Supports Docker-based and Frappe Cloud deployments, with automated setup scripts.

## Key Technical Decisions
- **Separation of Concerns:** Clear split between backend (business logic, data, integrations) and frontend (UI, state management, routing).
- **Extensibility:**
  - **Hooks:** Backend uses Frappe hooks for event handling, scheduled tasks, and custom routing.
  - **Plugins:** Plugin system for profile tabs and page extensions (custom JS/CSS injection).
  - **Widgets:** Jinja-based reusable HTML components for rapid UI composition.
- **SPA Navigation:** Frontend uses Vue Router for dynamic, client-side navigation and deep-linking.
- **API Integrations:** Modular integration with external services (Zoom, Unsplash, Razorpay) via backend modules.
- **Testing:** Cypress for E2E frontend tests, unittest for backend logic, and pre-commit hooks for code quality.

## Design Patterns
- **Plugin Pattern:** For extensible profile tabs and page extensions.
- **Widget/Macro Pattern:** Jinja widgets for reusable UI elements.
- **Event-Driven:** Frappe hooks for document events, scheduled jobs, and custom logic injection.
- **Resource Fetching:** Frontend uses resource and list resource patterns for API data fetching and caching.
- **SPA/SSR Hybrid:** Custom page renderers in backend for profile, SCORM, and static pages.

## Component Relationships
- **Backend Modules:**
  - `plugins.py`: Defines plugin interfaces and implementations.
  - `widgets.py`: Provides widget system for reusable UI.
  - `page_renderers.py`: Handles custom page rendering logic.
  - `install.py`: Manages setup, roles, and permissions.
  - `routing.py`: Custom route converters and utilities.
- **Frontend Components:**
  - `App.vue`: Root component, layout switching.
  - `router.js`: Defines all main routes (courses, lessons, batches, jobs, quizzes, profiles, etc.).
  - `pages/`: Vue components for each main view (Courses, CourseDetail, Lesson, Profile, etc.).
  - `components/`: Reusable UI elements (CourseCard, CourseOutline, UserAvatar, etc.).
  - `stores/`: Pinia stores for user/session/settings state.

---

This document captures the core system patterns and architecture for Frappe Learning, supporting future development and onboarding. 
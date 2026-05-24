# Book Search Engine

A full-stack book discovery app where users can search any title or author, save books to a personal list, and manage their collection. Built with the MERN stack — refactored from a REST API to GraphQL/Apollo as a learning exercise in API architecture.

---

## Features

- **Book search** — powered by the Google Books API, returns title, author, description, cover image, and a link to Google Books
- **User authentication** — signup and login with JWT-based sessions
- **Save and manage books** — logged-in users can save books to their profile and remove them later
- **Responsive design** — works across desktop and mobile

---

## Tech Stack

| | |
|---|---|
| Frontend | React, Bootstrap |
| Backend | Node.js, Express.js |
| Database | MongoDB + Mongoose |
| API layer | GraphQL + Apollo Server/Client |
| Auth | JWT + bcrypt |
| External API | Google Books API |

---

## Getting Started

### Prerequisites

- Node.js 18+
- MongoDB (local or Atlas)

### Install and run

```bash
git clone https://github.com/VithusanU/Book-Search-Engine.git
cd Book-Search-Engine
npm install
npm run develop
```

This starts both the Express server and the React dev server concurrently.

---

## Project Structure

```
Book-Search-Engine/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Navbar, LoginForm, SignupForm, BookCard
│   │   ├── pages/          # SearchBooks, SavedBooks
│   │   └── utils/          # Apollo client, auth helpers, GraphQL queries/mutations
│   └── public/
└── server/                 # Express + Apollo Server
    ├── models/             # User Mongoose model
    ├── schemas/            # GraphQL typeDefs + resolvers
    └── utils/              # JWT auth middleware
```

---

## Why GraphQL

The original project used a REST API. Migrating to GraphQL meant replacing multiple endpoints with a single typed schema — `searchBooks`, `saveBook`, `removeBook` — and co-locating data requirements with the components that use them. The result is fewer over-fetching issues and a more maintainable API contract as the app grows.

---

## License

MIT

---

*Built by [Vithusan Uruthirakumaran](https://github.com/VithusanU)*

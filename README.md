## E‑Commerce Website (React + Express + MongoDB)

This repository contains a minimal e‑commerce app:
- Browse products
- View product details
- Manage a client‑side shopping cart

### Tech Stack
- Frontend: React 18, React Router, Vite
- Backend: Node.js, Express, Mongoose
- Database: MongoDB

### Monorepo Structure
```
backend/   # Express API
frontend/  # React app (Vite)
docs/      # Technical architecture
```

### Prerequisites
- Node.js 18+
- MongoDB running locally (or a connection string)

### Setup
1) Backend
```
cd backend
npm install
```
Create a `.env` file (optional; defaults shown):
```
MONGODB_URI=mongodb://localhost:27017/ecommerce_dev
PORT=5000
CLIENT_ORIGIN=http://localhost:5173
```
Seed sample data:
```
npm run seed
```
Run the API:
```
npm run dev
```
The API is now at `http://localhost:5000` (health at `/api/health`).

2) Frontend
```
cd ../frontend
npm install
```
Create a `.env` file (optional; defaults shown):
```
VITE_API_BASE=http://localhost:5000/api
```
Run the dev server:
```
npm run dev
```
The app is at `http://localhost:5173`.

### Key Endpoints
- `GET /api/products?page=1&pageSize=12&q=shirt&category=Apparel`
- `GET /api/products/:idOrSlug`

### Notes
- Cart is stored client‑side in `localStorage`
- Replace sample images/brands with your own as needed

### Docs
- See `docs/architecture.md` for the technical architecture.



# OctoFit Tracker

A modern multi-tier fitness tracking application built with React 19, Express, TypeScript, and MongoDB.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
│   ├── src/          # React source files
│   ├── package.json  # Frontend dependencies
│   └── vite.config.js
└── backend/          # Node.js + Express + TypeScript + Mongoose
    ├── src/          # TypeScript source files
    ├── dist/         # Compiled JavaScript (generated)
    ├── package.json  # Backend dependencies
    └── tsconfig.json # TypeScript configuration
```

## Technology Stack

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and dev server
- **Port:** 5173

### Backend
- **Node.js** - Runtime
- **Express** - Web framework
- **TypeScript** - Type safety
- **Mongoose** - MongoDB ODM
- **Port:** 8000

### Database
- **MongoDB** - Document database
- **Port:** 27017

## Prerequisites

- Node.js (v18 or higher)
- npm (v9 or higher)
- MongoDB (running on localhost:27017)

## Installation & Setup

### Backend Setup

```bash
cd octofit-tracker/backend

# Dependencies are already installed
# To install manually: npm install

# Development
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

### Frontend Setup

```bash
cd octofit-tracker/frontend

# Dependencies are already installed
# To install manually: npm install

# Development
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Running the Application

1. **Start MongoDB** (if not already running):
   ```bash
   mongod
   ```

2. **Start Backend Server** (Terminal 1):
   ```bash
   cd octofit-tracker/backend
   npm run dev
   ```
   Backend will be available at `http://localhost:8000`

3. **Start Frontend Dev Server** (Terminal 2):
   ```bash
   cd octofit-tracker/frontend
   npm run dev
   ```
   Frontend will be available at `http://localhost:5173`

## API Endpoints

- `GET /` - Welcome message
- `GET /health` - Health check endpoint

## Environment Configuration

Backend configuration is documented in `.env.example`. Create a `.env` file if you need to customize:

```
MONGODB_URI=mongodb://localhost:27017/octofit
PORT=8000
NODE_ENV=development
```

## Development Workflow

- Frontend hot reload is enabled via Vite
- Backend uses `ts-node` for development with TypeScript directly
- Both services can run simultaneously in separate terminals
- MongoDB must be running for backend operations

## Build & Deployment

### Backend
```bash
npm run build  # Creates ./dist folder
npm start      # Runs compiled JavaScript
```

### Frontend
```bash
npm run build  # Creates ./dist folder
npm run preview # Preview the production build
```

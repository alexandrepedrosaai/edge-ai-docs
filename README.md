# Edge AI Documentation

A modern web application for Edge AI documentation, built with React, TypeScript, and Express.

## 🚀 Quick Start

### Development

```bash
# Install dependencies
pnpm install

# Start development server
pnpm run dev
```

The application will be available at `http://localhost:3000`

### Production Build

```bash
# Build the application
pnpm run build

# Start production server
pnpm start
```

## 📦 Deployment

This application supports multiple deployment options:

### Option 1: Docker

The easiest way to deploy is using Docker:

```bash
# Build the Docker image
docker build -t edge-ai-docs .

# Run the container
docker run -p 3000:3000 edge-ai-docs
```

Or use Docker Compose:

```bash
docker-compose up -d
```

### Option 2: Render

1. Fork/clone this repository
2. Create a new Web Service on [Render](https://render.com)
3. Connect your repository
4. Render will automatically detect the `render.yaml` configuration
5. Deploy!

The `render.yaml` file is already configured with the correct build and start commands.

### Option 3: Vercel

While this is a Node.js application, you can deploy the static build to Vercel:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

The `vercel.json` file is already configured for deployment.

### Option 4: Railway

1. Fork/clone this repository
2. Create a new project on [Railway](https://railway.app)
3. Connect your repository
4. Railway will automatically detect the `railway.json` configuration
5. Deploy!

### Option 5: Any Node.js Host

Deploy to any Node.js hosting provider (Heroku, DigitalOcean, AWS, etc.):

1. Build the application: `pnpm run build`
2. Set environment variables (see below)
3. Start the server: `pnpm start`

## 🔧 Environment Variables

- `NODE_ENV` - Set to `production` for production builds (default: `development`)
- `PORT` - Port to run the server on (default: `3000`)

## 📋 Scripts

- `pnpm dev` - Start development server with hot reload
- `pnpm build` - Build for production (client + server)
- `pnpm start` - Start production server
- `pnpm check` - Run TypeScript type checking
- `pnpm format` - Format code with Prettier

## 🏗️ Project Structure

```
edge-ai-docs/
├── client/              # Frontend React application
│   ├── src/            # React source code
│   ├── public/         # Static assets
│   └── index.html      # HTML template
├── server/             # Backend Express server
│   └── index.ts        # Server entry point
├── shared/             # Shared types and utilities
├── dist/               # Built application (generated)
│   ├── public/         # Built frontend
│   └── index.js        # Built server
├── Dockerfile          # Docker configuration
├── docker-compose.yml  # Docker Compose configuration
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions CI/CD
```

## 🔄 CI/CD

This project includes a GitHub Actions workflow that:

1. Runs type checking
2. Builds the application
3. Builds a Docker image
4. Uploads build artifacts

The workflow runs on:
- Push to `main` or `master` branches
- Pull requests to `main` or `master` branches
- Manual workflow dispatch

To enable Docker image publishing, uncomment the relevant sections in `.github/workflows/deploy.yml` and configure your Docker Hub credentials as GitHub secrets.

## 🛠️ Tech Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS, Vite
- **Backend**: Express, Node.js
- **UI Components**: Radix UI, Lucide React
- **Routing**: Wouter
- **Styling**: Tailwind CSS v4
- **Package Manager**: pnpm

## 📝 License

MIT

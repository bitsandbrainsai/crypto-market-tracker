<div align="center">
  <img 
    src="assets/Crypto Market Intelligence Platform.png" 
    alt="Crypto Market Intelligence Platform Logo Animation"
    width="100%"
  />

  <h1 style="font-size: 3em; font-weight: 800; margin: 0.4em 0 0;">
    Crypto Market Intelligence Platform  
  </h1>

  <h3 style="margin-top: 0.6em;">
    Real-Time Insights. Predictive Intelligence. High-Performance Crypto Analytics. 
  </h3>

  <p>
    <em>An ultra-modern, high-performance cryptocurrency intelligence platform engineered for real-time market visibility, advanced analytics, and seamless user interaction. Built on a scalable, API-driven architecture, the system delivers live crypto price tracking, precision-driven historical charting, and intelligent watchlists with minimal latency and optimized rendering performance. </em>
  </p>
<p>
    <img src="https://img.shields.io/badge/Status-Ready%20for%20Deployment-success" />
    <img src="https://img.shields.io/badge/License-MIT-blue" />
  </p>

</div>

## ✨ Features

- **Real-time Price Tracking**: Live cryptocurrency price updates via WebSocket
- **Interactive Charts**: Visualize price history with Chart.js
- **Watchlists**: Create custom watchlists to track your favorite cryptocurrencies
- **Price Alerts**: Set up notifications when prices hit your target values
- **Dark Mode**: Beautiful dark theme powered by Tailwind CSS
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Market Analytics**: View market cap, volume, 24h changes, and more

## 🛠 Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and optimized builds
- **TailwindCSS** for styling
- **shadcn/ui** components (Radix UI primitives)
- **TanStack Query** for server state management
- **Chart.js** for data visualization
- **Wouter** for routing

### Backend
- **Express.js** with TypeScript (ESM)
- **PostgreSQL** with Drizzle ORM
- **WebSocket** (ws) for real-time updates
- **Passport.js** for authentication
- **CoinGecko API** for cryptocurrency data

## 📋 Prerequisites

- **Node.js** 18+ and npm
- **PostgreSQL** database (recommended: [Neon Database](https://neon.tech) free tier)

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/CryptoPulse.git
cd CryptoPulse
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
DATABASE_URL=postgresql://user:password@host:5432/cryptopulse
PORT=5000
NODE_ENV=development
SESSION_SECRET=your-secret-key-here
```

See [`.env.example`](.env.example) for detailed configuration options.

### 4. Initialize Database

Push the database schema:

```bash
npm run db:push
```

### 5. Run Development Server

```bash
npm run dev
```

Open [http://localhost:5000](http://localhost:5000) in your browser.

## 🌐 Environment Variables

| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `DATABASE_URL` | PostgreSQL connection string | ✅ Yes | - |
| `PORT` | Server port | ❌ No | `5000` |
| `NODE_ENV` | Environment (`development` or `production`) | ❌ No | `development` |
| `SESSION_SECRET` | Secret key for session encryption | ✅ Yes | - |

### Database Setup (Neon)

1. Sign up at [neon.tech](https://neon.tech)
2. Create a new project
3. Copy the connection string
4. Add to your `.env` file as `DATABASE_URL`

## 📦 Build & Deployment

### Build for Production

```bash
npm run build
```

This creates:
- `dist/public/` - Frontend static assets
- `dist/index.js` - Backend server bundle

### Run Production Build

```bash
npm start
```

## 🚀 Deploy to Vercel

### One-Click Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/CryptoPulse)

### Manual Deployment

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/yourusername/CryptoPulse.git
   git push -u origin main
   ```

2. **Import to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will auto-detect the build settings

3. **Configure Environment Variables**
   
   In Vercel dashboard → Settings → Environment Variables, add:
   - `DATABASE_URL` - Your Neon database connection string
   - `SESSION_SECRET` - A random secret key ([generate one](https://randomkeygen.com/))

4. **Deploy**
   
   Click "Deploy" and wait for the build to complete!

## 🗂 Project Structure

```
CryptoPulse/
├── client/              # React frontend
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── hooks/       # Custom React hooks
│   │   ├── lib/         # Utilities & helpers
│   │   └── pages/       # Page components
│   └── index.html
├── server/              # Express backend
│   ├── index.ts         # Server entry point
│   ├── routes.ts        # API routes
│   ├── storage.ts       # Database abstraction
│   └── vite.ts          # Vite integration
├── shared/              # Shared types & schemas
│   └── schema.ts        # Database schema (Drizzle)
├── package.json
├── vite.config.ts
├── drizzle.config.ts
└── tsconfig.json
```

## 🔧 Development Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm start` | Run production server |
| `npm run check` | TypeScript type checking |
| `npm run db:push` | Push database schema changes |

## 🐛 Troubleshooting

### Database Connection Issues

- Verify `DATABASE_URL` is correct in `.env`
- Ensure database is running and accessible
- Check firewall/network settings

### Build Errors

- Clear `node_modules` and reinstall: `rm -rf node_modules package-lock.json && npm install`
- Ensure Node.js version is 18+
- Run `npm run check` to identify TypeScript errors

### Port Already in Use

- Change `PORT` in `.env` file
- Kill process using port 5000: `npx kill-port 5000`

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- [CoinGecko API](https://www.coingecko.com/api) for cryptocurrency data
- [shadcn/ui](https://ui.shadcn.com/) for beautiful UI components
- [Neon Database](https://neon.tech) for serverless PostgreSQL

---

Built with ❤️ using React & Express

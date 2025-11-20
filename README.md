# LeadX CRM - Frontend

React + Vite frontend application for LeadX CRM system.

## 🚀 Quick Start

### Development
```bash
npm install
npm run dev
```

### Build for Production
```bash
npm run build
```

## 📦 Deployment to Vercel

### Prerequisites
- GitHub repository with your code
- Vercel account (free tier works)
- Backend API deployed separately

### Deployment Steps

1. **Push code to GitHub**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Deploy on Vercel**
   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "Add New Project"
   - Import your GitHub repository
   - Configure:
     - **Framework Preset**: Vite
     - **Root Directory**: `LeadX_crm/leadx-frontend`
     - **Build Command**: `npm run build` (auto-detected)
     - **Output Directory**: `dist` (auto-detected)

3. **Set Environment Variables**
   In Vercel project settings, add:
   ```
   VITE_API_URL=https://your-backend-url.com
   ```
   Replace with your actual backend API URL.

4. **Deploy**
   Click "Deploy" and wait for build to complete.

### Environment Variables

Create a `.env` file for local development:
```env
VITE_API_URL=http://localhost:5000
```

For production, set `VITE_API_URL` in Vercel dashboard to your deployed backend URL.

## 🛠️ Tech Stack

- **React 19.1.1** - UI Framework
- **Vite 7.1.2** - Build Tool
- **Tailwind CSS 4.1.12** - Styling
- **Ant Design 4.24.16** - UI Components
- **React Router 7.8.2** - Routing
- **Socket.io Client 4.8.1** - Real-time Communication
- **Axios 1.11.0** - HTTP Client
- **Formik + Yup** - Form Management

## 📁 Project Structure

```
src/
├── components/      # Reusable components
├── context/         # React Context providers
├── pages/           # Page components
│   ├── admin/       # Admin pages
│   ├── ambassador/   # Ambassador pages
│   ├── user/        # User pages
│   └── auth/        # Authentication pages
└── utils/           # Utility functions
```

## 🔧 Configuration

The `vercel.json` file is configured for:
- SPA routing (all routes redirect to index.html)
- Asset caching for better performance
- Automatic build and deployment

## 📝 Notes

- Frontend is deployed as a static site
- Backend must be deployed separately (Railway, Render, etc.)
- Ensure CORS is configured in backend to allow Vercel domain
- Socket.io connection requires backend WebSocket support

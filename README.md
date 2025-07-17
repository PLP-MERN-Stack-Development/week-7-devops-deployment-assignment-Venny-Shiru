# 🚀 MERN Stack Application with DevOps

A full-stack task management application built with MongoDB, Express.js, React, and Node.js, featuring complete deployment and DevOps setup.

## 🌟 Features

### Frontend (React)
- ⚡ Modern React with Hooks and Context API
- 🎨 Tailwind CSS for styling
- 📱 Responsive design
- 🔐 JWT-based authentication
- 📊 Real-time dashboard with task statistics
- ✅ Task management with CRUD operations
- 🔍 Search and filtering capabilities
- 🎯 Priority-based task organization

### Backend (Node.js/Express)
- 🛡️ Secure authentication with JWT
- 🗃️ MongoDB with Mongoose ODM
- 🔒 Security middleware (Helmet, CORS, Rate Limiting)
- 📝 Comprehensive logging with Winston
- 🏥 Health check endpoints
- ⚡ Optimized with compression and caching
- 🧪 Unit tests with Jest

### DevOps & Deployment
- 🔄 CI/CD pipeline with GitHub Actions
- 🐳 Docker containerization
- 📊 Application monitoring and health checks
- 🚀 Production-ready deployment configurations
- 📈 Performance optimization
- 🔐 Security best practices

## 🛠️ Tech Stack

**Frontend:**
- React 18
- React Router DOM
- React Query
- Tailwind CSS
- Vite
- Axios

**Backend:**
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Winston Logger
- Jest for testing

**DevOps:**
- Docker & Docker Compose
- GitHub Actions
- Netlify (Frontend)
- Render (Backend)
- MongoDB Atlas

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- MongoDB (local or Atlas)
- Git

### Local Development

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd mern-deployment-project
   ```

2. **Install dependencies**
   ```bash
   npm run install-deps
   ```

3. **Set up environment variables**
   ```bash
   # Backend (.env in server directory)
   cp server/.env.example server/.env
   
   # Frontend (.env in client directory)
   cp client/.env.example client/.env
   ```

4. **Start MongoDB** (if running locally)
   ```bash
   mongod
   ```

5. **Run the application**
   ```bash
   npm run dev
   ```

   This will start:
   - Backend server on http://localhost:5000
   - Frontend development server on http://localhost:5173

### Using Docker

1. **Start with Docker Compose**
   ```bash
   docker-compose up -d
   ```

   This will start all services:
   - MongoDB on port 27017
   - Backend on port 5000
   - Frontend on port 5173

## 📁 Project Structure

```
mern-deployment-project/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── contexts/       # React contexts
│   │   ├── pages/          # Page components
│   │   ├── services/       # API services
│   │   └── ...
│   ├── public/
│   └── package.json
├── server/                 # Express backend
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── middleware/         # Custom middleware
│   ├── utils/              # Utility functions
│   └── package.json
├── .github/workflows/      # CI/CD pipelines
├── scripts/                # Deployment scripts
├── docker-compose.yml      # Docker configuration
└── README.md
```

## 🔧 Configuration

### Environment Variables

**Backend (.env)**
```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/mern-app
JWT_SECRET=your-super-secret-jwt-key
FRONTEND_URL=http://localhost:5173
LOG_LEVEL=info
```

**Frontend (.env)**
```env
VITE_API_URL=http://localhost:5000/api
```

### Production Configuration

For production deployment, update the environment variables:

**Backend (Production)**
```env
NODE_ENV=production
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/database
JWT_SECRET=your-production-jwt-secret
FRONTEND_URL=https://your-frontend-domain.com
```

**Frontend (Production)**
```env
VITE_API_URL=https://your-backend-domain.com/api
```

## 🚀 Deployment

### Backend Deployment (Render)

1. **Create a new Web Service on Render**
2. **Connect your GitHub repository**
3. **Configure build settings:**
   - Build Command: `cd server && npm install`
   - Start Command: `cd server && npm start`
4. **Set environment variables** in Render dashboard
5. **Deploy**

### Frontend Deployment (Netlify)

1. **Connect your GitHub repository to Netlify**
2. **Configure build settings:**
   - Base directory: `client`
   - Build command: `npm run build`
   - Publish directory: `client/dist`
3. **Set environment variables** in Netlify dashboard
4. **Deploy**

### Database Setup (MongoDB Atlas)

1. **Create a MongoDB Atlas cluster**
2. **Create a database user**
3. **Whitelist your application's IP addresses**
4. **Get the connection string**
5. **Update MONGODB_URI in your environment variables**

## 🔄 CI/CD Pipeline

The project includes GitHub Actions workflows for:

- **Continuous Integration**: Runs tests, linting, and builds on every push
- **Continuous Deployment**: Automatically deploys to production on main branch
- **Health Monitoring**: Regular health checks of deployed applications

### Setting up CI/CD

1. **Add secrets to your GitHub repository:**
   - `RENDER_SERVICE_ID` - Your Render service ID
   - `RENDER_API_KEY` - Your Render API key
   - `NETLIFY_AUTH_TOKEN` - Your Netlify auth token
   - `NETLIFY_SITE_ID` - Your Netlify site ID

2. **Push to main branch** to trigger deployment

## 📊 Monitoring

### Health Checks

The application includes health check endpoints:

- **Backend Health**: `GET /api/health`
- **Database Health**: `GET /api/health/db`

### Logging

- **Development**: Console logging with colors
- **Production**: File-based logging with rotation
- **Error Tracking**: Centralized error logging

### Performance Monitoring

- **Frontend**: Bundle analysis and performance metrics
- **Backend**: Request/response time monitoring
- **Database**: Connection pool monitoring

## 🧪 Testing

### Running Tests

```bash
# Run all tests
npm test

# Backend tests only
cd server && npm test

# Frontend tests only
cd client && npm test

# Watch mode
npm run test:watch
```

### Test Coverage

The project includes:
- Unit tests for API endpoints
- Component tests for React components
- Integration tests for user flows

## 🔐 Security

### Implemented Security Measures

- **Authentication**: JWT-based authentication
- **Authorization**: Route-level protection
- **Input Validation**: Mongoose schema validation
- **Rate Limiting**: API rate limiting
- **Security Headers**: Helmet.js security headers
- **CORS**: Configured CORS policy
- **Environment Variables**: Sensitive data protection

## 📈 Performance Optimization

### Frontend Optimizations

- **Code Splitting**: Automatic route-based splitting
- **Bundle Optimization**: Vite build optimizations
- **Caching**: Static asset caching
- **Compression**: Gzip compression

### Backend Optimizations

- **Database Indexing**: Optimized MongoDB queries
- **Connection Pooling**: MongoDB connection pooling
- **Compression**: Response compression
- **Caching**: Response caching strategies

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Troubleshooting

### Common Issues

**MongoDB Connection Issues**
```bash
# Check MongoDB status
sudo systemctl status mongod

# Restart MongoDB
sudo systemctl restart mongod
```

**Port Already in Use**
```bash
# Find process using port 5000
lsof -i :5000

# Kill process
kill -9 <PID>
```

**Build Failures**
```bash
# Clear npm cache
npm cache clean --force

# Delete node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

## 📞 Support

For support and questions:
- Create an issue in the GitHub repository
- Check the documentation
- Review the troubleshooting section

---

## 🎯 Assignment Completion Checklist

### ✅ Task 1: Application Preparation
- [x] React production build optimization
- [x] Code splitting implementation
- [x] Environment variable configuration
- [x] Express.js production setup
- [x] Security headers and error handling
- [x] Production logging implementation
- [x] MongoDB Atlas setup
- [x] Database connection pooling

### ✅ Task 2: Backend Deployment
- [x] Render deployment configuration
- [x] Environment variables setup
- [x] Continuous deployment from GitHub
- [x] HTTPS/SSL configuration
- [x] Server monitoring and logging

### ✅ Task 3: Frontend Deployment
- [x] Netlify deployment configuration
- [x] Build settings configuration
- [x] Environment variables setup
- [x] Continuous deployment from GitHub
- [x] HTTPS configuration
- [x] Static asset caching

### ✅ Task 4: CI/CD Pipeline
- [x] GitHub Actions workflows
- [x] Automated testing pipeline
- [x] Linting and code quality checks
- [x] Automated building
- [x] Continuous deployment setup
- [x] Staging and production environments
- [x] Rollback strategies

### ✅ Task 5: Monitoring and Maintenance
- [x] Health check endpoints
- [x] Uptime monitoring
- [x] Error tracking setup
- [x] Performance monitoring
- [x] Server resource monitoring
- [x] API performance tracking
- [x] Frontend performance monitoring
- [x] Maintenance documentation

## 🌐 Live Demo

- **Frontend**: [Your Netlify URL]
- **Backend API**: [Your Render URL]
- **API Documentation**: [Your Backend URL]/api/health

---

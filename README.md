# Anysite QR Generator

A powerful, full-stack web application for generating customizable QR codes for any website URL. Built with modern web technologies including React, Node.js, Express, and MongoDB.

![QR Code Generator](https://img.shields.io/badge/QR-Code_Generator-green) ![React](https://img.shields.io/badge/React-18.2.0-blue) ![Node.js](https://img.shields.io/badge/Node.js-Express-brightgreen) ![MongoDB](https://img.shields.io/badge/MongoDB-Database-green)

## 🌟 Features

- **QR Code Generation**: Create QR codes for any website URL
- **Customizable Design**: Adjust colors, size, and format of QR codes
- **User Authentication**: Secure signup/login system with JWT tokens
- **History Tracking**: Save and manage your previously generated QR codes
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Download Options**: Export QR codes in PNG, JPEG, or SVG formats
- **Social Sharing**: Easily share QR codes on social media platforms

## 🛠️ Technology Stack

### Frontend
- **React** 18.2.0 - User interface library
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client for API requests
- **QRCode.react** - QR code generation library
- **Bootstrap** - UI framework for responsive design
- **React-Icons** - Icon library

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variables management

### Deployment
- **Docker** - Containerization
- **GitHub Actions** - CI/CD pipeline
- **Render/Vercel** - Deployment platforms

## 📦 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance like MongoDB Atlas)
- Git

### 1. Clone the Repository
```bash
git clone https://github.com/Muhammad-Aamir1/Anysite-QR-generator.git
cd Anysite-QR-generator
```

### 2. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your configurations:
# MONGODB_URI=your_mongodb_connection_string
# JWT_SECRET=your_jwt_secret_key
# PORT=5000

# Start the development server
npm run dev
```

### 3. Frontend Setup
```bash
# Navigate to frontend directory (in a new terminal)
cd frontend

# Install dependencies
npm install

# Start the development server
npm start
```

### 4. Database Setup
- Create a MongoDB database (local installation or MongoDB Atlas)
- Update the `MONGODB_URI` in your backend `.env` file
- The server will automatically create the necessary collections

## 🚀 Usage

1. **Register/Login**: Create an account or login to access all features
2. **Generate QR Code**: Enter a URL and customize the QR code appearance
3. **Save QR Code**: Store your generated QR codes in your personal history
4. **Download/Share**: Export your QR code in various formats or share directly

## 🔧 Environment Variables

### Backend (.env)
```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
PORT=5000
CLIENT_URL=http://localhost:3000
NODE_ENV=development
```

### Frontend (.env)
```
REACT_APP_API_BASE_URL=http://localhost:5000/api
REACT_APP_APP_NAME=Anysite QR Generator
```

## 📁 Project Structure

```
Anysite-QR-generator/
├── backend/
│   ├── controllers/     # Route controllers
│   ├── models/          # MongoDB models
│   ├── routes/          # API routes
│   ├── middleware/      # Custom middleware
│   ├── utils/           # Utility functions
│   ├── config/          # Database configuration
│   └── server.js        # Server entry point
├── frontend/
│   ├── public/          # Static files
│   ├── src/
│   │   ├── components/  # Reusable components
│   │   ├── pages/       # Page components
│   │   ├── context/     # React context
│   │   ├── hooks/       # Custom hooks
│   │   ├── services/    # API services
│   │   └── styles/      # CSS files
│   └── package.json
├── docker-compose.yml   # Docker compose configuration
├── Dockerfile           # Backend Dockerfile
└── README.md
```

## 🐳 Docker Deployment

### Using Docker Compose
```bash
# Start all services
docker-compose up -d

# Stop services
docker-compose down
```

### Individual Containers
```bash
# Build and run backend
cd backend
docker build -t qr-backend .
docker run -p 5000:5000 qr-backend

# Build and run frontend
cd frontend
docker build -t qr-frontend .
docker run -p 3000:3000 qr-frontend
```

## 📊 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user (protected)

### QR Codes
- `POST /api/qr/generate` - Generate a new QR code (protected)
- `GET /api/qr/history` - Get user's QR code history (protected)
- `DELETE /api/qr/:id` - Delete a QR code (protected)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

Muhammad Aamir - [GitHub](https://github.com/Muhammad-Aamir1)

## 🙏 Acknowledgments

- QR code generation using [qrcode.react](https://www.npmjs.com/package/qrcode.react)
- Icons from [React Icons](https://react-icons.github.io/react-icons/)
- UI components from [Bootstrap](https://getbootstrap.com/)

## 📞 Support

If you have any questions or issues, please open an issue on the GitHub repository or contact the maintainer.

---

⭐ Star this repository if you found it helpful!

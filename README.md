# ConnectCamp 🏕️

ConnectCamp is a comprehensive camping and outdoor adventure platform that connects camping enthusiasts with campsites, gear, knowledge, and community.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)

## ✨ Features

### Core Features
- **🏕️ Campsite Discovery & Booking** - Search, filter, and book campsites with real-time availability
- **🎒 Trip Planning** - Create itineraries, manage packing lists, and budget estimation
- **📚 Camping Academy** - Educational content, expert videos, and certification programs
- **🛒 Gear Marketplace** - Buy, rent, and review camping equipment
- **👥 Community Hub** - Connect with fellow campers, share stories, and get help
- **🚨 Safety & Compliance** - Emergency check-ins, safety alerts, and environmental regulations
- **🚗 Transportation** - Integrated route planning and transport options
- **🎉 Events** - Discover and join camping events and gatherings

### User Roles
- **Campers** - Regular users booking sites and planning trips
- **Providers** - Campsite owners managing bookings and availability
- **Gear Vendors** - Sellers managing inventory and deliveries
- **Experts** - Content creators sharing knowledge and certifications
- **Admins** - Platform management and moderation

## 🛠️ Tech Stack

### Frontend (Angular)
- **Framework**: Angular 21.1.4
- **UI Library**: Tailwind CSS 3.4.19
- **Icons**: Lucide Angular
- **State Management**: RxJS
- **Routing**: Angular Router
- **HTTP Client**: Angular HttpClient

### Backend (Spring Boot)
- **Framework**: Spring Boot 3.2.3
- **Language**: Java 17
- **Database**: MongoDB
- **Security**: Spring Security + JWT
- **Build Tool**: Maven

## 📁 Project Structure

```
ConnectCamp/
├── angular-campconnect/          # Frontend Angular application
│   ├── src/
│   │   ├── app/
│   │   │   ├── core/            # Core services, guards, interceptors
│   │   │   ├── features/        # Feature modules
│   │   │   │   ├── auth/        # Authentication
│   │   │   │   ├── bookings/    # Booking management
│   │   │   │   ├── trips/       # Trip planning
│   │   │   │   ├── academy/     # Learning platform
│   │   │   │   ├── gear/        # Gear marketplace
│   │   │   │   ├── community/   # Social features
│   │   │   │   ├── safety/      # Safety features
│   │   │   │   └── ...          # Other features
│   │   │   └── shared/          # Shared components & utilities
│   │   ├── public/              # Static assets
│   │   └── styles/              # Global styles
│   ├── angular.json
│   ├── tailwind.config.js
│   └── package.json
│
└── backend/                      # Backend Spring Boot application
    ├── src/
    │   └── main/
    │       ├── java/
    │       │   └── com/campconnect/
    │       │       ├── config/
    │       │       ├── controller/
    │       │       ├── model/
    │       │       ├── repository/
    │       │       └── service/
    │       └── resources/
    │           └── application.properties
    └── pom.xml
```

## 📦 Prerequisites

### Frontend
- **Node.js**: 18.x or higher
- **npm**: 9.x or higher
- **Angular CLI**: 21.x or higher

### Backend
- **Java**: JDK 17 or higher
- **Maven**: 3.8 or higher
- **MongoDB**: 6.0 or higher

## 🚀 Installation

### Clone the Repository
```bash
git clone https://github.com/yourusername/ConnectCamp.git
cd ConnectCamp
```

### Frontend Setup
```bash
cd angular-campconnect
npm install
```

### Backend Setup
```bash
cd backend
mvn clean install
```

## 🏃 Running the Application

### Start MongoDB
Ensure MongoDB is running on your local machine:
```bash
mongod
```

### Run Backend
```bash
cd backend
mvn spring-boot:run
```
The backend API will be available at `http://localhost:8080`

### Run Frontend
```bash
cd angular-campconnect
npm start
```
The frontend will be available at `http://localhost:4200`

## ⚙️ Configuration

### Frontend Configuration
Edit `angular-campconnect/src/environments/environment.ts`:
```typescript
export const environment = {
  production: false,
  apiUrl: 'http://localhost:8080/api'
};
```

### Backend Configuration
Edit `backend/src/main/resources/application.properties`:
```properties
# MongoDB Configuration
spring.data.mongodb.uri=mongodb://localhost:27017/campconnect

# JWT Configuration
jwt.secret=your-secret-key
jwt.expiration=86400000

# Server Configuration
server.port=8080
```

## 📚 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/me` - Get current user

### Campsite Endpoints
- `GET /api/campsites` - List all campsites
- `GET /api/campsites/:id` - Get campsite details
- `POST /api/campsites` - Create campsite (Provider)
- `PUT /api/campsites/:id` - Update campsite (Provider)
- `DELETE /api/campsites/:id` - Delete campsite (Provider)

### Booking Endpoints
- `POST /api/bookings` - Create booking
- `GET /api/bookings` - Get user bookings
- `GET /api/bookings/:id` - Get booking details
- `PUT /api/bookings/:id/cancel` - Cancel booking

*(More endpoints documentation coming soon)*

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Coding Standards
- Follow Angular style guide for frontend
- Follow Java coding conventions for backend
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

## 👥 Authors

- Your Name - Initial work

## 🙏 Acknowledgments

- Thanks to all contributors
- Inspired by the camping community
- Built with modern web technologies


---

**Happy Camping! 🏕️**

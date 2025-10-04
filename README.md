# Enhanced Railway Booking Platform

A modern, full-stack railway booking platform with AI-powered features, integrated services, and accessibility-focused design.

## Features

### Core Features
- 🎫 **Smart Ticket Booking** - Intuitive booking system with multiple class options
- 🎤 **AI Voice Assistant** - Multi-language voice booking for accessibility
- 🗺️ **Seat Finder Navigation** - Turn-by-turn navigation to your exact seat
- 🚗 **Integrated Cab Booking** - Door-to-door service with Uber/Ola integration
- 👨‍💼 **Verified Porter Service** - Government-registered porters at fixed rates
- 🍽️ **Train Kitchen Hub** - Food ordering with veg/non-veg options
- 🏆 **Cleanliness Rewards** - AI-verified cleanliness rewards system

### Technical Features
- ⚡ **Modern React Frontend** - Beautiful, responsive UI with animations
- 🔐 **Secure Authentication** - JWT-based auth with MongoDB
- 🎨 **Engaging Animations** - Train loading animations and smooth transitions
- 📱 **Mobile Responsive** - Optimized for all device sizes
- 🔊 **Voice Recognition** - Web Speech API integration
- 💳 **Payment Integration** - Multiple payment options

## Tech Stack

### Frontend
- React 18
- React Router
- Framer Motion (animations)
- Styled Components
- Axios
- React Query

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- Redis (caching)
- JWT Authentication
- bcrypt (password hashing)

### External Integrations
- Google Maps API
- Web Speech API
- Payment Gateways (Razorpay/Stripe)
- Cab Service APIs (Uber/Ola)

## Project Structure

```
enhanced-railway-booking-platform/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── services/
│   ├── utils/
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
│   │   └── App.js
│   └── package.json
├── package.json
└── README.md
```

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB
- Redis (optional, for caching)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd enhanced-railway-booking-platform
   ```

2. **Install all dependencies**
   ```bash
   npm run install-all
   ```

3. **Set up environment variables**
   ```bash
   cd backend
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start the development servers**
   ```bash
   npm run dev
   ```

This will start:
- Backend API on http://localhost:5000
- Frontend React app on http://localhost:3000

### Individual Commands

**Backend only:**
```bash
cd backend
npm run dev
```

**Frontend only:**
```bash
cd frontend
npm start
```

**Build for production:**
```bash
npm run build
```

## Environment Variables

Create a `.env` file in the backend directory with the following variables:

```env
# Server Configuration
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/railway_booking_platform
REDIS_URL=redis://localhost:6379

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_here
JWT_EXPIRE=7d

# External API Keys
GOOGLE_MAPS_API_KEY=your_google_maps_api_key
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Voice Recognition API
SPEECH_API_KEY=your_speech_api_key

# Cab Service APIs
UBER_API_KEY=your_uber_api_key
OLA_API_KEY=your_ola_api_key
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile
- `PUT /api/auth/profile` - Update user profile

### Booking
- `GET /api/trains/search` - Search trains
- `POST /api/bookings/create` - Create booking
- `GET /api/bookings/user/:userId` - Get user bookings
- `GET /api/bookings/:bookingId` - Get booking details

### Features
- `POST /api/voice/process` - Process voice commands
- `GET /api/maps/navigation` - Get navigation data
- `POST /api/cab/book` - Book cab service
- `GET /api/porter/available` - Get available porters
- `GET /api/food/menu` - Get food menu
- `POST /api/cleanliness/verify` - Verify cleanliness

### Payment
- `POST /api/payment/initiate` - Initiate payment
- `POST /api/payment/verify` - Verify payment
- `GET /api/payment/status/:paymentId` - Get payment status

## Development Guidelines

### Code Style
- Use functional components with hooks
- Follow React best practices
- Use meaningful variable and function names
- Add comments for complex logic
- Maintain consistent indentation

### Git Workflow
- Create feature branches for new features
- Write descriptive commit messages
- Test before committing
- Keep commits focused and atomic

### Testing
- Write unit tests for components
- Test API endpoints
- Ensure responsive design works
- Test accessibility features

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions, please open an issue in the repository or contact the development team.

---

Built with ❤️ for modern railway travel experiences
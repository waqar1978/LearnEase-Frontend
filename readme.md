# LearnEase - Frontend

![Logo](https://i.ibb.co/ngwjLL5/Unsastitled-2.png)

## Overview

LearnEase is an innovative virtual classroom application that transforms online education through interactive video conferencing and collaborative learning tools. Built with modern web technologies, it provides a comprehensive platform for educators and students to engage in real-time learning experiences with features like live video calls, interactive whiteboards, document sharing, and activity management.

The application offers a seamless user experience with responsive design, supporting both desktop and mobile devices. With secure authentication and personalized themes, LearnEase creates an engaging and protected virtual learning environment.

## Features

### Core Functionality
- **Group Video Conferencing**: Real-time video and audio communication for virtual classrooms
- **Interactive Whiteboard**: Collaborative drawing and annotation tools for dynamic lessons
- **Screen Sharing**: Share presentations, documents, and multimedia content seamlessly
- **Live Chat**: Real-time messaging system for interactive discussions and Q&A
- **Document Sharing**: Upload, share, and access study materials and resources
- **Teaching Activities**: Create and manage interactive learning activities and assignments
- **Grade Management**: Track and manage student progress and performance
- **Participant Management**: View and manage classroom participants with role-based access

### User Experience
- **JWT Authentication**: Secure user authentication and authorization
- **Email Verification**: Account verification system for enhanced security
- **Light/Dark Mode**: Customizable theme preferences for comfortable viewing
- **Responsive Design**: Optimized layouts for both large screens and mobile devices
- **Protected Routes**: Secure access control for authenticated users only

## Tech Stack

### Frontend Framework
- **React 18.2.0**: Modern UI library with hooks and functional components
- **Vite**: Fast build tool and development server
- **React Router DOM 6.12.1**: Client-side routing and navigation

### State Management
- **Redux Toolkit 1.9.5**: Efficient state management with modern Redux patterns
- **React Redux 8.1.0**: React bindings for Redux
- **Redux Persist 6.0.0**: State persistence across sessions

### UI Libraries & Styling
- **Material-UI (MUI) 5.14.0**: Comprehensive React component library
- **Ant Design 5.6.2**: Enterprise-class UI design system
- **Tailwind CSS 3.3.2**: Utility-first CSS framework
- **Emotion**: CSS-in-JS styling solution
- **React Icons 4.9.0**: Popular icon library

### Real-time Communication
- **WebSocket (ws 8.13.0)**: Real-time bidirectional communication
- **React Use WebSocket 4.3.1**: WebSocket hooks for React

### Media & File Handling
- **React Player 2.12.0**: Video and audio player component
- **React Media Recorder 1.6.6**: Media recording capabilities
- **js-file-download 0.4.12**: File download utility
- **Axios 1.4.0**: HTTP client for API requests

### Additional Libraries
- **React Tooltip 5.14.0**: Accessible tooltip components
- **React Loading Skeleton 3.3.1**: Loading state placeholders
- **React Toggle Dark Mode 1.1.1**: Theme switching component
- **classnames 2.3.2**: Conditional CSS class utility

### Development Tools
- **ESLint**: Code linting and quality assurance
- **PostCSS & Autoprefixer**: CSS processing and browser compatibility

## Project Structure

```
LearnEase-Client/
├── public/                          # Static assets
│   ├── icons/                       # App icons and favicons
│   └── manifest.json                # PWA manifest
│
├── src/
│   ├── assets/                      # Images and media files
│   │   ├── banner-images/           # Page banners
│   │   ├── loading-images/          # Loading animations
│   │   └── logo/                    # Brand logos
│   │
│   ├── components/                  # React components
│   │   ├── BannerPage/              # Banner component
│   │   ├── HomeOutside/             # Landing page wrapper
│   │   ├── LoginForm/               # Login form component
│   │   ├── SignupForm/              # Registration form
│   │   │
│   │   ├── LandingPage/             # Home page components
│   │   │   ├── CreateRoomModal/     # Room creation modal
│   │   │   └── HomeBody/            # Landing page content
│   │   │
│   │   ├── RoomPage/                # Virtual classroom components
│   │   │   ├── GeneralComponents/   # Shared room components
│   │   │   ├── MainComponents/      # Primary features
│   │   │   │   ├── VideoCallsPage/  # Video conferencing
│   │   │   │   ├── WhiteboardPage/  # Interactive whiteboard
│   │   │   │   ├── TopicsPage/      # Topics management
│   │   │   │   └── GradesPage/      # Grade tracking
│   │   │   │
│   │   │   ├── SecondaryComponents/ # Supporting features
│   │   │   │   ├── Activities/      # Activity management
│   │   │   │   ├── DocumentsList/   # Document sharing
│   │   │   │   ├── Messages/        # Chat functionality
│   │   │   │   └── ParticipantsList/ # User management
│   │   │   │
│   │   │   ├── LargeScreen/         # Desktop layout
│   │   │   ├── SmallScreen/         # Mobile layout
│   │   │   └── RoomBody/            # Room container
│   │   │
│   │   └── UtilityComponents/       # Reusable utilities
│   │       ├── InputFields/         # Form inputs
│   │       ├── LazyImage/           # Lazy-loaded images
│   │       └── ProtectedRoute/      # Route guards
│   │
│   ├── pages/                       # Page-level components
│   ├── App.jsx                      # Root application component
│   └── main.jsx                     # Application entry point
│
├── .eslintrc.cjs                    # ESLint configuration
├── postcss.config.js                # PostCSS configuration
├── tailwind.config.js               # Tailwind CSS configuration
├── vite.config.js                   # Vite build configuration
├── Dockerfile                       # Docker containerization
└── package.json                     # Project dependencies

```

## Installation and Setup

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn package manager

### Installation Steps

1. **Clone the Repository**
```bash
git clone https://github.com/shahsad-kp/LearnEase-Client.git
cd LearnEase-Client
```

2. **Install Dependencies**
```bash
npm install
```

3. **Configure Environment Variables**

Create a `.env` file in the root directory with the following variables:

```env
VITE_BACKEND_URL=your_backend_api_url
VITE_WEBSOCKET_URL=your_websocket_server_url
```

4. **Start Development Server**
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build production-ready application
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint for code quality checks

## Deployment

### Frontend Deployment
Build the production version of the application:

```bash
npm run build
```

The optimized files will be generated in the `dist/` directory, ready for deployment to any static hosting service.

### Backend Setup
This frontend application requires a backend server to function properly. For backend setup and deployment instructions, refer to:

[LearnEase Backend Repository](https://github.com/shahsad-kp/LearnEase-Server)

### Docker Deployment
A Dockerfile is included for containerized deployment:

```bash
docker build -t learnease-frontend .
docker run -p 5173:5173 learnease-frontend
```

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_BACKEND_URL` | Backend API server URL | Yes |
| `VITE_WEBSOCKET_URL` | WebSocket server URL for real-time features | Yes |

## Browser Support

LearnEase supports all modern browsers:
- Chrome (recommended)
- Firefox
- Safari
- Edge

For optimal video conferencing experience, use the latest version of Chrome or Firefox.

## License

This project is private and proprietary.

## Support

If you find this project helpful, please consider giving it a ⭐ on GitHub!

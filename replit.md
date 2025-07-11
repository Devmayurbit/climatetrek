# ClimaTrack - Carbon Footprint Tracking Application

## Overview

ClimaTrack is a web application designed to help users track their carbon footprint through daily activities. The application features AR-based carbon visualization, AI-powered carbon estimation, user activity logging, and a gamified experience with eco-scores and leaderboards.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a modern full-stack architecture with clear separation between frontend and backend concerns:

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with custom styling

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **API**: RESTful API with JSON responses
- **Authentication**: Mock authentication system (user ID hardcoded to 1)

## Key Components

### Database Schema
The application uses three main tables:
- **users**: User profiles with eco-scores and badges
- **activities**: Carbon footprint activities with AI-estimated impact
- **achievements**: User achievements and rewards

### Core Features
- **Activity Logging**: Users can log various activities (food, transport, energy, home, shopping)
- **AI Carbon Estimation**: OpenAI integration for intelligent carbon footprint calculations
- **AR Visualization**: Simulated AR experience showing environmental impact
- **Leaderboard System**: Competitive ranking based on eco-scores
- **Rewards System**: Badges and achievements for sustainable behavior

### Frontend Components
- **Activity Form**: Form for logging new activities with real-time validation
- **AR Visualization**: Mock AR interface showing carbon impact visualizations
- **Stats Dashboard**: Overview of user's carbon footprint metrics
- **Leaderboard Table**: Competitive ranking display
- **Rewards Card**: Achievement and badge system

## Data Flow

1. **Activity Logging**: User submits activity → Frontend validates → Backend processes with AI estimation → Database stores → UI updates
2. **Carbon Calculation**: Activity data → OpenAI API → Carbon estimate + points → Database storage
3. **Statistics**: Database queries → Aggregated carbon data → Dashboard display
4. **Leaderboard**: User scores → Ranking calculation → Competitive display

## External Dependencies

### Third-Party Services
- **OpenAI API**: For intelligent carbon footprint estimation
- **Neon Database**: Serverless PostgreSQL hosting

### Key Libraries
- **Frontend**: React, Vite, Tailwind CSS, Radix UI, TanStack Query, Wouter
- **Backend**: Express.js, Drizzle ORM, OpenAI SDK
- **Database**: PostgreSQL with Drizzle migrations
- **UI Components**: Complete shadcn/ui component library

## Deployment Strategy

### Development
- **Frontend**: Vite development server with HMR
- **Backend**: Node.js with tsx for TypeScript execution
- **Database**: Neon Database with connection pooling

### Production Build
- **Frontend**: Vite build to static assets
- **Backend**: esbuild bundle for optimized server code
- **Database**: Drizzle migrations for schema management

### Environment Configuration
- Database connection via `DATABASE_URL` environment variable
- OpenAI API key via `OPENAI_API_KEY` environment variable
- Production/development mode via `NODE_ENV`

The application is structured for easy deployment to platforms like Replit, Vercel, or traditional hosting with minimal configuration changes.
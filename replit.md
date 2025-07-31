# BoltLanding - Landing Page Builder

## Overview

BoltLanding is a full-stack web application for creating and managing landing pages. The project uses a modern tech stack with React on the frontend, Express.js on the backend, and PostgreSQL with Drizzle ORM for data persistence. The application features a complete landing page showcase with navigation, hero, stats, features, testimonials, pricing, FAQ, CTA, and footer sections, plus full database integration for user management, landing page creation, and analytics tracking.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: Wouter for lightweight client-side routing
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens and dark mode support
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints with `/api` prefix
- **Error Handling**: Centralized error middleware with status code mapping
- **Development**: Hot reload with Vite SSR integration

### Data Layer
- **Database**: PostgreSQL (Neon Database) with full database integration
- **ORM**: Drizzle ORM with schema-first approach and explicit relations
- **Migrations**: Drizzle Kit for database schema management
- **Storage Interface**: DatabaseStorage implementation with comprehensive CRUD operations
- **Tables**: Users, Landing Pages, and Page Analytics with proper relationships

## Key Components

### Frontend Components
- **Landing Page Sections**: Modular components for hero, features, testimonials, pricing, FAQ, and CTA sections
- **UI Components**: Comprehensive shadcn/ui component library including buttons, cards, forms, dialogs, and navigation
- **Responsive Design**: Mobile-first approach with breakpoint-based layouts
- **Theme System**: CSS custom properties for consistent theming

### Backend Components
- **Server Setup**: Express application with JSON parsing and URL encoding
- **Route Registration**: Modular route system with HTTP server creation
- **Storage Layer**: Interface-based storage with pluggable implementations
- **Request Logging**: Comprehensive logging for API requests with timing and response data

### Development Tools
- **Vite Integration**: Custom Vite setup for SSR and hot module replacement
- **TypeScript Configuration**: Strict type checking with path aliases
- **Error Overlays**: Runtime error display for development
- **Build Process**: Separate client and server build pipelines

## Data Flow

### Client-Server Communication
1. **API Requests**: Frontend uses fetch with credentials for authenticated requests
2. **Query Management**: TanStack Query handles caching, background refetching, and error states
3. **Error Handling**: Unified error handling with toast notifications
4. **Response Processing**: JSON responses with status code validation

### Database Operations
1. **Schema Definition**: Drizzle schema defines table structures and relationships
2. **Type Safety**: Auto-generated TypeScript types from schema
3. **CRUD Operations**: Storage interface abstracts database operations
4. **Migration Management**: Version-controlled schema changes

## External Dependencies

### Production Dependencies
- **UI Framework**: React ecosystem with Radix UI primitives
- **Database**: Neon Database serverless PostgreSQL
- **Form Handling**: React Hook Form with Hookform resolvers
- **Date Handling**: date-fns for date manipulation
- **Styling**: Tailwind CSS with utility classes
- **State Management**: TanStack Query for server state

### Development Dependencies
- **Build Tools**: Vite with TypeScript support
- **Code Quality**: ESBuild for production builds
- **Database Tools**: Drizzle Kit for migrations and introspection

## Deployment Strategy

### Build Process
1. **Client Build**: Vite builds React application to `dist/public`
2. **Server Build**: ESBuild bundles Express server to `dist/index.js`
3. **Asset Optimization**: Vite handles code splitting and asset optimization
4. **Type Checking**: TypeScript compilation verification

### Environment Configuration
- **Database**: PostgreSQL connection via `DATABASE_URL` environment variable
- **Development**: Hot reload with Vite middleware integration
- **Production**: Static file serving with Express

### Deployment Considerations
- **Database Migrations**: Manual migration execution with `db:push` command
- **Environment Variables**: Database URL required for production
- **Static Assets**: Public directory served by Express in production
- **Process Management**: Single Node.js process handling both API and static files

The application follows a monorepo structure with clear separation between client, server, and shared code, making it maintainable and scalable for landing page creation and management features.
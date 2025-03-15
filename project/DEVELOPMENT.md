# Development Guide

## Project Overview
This is a web application built with Next.js, React, Node.js, and Nest.js. The project uses PostgreSQL via Supabase for the database, with frontend deployment on Vercel and backend on DigitalOcean.

## Tech Stack
- Frontend: Next.js & React
- Backend: Node.js & Nest.js
- Database: PostgreSQL (Supabase)
- Deployment: Vercel (Frontend), DigitalOcean (Backend)

## Development Setup

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Git

### Environment Setup
1. Clone the repository
2. Install dependencies: `npm install`
3. Configure environment variables:
   ```env
   # Supabase
   SUPABASE_URL=your_supabase_url
   SUPABASE_ANON_KEY=your_supabase_anon_key
   
   # API
   NEXT_PUBLIC_API_URL=your_api_url
   ```

### Development Workflow
1. Start the development server:
   ```bash
   npm run dev
   ```
2. Follow the Git workflow:
   - Create feature branches from `main`
   - Use conventional commits
   - Submit PRs for review

### Database Management
- All database changes should be made through Supabase migrations
- Test queries locally before deploying
- Follow the schema design in documentation

### Deployment Process
1. Frontend (Vercel):
   - Automatic deployments from main branch
   - Preview deployments for PRs

2. Backend (DigitalOcean):
   - CI/CD pipeline handles deployments
   - Staging environment for testing

### Testing
- Write unit tests for new features
- Run integration tests before deployment
- Ensure mobile responsiveness
- Cross-browser testing

### Performance Optimization
- Use React.memo for expensive components
- Implement proper caching strategies
- Optimize API calls and database queries
- Monitor application performance

## Documentation
- API endpoints are documented in `/api-docs`
- Component documentation in respective component files
- Database schema in `/db/schema.md`

## Support
For questions or issues:
1. Check existing documentation
2. Consult with team members
3. Create detailed issue reports

## Best Practices
- Follow ESLint and Prettier configurations
- Write clean, maintainable code
- Document complex logic
- Review PR feedback promptly
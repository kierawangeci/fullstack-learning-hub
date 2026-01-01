# Complete Affiliate Platform Structure

## Full Directory Structure with File Examples
affiliate-platform/
├── .vscode/
│ ├── settings.json # VS Code workspace settings
│ ├── extensions.json # Recommended extensions
│ └── launch.json # Debug configurations
├── .github/
│ └── workflows/
│ ├── ci.yml # Continuous Integration
│ └── cd.yml # Continuous Deployment
├── docker/
│ ├── nginx/
│ │ └── nginx.conf # Nginx configuration
│ ├── postgres/
│ │ └── init.sql # Database initialization
│ ├── redis/
│ │ └── redis.conf # Redis configuration
│ └── docker-compose.yml # Multi-container setup
├── docs/
│ ├── api/
│ │ ├── endpoints.md # API documentation
│ │ └── webhooks.md # Webhook specifications
│ ├── deployment/
│ │ ├── production.md # Production deployment guide
│ │ └── staging.md # Staging environment setup
│ └── architecture.md # System architecture
├── frontend/ # Next.js 14 Application
│ ├── public/
│ │ ├── images/
│ │ │ ├── logo.svg
│ │ │ └── favicon.ico
│ │ ├── videos/
│ │ │ └── intro.mp4
│ │ └── robots.txt
│ ├── src/
│ │ ├── app/ # App Router (Next.js 14)
│ │ │ ├── (auth)/ # Route group for authentication
│ │ │ │ ├── login/
│ │ │ │ │ └── page.tsx
│ │ │ │ └── register/
│ │ │ │ └── page.tsx
│ │ │ ├── dashboard/
│ │ │ │ ├── page.tsx
│ │ │ │ └── layout.tsx
│ │ │ ├── earn/
│ │ │ │ ├── videos/
│ │ │ │ │ └── page.tsx
│ │ │ │ ├── offers/
│ │ │ │ │ └── page.tsx
│ │ │ │ └── surveys/
│ │ │ │ └── page.tsx
│ │ │ ├── blog/
│ │ │ │ ├── page.tsx
│ │ │ │ └── [slug]/
│ │ │ │ └── page.tsx
│ │ │ ├── api/ # Next.js API routes
│ │ │ │ └── webhooks/
│ │ │ │ └── stripe/
│ │ │ │ └── route.ts
│ │ │ ├── layout.tsx # Root layout
│ │ │ └── page.tsx # Home page
│ │ ├── components/
│ │ │ ├── ui/ # Reusable UI components
│ │ │ │ ├── Button/
│ │ │ │ │ ├── Button.tsx
│ │ │ │ │ ├── Button.test.tsx
│ │ │ │ │ ├── Button.stories.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ ├── Card/
│ │ │ │ │ ├── Card.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ ├── Modal/
│ │ │ │ │ ├── Modal.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ └── Table/
│ │ │ │ ├── Table.tsx
│ │ │ │ └── index.ts
│ │ │ ├── layout/ # Layout components
│ │ │ │ ├── Header/
│ │ │ │ │ ├── Header.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ ├── Sidebar/
│ │ │ │ │ ├── Sidebar.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ └── Footer/
│ │ │ │ ├── Footer.tsx
│ │ │ │ └── index.ts
│ │ │ ├── dashboard/ # Dashboard specific components
│ │ │ │ ├── StatsCard/
│ │ │ │ │ ├── StatsCard.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ ├── EarningsChart/
│ │ │ │ │ ├── EarningsChart.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ └── ReferralTable/
│ │ │ │ ├── ReferralTable.tsx
│ │ │ │ └── index.ts
│ │ │ ├── earn/ # Earning components
│ │ │ │ ├── VideoPlayer/
│ │ │ │ │ ├── VideoPlayer.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ ├── OfferCard/
│ │ │ │ │ ├── OfferCard.tsx
│ │ │ │ │ └── index.ts
│ │ │ │ └── SurveyWidget/
│ │ │ │ ├── SurveyWidget.tsx
│ │ │ │ └── index.ts
│ │ │ └── shared/ # Shared components
│ │ │ ├── LoadingSpinner/
│ │ │ │ ├── LoadingSpinner.tsx
│ │ │ │ └── index.ts
│ │ │ ├── ErrorBoundary/
│ │ │ │ ├── ErrorBoundary.tsx
│ │ │ │ └── index.ts
│ │ │ └── Toast/
│ │ │ ├── Toast.tsx
│ │ │ └── index.ts
│ │ ├── hooks/ # Custom React hooks
│ │ │ ├── useAuth.ts
│ │ │ ├── useEarnings.ts
│ │ │ ├── useMpesa.ts
│ │ │ └── useReferrals.ts
│ │ ├── lib/ # Utility libraries
│ │ │ ├── api/ # API clients
│ │ │ │ ├── axios.ts
│ │ │ │ ├── mpesa.ts
│ │ │ │ └── youtube.ts
│ │ │ ├── utils/ # Helper functions
│ │ │ │ ├── formatCurrency.ts
│ │ │ │ ├── validation.ts
│ │ │ │ └── dateFormatter.ts
│ │ │ ├── constants/ # Constants
│ │ │ │ ├── routes.ts
│ │ │ │ ├── earningRates.ts
│ │ │ │ └── config.ts
│ │ │ └── providers/ # Context providers
│ │ │ ├── AuthProvider.tsx
│ │ │ ├── ThemeProvider.tsx
│ │ │ └── EarningsProvider.tsx
│ │ ├── styles/ # Global styles
│ │ │ ├── globals.css
│ │ │ ├── tailwind.css
│ │ │ └── theme.css
│ │ ├── types/ # TypeScript types
│ │ │ ├── user.ts
│ │ │ ├── earning.ts
│ │ │ └── api.ts
│ │ └── store/ # State management
│ │ ├── slices/
│ │ │ ├── authSlice.ts
│ │ │ └── earningsSlice.ts
│ │ └── index.ts
│ ├── .env.local # Frontend environment variables
│ ├── next.config.js # Next.js configuration
│ ├── tailwind.config.js # Tailwind CSS configuration
│ ├── tsconfig.json # TypeScript configuration
│ ├── eslint.config.js # ESLint configuration
│ └── package.json # Dependencies and scripts
├── backend/ # Node.js/Express Backend
│ ├── src/
│ │ ├── api/ # API endpoints
│ │ │ ├── v1/ # API version 1
│ │ │ │ ├── auth/
│ │ │ │ │ ├── controller.ts
│ │ │ │ │ ├── routes.ts
│ │ │ │ │ └── middleware.ts
│ │ │ │ ├── earnings/
│ │ │ │ │ ├── controller.ts
│ │ │ │ │ └── routes.ts
│ │ │ │ ├── payments/
│ │ │ │ │ ├── controller.ts
│ │ │ │ │ └── routes.ts
│ │ │ │ ├── referrals/
│ │ │ │ │ ├── controller.ts
│ │ │ │ │ └── routes.ts
│ │ │ │ ├── videos/
│ │ │ │ │ ├── controller.ts
│ │ │ │ │ └── routes.ts
│ │ │ │ └── admin/
│ │ │ │ ├── controller.ts
│ │ │ │ └── routes.ts
│ │ │ └── webhooks/ # Webhook endpoints
│ │ │ ├── mpesa.ts
│ │ │ └── youtube.ts
│ │ ├── config/ # Configuration files
│ │ │ ├── database.ts
│ │ │ ├── redis.ts
│ │ │ └── mpesa.ts
│ │ ├── controllers/ # Business logic controllers
│ │ │ ├── AuthController.ts
│ │ │ ├── EarningsController.ts
│ │ │ └── MpesaController.ts
│ │ ├── models/ # Database models
│ │ │ ├── User.ts
│ │ │ ├── Earning.ts
│ │ │ ├── Withdrawal.ts
│ │ │ └── Referral.ts
│ │ ├── services/ # Business services
│ │ │ ├── AuthService.ts
│ │ │ ├── PaymentService.ts
│ │ │ ├── MpesaService.ts
│ │ │ ├── YouTubeService.ts
│ │ │ └── AnalyticsService.ts
│ │ ├── middleware/ # Express middleware
│ │ │ ├── auth.ts
│ │ │ ├── validation.ts
│ │ │ ├── rateLimit.ts
│ │ │ └── errorHandler.ts
│ │ ├── utils/ # Utility functions
│ │ │ ├── logger.ts
│ │ │ ├── validators.ts
│ │ │ ├── encryption.ts
│ │


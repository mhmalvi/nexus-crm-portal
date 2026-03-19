# Nexus CRM Portal

A general-purpose frontend portal for the **Nexus CRM** microservices platform. This React application provides a streamlined interface for CRM operations, client-facing dashboards, and subscription management with PayPal and Stripe payment support.

## Features

- **Interactive Dashboard** — Visual overview of leads, campaigns, and key performance indicators
- **Lead Management** — Browse, filter, and manage leads with detailed status tracking and communication logs
- **Campaign Management** — Monitor campaign performance and lead attribution
- **Payment Integration** — Dual payment gateway support with Stripe and PayPal
- **Subscription Management** — Package selection, subscription lifecycle, and billing history
- **Requisition System** — Submit and track internal requisitions
- **Real-time Messaging** — Live chat and communication via WebSocket integration
- **Notifications** — In-app notification center for alerts and updates
- **Landing Page Module** — Built-in marketing and onboarding pages
- **Data Export** — Download reports in CSV format with screenshot capture capabilities
- **Animated UI** — Lottie-based animations for enhanced user experience

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | React 18 |
| State Management | Redux Toolkit |
| UI Library | Ant Design 4 |
| Styling | Tailwind CSS 3 |
| HTTP Client | Axios |
| Charts | Recharts |
| Payments | Stripe.js, PayPal React SDK |
| Real-time | Socket.IO Client |
| Carousel | React Slick |
| PDF Generation | jsPDF + html2canvas |
| Routing | React Router 6 |

## Prerequisites

- Node.js >= 16
- npm or Yarn

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/mhmalvi/nexus-crm-portal.git
   cd nexus-crm-portal
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure environment variables**

   ```bash
   cp .env.example .env.development.local
   ```

   Update the `.env.development.local` file with the required API URLs and payment gateway keys.

4. **Start the development server**

   ```bash
   npm start
   ```

   The application will be available at `http://localhost:3000`.

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start local development server |
| `npm run start-prod` | Start with production environment |
| `npm run build-local` | Build for local/staging deployment |
| `npm run build-prod` | Build for production deployment |
| `npm test` | Run the test suite |

## Project Structure

```
src/
├── Components/       # Reusable UI components
├── Pages/            # Route-level page components
│   ├── Authentication/
│   ├── Campaigns/
│   ├── Dashborad/
│   ├── LandingPage/
│   ├── LeadDetails/
│   ├── Messages/
│   ├── Notifications/
│   ├── Overview/
│   ├── Payments/
│   ├── Requisition/
│   ├── Settings/
│   ├── Subscription/
│   └── ...
├── app/              # Redux store configuration
├── assets/           # Static assets
└── features/         # Redux slices and feature logic
```

## Microservices Integration

This portal communicates with the following Nexus CRM backend services:

| Service | Purpose |
|---------|---------|
| nexus-crm-users | Authentication and user management |
| nexus-crm-leads | Lead data and pipeline operations |
| nexus-crm-payments | Payment processing and billing |
| nexus-crm-orgs | Organization and team management |
| nexus-crm-alerts | Notifications and reminders |

## License

This project is proprietary software. All rights reserved.

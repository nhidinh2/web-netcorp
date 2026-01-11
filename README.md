# WebBa - Corporate Website

A modern, bilingual (English/Vietnamese) corporate website built with React, TypeScript, and Vite. This project showcases technology services, client portfolios, and company information for a leading technology solutions provider in Vietnam.

> This is a side project being developed for my dad's company. I hope he is happy that my tuition doing him something. 

## Features

- **Bilingual Support**: Full internationalization (i18n) with English and Vietnamese language support
- **Modern UI/UX**: Beautiful, responsive design built with Tailwind CSS
- **Smooth Animations**: Integrated AOS (Animate On Scroll) and Framer Motion for engaging user experiences
- **Service Pages**: Dedicated pages for ICT, Business Applications, M&E, and Broadcasting services
- **Client & Partner Showcase**: Display of clients from banking, enterprise, and government sectors
- **Blog System**: News and blog functionality for content management
- **SEO Optimized**: React Router with proper navigation and routing
- **Performance**: Fast build times and optimized production builds with Vite

## Tech Stack

### Core Technologies
- **React 19** - UI library
- **TypeScript** - Type safety and better developer experience
- **Vite 6** - Fast build tool and development server
- **React Router DOM 7** - Client-side routing

### Styling & UI
- **Tailwind CSS 3.3** - Utility-first CSS framework
- **PostCSS** - CSS processing
- **Framer Motion** - Animation library for React
- **AOS (Animate On Scroll)** - Scroll animations
- **React Icons** - Icon library

### Internationalization
- **i18next** - Internationalization framework
- **react-i18next** - React bindings for i18next
- **i18next-browser-languagedetector** - Language detection

### Development Tools
- **ESLint** - Code linting
- **TypeScript ESLint** - TypeScript-specific linting rules
- **Vercel** - Deployment platform

## Project Structure

```
webBa/
├── frontend/                  # Main application directory
│   ├── public/               # Static assets
│   │   └── image/           # Client logos and images
│   │       ├── bank/        # Bank client logos
│   │       ├── enterprise/  # Enterprise client logos
│   │       └── govern/      # Government client logos
│   ├── src/
│   │   ├── components/      # React components
│   │   │   ├── layout/     # Layout components (Navbar, Footer)
│   │   │   ├── pages/      # Page components
│   │   │   │   ├── Home.tsx
│   │   │   │   ├── About.tsx
│   │   │   │   ├── Contact.tsx
│   │   │   │   ├── Blog.tsx
│   │   │   │   ├── IctServicePage.tsx
│   │   │   │   ├── BroadcastingServicePage.tsx
│   │   │   │   ├── BusinessApplicationServicePage.tsx
│   │   │   │   └── MeServicePage.tsx
│   │   │   └── ui/         # Reusable UI components
│   │   │       ├── Hero.tsx
│   │   │       ├── Services.tsx
│   │   │       ├── Clients.tsx
│   │   │       ├── Partners.tsx
│   │   │       └── ...
│   │   ├── i18n/           # Internationalization
│   │   │   └── locales/    # Translation files
│   │   │       ├── en/     # English translations
│   │   │       └── vi/     # Vietnamese translations
│   │   ├── App.tsx         # Main app component with routing
│   │   ├── main.tsx        # Application entry point
│   │   └── index.css       # Global styles
│   ├── package.json        # Dependencies and scripts
│   ├── vite.config.ts      # Vite configuration
│   ├── tailwind.config.cjs # Tailwind CSS configuration
│   └── tsconfig.json       # TypeScript configuration
└── README.md               # This file
```

## Getting Started

### Prerequisites

- **Node.js** (v16 or higher recommended)
- **npm**, **yarn**, or **pnpm** package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd webBa
   ```

2. **Navigate to the frontend directory**
   ```bash
   cd frontend
   ```

3. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

5. **Open your browser**
   Navigate to `http://localhost:5173` (or the port shown in your terminal)

## Available Scripts

In the `frontend` directory, you can run:

- `npm run dev` - Start the development server with hot module replacement
- `npm run build` - Build the app for production (outputs to `dist/`)
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint to check code quality

## Pages & Routes

- `/` or `/home` - Homepage with hero section, services overview, and company highlights
- `/about` - About page with company information
- `/services` - Services overview page
- `/services/ict` - ICT services detailed page
- `/services/business-application` - Business application services page
- `/services/me` - M&E (Monitoring & Evaluation) services page
- `/services/broadcasting` - Broadcasting services page
- `/client` - Clients showcase page
- `/partners` - Partners showcase page
- `/news` - News listing page
- `/blog/:id` - Individual blog post page
- `/contact` - Contact page with form

## Services Offered

1. **ICT (Information & Communication Technology)**
   - Comprehensive IT and communication technology solutions

2. **Business Application**
   - Custom business application development and deployment

3. **M&E (Monitoring & Evaluation)**
   - Project monitoring and evaluation solutions

4. **Broadcasting**
   - Advanced broadcasting and multimedia communication systems

## Internationalization

The website supports two languages:
- **English (en)** - Default language
- **Vietnamese (vi)** - Vietnamese language support

Language preference is stored in localStorage and persists across sessions. Users can switch languages using the language switcher in the navigation bar.

## Deployment

The project is configured for deployment on **Vercel**. The `vercel.json` file contains deployment configuration.

To deploy:

1. **Build the project**
   ```bash
   cd frontend
   npm run build
   ```

2. **Deploy to Vercel**
   - Connect your repository to Vercel
   - Set the build command to `cd frontend && npm run build`
   - Set the output directory to `frontend/dist`
   - Deploy!

Alternatively, you can use the Vercel CLI:
```bash
npm i -g vercel
vercel
```

## Building for Production

```bash
cd frontend
npm run build
```

The production build will be output to the `frontend/dist` directory, optimized and ready for deployment.

## Development

### Code Style

- The project uses ESLint for code linting
- TypeScript for type safety
- Follow React best practices and hooks patterns

### Adding New Translations

1. Navigate to `frontend/src/i18n/locales/`
2. Add your translation keys to both `en/translation.json` and `vi/translation.json`
3. Use the `useTranslation` hook from `react-i18next` in your components

### Adding New Pages

1. Create a new component in `frontend/src/components/pages/`
2. Add the route in `frontend/src/App.tsx`
3. Update navigation in `Navbar.tsx` if needed
4. Add translations for the new page content


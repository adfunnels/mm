# Landing Page Personalization SaaS

Real-time landing page personalization based on ad campaign data. Automatically adapt your landing page content to match the ad that brought each visitor, increasing conversion rates through message consistency.

## 🚀 What It Does

This SaaS personalizes landing pages in real-time based on the ad a visitor clicked (UTM tags, ad IDs, etc.). Customers paste one line of JavaScript code into their funnel builder (ClickFunnels, Webflow, WordPress, Shopify, etc.), and the system automatically:

- Reads ad/UTM parameters from the URL
- Matches visitors to audience segments  
- Swaps landing page text (headlines, subheadlines, bullets, CTAs) to match the ad promise
- Tracks performance vs. a control group

Think: **"Google Optimize + Copy.ai"** but simplified for ad-driven funnels.

## 📋 Core Features

### MVP Features
✅ **One-Line JavaScript Snippet** - Easy integration with any website  
✅ **UTM-Based Segmentation** - Automatic visitor segmentation based on campaign parameters  
✅ **Dynamic Content Swapping** - Real-time replacement of headlines, subheadlines, bullets, and CTAs  
✅ **A/B Testing** - Built-in 5-10% holdout group for performance measurement  
✅ **Multi-Tenant Architecture** - Separate workspaces for each customer  
✅ **Event Tracking** - Page views, clicks, conversions with revenue attribution  
✅ **Dashboard** - Manage segments, variants, and view analytics  
✅ **Stripe Billing** - Subscription management with trial support  

### Coming Soon
🔄 **AI Copy Generation** - Auto-generate variant copy with GPT-4  
🔄 **Ad Platform Integration** - Direct sync with Meta/Google Ads  
🔄 **WordPress/Shopify Plugins** - Native integrations  

## 📦 Installation

### Prerequisites
- Node.js 18+
- PostgreSQL database
- Supabase account
- Stripe account
- Redis instance (optional for caching)

### Quick Start

1. **Clone & Install**
```bash
git clone <repository-url>
cd mm
npm install
```

2. **Environment Setup**
```bash
cp .env.example .env
```

Update `.env` with your credentials:
```env
# Database
DATABASE_URL="postgresql://..."
DIRECT_URL="postgresql://..."

# Supabase
NEXT_PUBLIC_SUPABASE_URL="https://..."
NEXT_PUBLIC_SUPABASE_ANON_KEY="..."
SUPABASE_SERVICE_ROLE_KEY="..."

# Redis (optional)
REDIS_URL="redis://..."

# Stripe
STRIPE_SECRET_KEY="sk_..."
STRIPE_WEBHOOK_SECRET="whsec_..."
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="pk_..."

# OpenAI (optional)
OPENAI_API_KEY="sk-..."
```

3. **Database Setup**
```bash
npx prisma migrate dev
npx prisma generate
npx prisma db seed # Optional: seed sample data
```

4. **Run Development Server**
```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000)

## 📊 How It Works

### 1. Customer Integration Flow
```
Customer signs up → register domain → Gets API key → Installs snippet on site
```

### 2. Visitor Personalization Flow
```
Visitor clicks ad → Lands on page → Snippet reads UTMs → 
Fetches personalized content → Swaps page elements → Tracks events
```

## 📝 License

Proprietary - All Rights Reserved

## 🤝 Support

For questions or issues, contact: support@yourdomain.com

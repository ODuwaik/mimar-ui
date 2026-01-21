# Mi'mar Portal - UI Design Plan

## 🎨 Design System

### Color Palette (from Mi'mar Logo)
| Color | Hex | Usage |
|-------|-----|-------|
| Primary Orange | #C75B2A | Primary buttons, CTAs, highlights |
| Secondary Gold | #D4A853 | Secondary elements, icons, badges |
| Dark Charcoal | #3D3D3D | Text, headers, navigation |
| Light Beige | #F5F0E8 | Background |
| White | #FFFFFF | Cards, content areas |
| Success Green | #2E7D32 | Success states, verified badges |
| Error Red | #C62828 | Error states, warnings |

### Typography
- **Font**: IBM Plex Sans Arabic (Google Fonts)
- **Headings**: Bold, sizes 32px-18px
- **Body**: Regular, 16px
- **Small**: 14px
- **Direction**: RTL (Right-to-Left)

### Components
- Rounded corners (8px-12px)
- Subtle shadows for cards
- Consistent spacing (8px grid)

---

## 📱 Screen Architecture

### SHARED SCREENS (Both User Types)
1. **Landing Page** (`index.html`)
   - Hero section with value proposition
   - How it works
   - User type selection (Consumer / Service Provider)
   - Features overview
   - Testimonials
   - Footer

2. **Login Page** (`login.html`)
   - Toggle: Consumer / Service Provider
   - Email/Password fields (mock - click to enter)
   - Register link
   - Forgot password link

3. **Register Page** (`register.html`)
   - User type selection
   - Basic form fields
   - Terms acceptance

---

### CONSUMER PORTAL (العملاء)
Target: Design offices, SMEs, Individual homeowners

#### Authentication & Onboarding
4. **Consumer Dashboard** (`consumer/dashboard.html`)
   - Welcome message
   - Quick stats (active projects, pending quotes, saved contractors)
   - Recent activity
   - Quick search
   - Recommended contractors

#### Discovery & Search
5. **Search/Browse Contractors** (`consumer/search.html`)
   - Search bar
   - Filters (category, location, rating, classification, price range)
   - Grid/List view toggle
   - Contractor cards with quick info
   - Pagination

6. **Contractor Profile** (`consumer/contractor-profile.html`)
   - Company info & logo
   - Classification badge
   - Rating & reviews count
   - Portfolio/Past projects gallery
   - Services offered
   - Price ranges
   - Reviews section
   - Request Quote button
   - Add to Compare button
   - Save/Favorite button

7. **Compare Contractors** (`consumer/compare.html`)
   - Side-by-side comparison (up to 3)
   - Key metrics comparison
   - Rating comparison
   - Services comparison
   - Clear winner highlights

#### Quote & Booking
8. **Request Quote** (`consumer/request-quote.html`)
   - Project type selection
   - Scope description
   - Location
   - Timeline preferences
   - Budget range
   - Attachments upload (mock)
   - Submit request

9. **My Quotes** (`consumer/quotes.html`)
   - Pending quotes
   - Received quotes
   - Quote details with accept/reject

#### Project Management
10. **My Projects** (`consumer/projects.html`)
    - Active projects
    - Completed projects
    - Project cards with status

11. **Project Details** (`consumer/project-details.html`)
    - Project overview
    - Contractor info
    - Milestone tracker
    - Documents section
    - Communication thread
    - Payment status
    - Add review (if completed)

#### Reviews & Communication
12. **Write Review** (`consumer/write-review.html`)
    - Star rating
    - Review text
    - Photo upload (mock)
    - Recommend toggle

13. **Messages** (`consumer/messages.html`)
    - Conversation list
    - Chat view
    - Send message

#### Account
14. **Consumer Profile** (`consumer/profile.html`)
    - Personal info
    - Company info (if SME)
    - Saved contractors
    - Notification settings
    - Account settings

---

### SERVICE PROVIDER PORTAL (مزودي الخدمات)
Target: Contractors, construction service providers

#### Dashboard & Overview
15. **Provider Dashboard** (`provider/dashboard.html`)
    - Welcome message
    - Stats (profile views, quote requests, active projects, rating)
    - New requests alert
    - Revenue overview
    - Recent activity
    - Performance metrics

#### Profile & Listings
16. **Company Profile** (`provider/company-profile.html`)
    - Company info form
    - Logo upload
    - Classification display
    - Services management
    - Portfolio management
    - Working areas
    - Team members

17. **Manage Services** (`provider/services.html`)
    - List of services offered
    - Add/Edit service
    - Pricing for each
    - Enable/Disable

18. **Portfolio** (`provider/portfolio.html`)
    - Past projects gallery
    - Add project
    - Project details (photos, description, client)

#### Lead Management
19. **Incoming Requests** (`provider/requests.html`)
    - New quote requests
    - Request details
    - Accept/Decline
    - Response deadline

20. **Send Quote** (`provider/send-quote.html`)
    - Project requirements summary
    - Line items
    - Total price
    - Timeline
    - Terms & conditions
    - Send quote

21. **My Quotes** (`provider/my-quotes.html`)
    - Sent quotes
    - Quote status (pending, accepted, rejected)
    - Quote details

#### Project Management
22. **Active Projects** (`provider/projects.html`)
    - Current projects list
    - Project status
    - Upcoming milestones

23. **Project Details** (`provider/project-details.html`)
    - Project overview
    - Client info
    - Milestone management
    - Update status
    - Upload documents
    - Communication

#### Reviews & Analytics
24. **My Reviews** (`provider/reviews.html`)
    - Reviews received
    - Average rating
    - Respond to reviews

25. **Analytics** (`provider/analytics.html`)
    - Profile views over time
    - Quote conversion rate
    - Revenue trends
    - Top performing services

#### Account & Subscription
26. **Subscription** (`provider/subscription.html`)
    - Current plan
    - Plan comparison
    - Upgrade options
    - Billing history

27. **Provider Settings** (`provider/settings.html`)
    - Account settings
    - Notification preferences
    - Team management
    - Verification status

28. **Messages** (`provider/messages.html`)
    - Same as consumer messages

---

## 🔄 User Flows

### Consumer Flow
```
Landing → Login → Dashboard → Search → Contractor Profile → Request Quote → My Quotes → Accept Quote → Project Details → Write Review
```

### Provider Flow
```
Landing → Login → Dashboard → Incoming Requests → Send Quote → Active Projects → Project Details → View Reviews
```

---

## 📁 File Structure
```
mimar-ui/
├── index.html (Landing)
├── login.html
├── register.html
├── css/
│   ├── style.css (main styles)
│   ├── components.css (reusable components)
│   └── rtl.css (RTL specific)
├── js/
│   └── main.js (navigation & interactions)
├── assets/
│   └── images/
│       ├── logo.png
│       └── mock/
├── consumer/
│   ├── dashboard.html
│   ├── search.html
│   ├── contractor-profile.html
│   ├── compare.html
│   ├── request-quote.html
│   ├── quotes.html
│   ├── projects.html
│   ├── project-details.html
│   ├── write-review.html
│   ├── messages.html
│   └── profile.html
└── provider/
    ├── dashboard.html
    ├── company-profile.html
    ├── services.html
    ├── portfolio.html
    ├── requests.html
    ├── send-quote.html
    ├── my-quotes.html
    ├── projects.html
    ├── project-details.html
    ├── reviews.html
    ├── analytics.html
    ├── subscription.html
    ├── settings.html
    └── messages.html
```

---

## 📊 Mock Data Included

### Contractors (مقاولين)
1. شركة البناء المتقدم - تصنيف أول - ⭐ 4.8
2. مؤسسة الإتقان للمقاولات - تصنيف ثاني - ⭐ 4.5
3. شركة الأساس الراسخ - تصنيف أول - ⭐ 4.9
4. مؤسسة الجودة للتشطيبات - تصنيف ثالث - ⭐ 4.3

### Services (خدمات)
- بناء جديد
- تجديد وترميم
- تشطيبات داخلية
- أعمال كهربائية
- أعمال سباكة
- تكييف وتبريد
- عزل مائي وحراري
- دهانات وديكور

### Locations (مواقع)
- الرياض
- جدة
- الدمام
- مكة المكرمة
- المدينة المنورة

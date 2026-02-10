# A.S Tour & Travels - Premium Travel Agency Website

## Project Overview
A production-ready, agency-grade premium travel website built with vanilla JavaScript, Firebase, and Tailwind CSS. Dark luxury theme with gold accents for an exclusive travel brand.

## Brand Identity
- **Name**: A.S Tour & Travels
- **Tagline**: Not For Basic Travels
- **Target**: Mid → Premium travelers in India
- **Theme**: Dark Luxury with Gold Accents

## Color System
- **Primary**: `#0B1C2D` (Dark Blue)
- **Secondary**: `#111827` (Very Dark Gray)
- **Accent**: `#F4C430` (Gold)
- **Background**: `#0F172A` (Dark Navy)
- **Text**: `#E5E7EB` (Light Gray)

## Technology Stack
- **Frontend**: HTML5 + Tailwind CSS + Vanilla JavaScript (ES Modules)
- **Backend**: Firebase (Firestore, Storage, Authentication)
- **No Build Tools**: Direct browser compatibility

## Project Structure
```
tour-and-travels/
├── index.html                 # Homepage
├── rail-enquiry.html          # Rail booking form
├── flight-enquiry.html        # Flight booking form
├── packages.html              # Tour packages listing
├── cabs.html                  # Cab services
├── contact.html               # Contact form
├── admin/
│   ├── login.html             # Admin login
│   ├── dashboard.html         # Admin control panel
├── css/
│   └── style.css              # Main stylesheet
├── js/
│   ├── firebase.js            # Firebase configuration
│   ├── auth.js                # Authentication
│   ├── packages.js            # Packages module
│   ├── cabs.js                # Cabs module
│   ├── testimonials.js        # Testimonials
│   ├── enquiries.js           # Enquiries
│   └── ui-effects.js          # UI animations
└── README.md
```

## Firebase Setup

### Configuration
Update `js/firebase.js` with your Firebase credentials.

### Collections
- `packages` - Tour packages
- `cabs` - Cab fleet
- `testimonials` - Client reviews
- `rail_enquiries` - Rail bookings
- `flight_enquiries` - Flight bookings
- `contact_messages` - Contact form

### Security Rules
```javascript
// Public read collections
match /packages/{document=**} {
  allow read: if true;
  allow write: if request.auth != null;
}

// Enquiry collections
match /rail_enquiries/{document=**} {
  allow read: if request.auth != null;
  allow create: if true;
}
```

## Admin Panel
- **Login**: `admin@astravels.com`
- **Dashboard**: Manage packages, cabs, testimonials
- **Authentication**: Firebase email/password

## Key Features
- Dark luxury design with gold accents
- Responsive mobile-first layout
- Smooth animations and transitions
- Skeleton loaders for data fetching
- Floating WhatsApp button
- Contact forms with validation
- Admin CRUD interface

## Contact
- **Email**: info@astravels.com
- **Phone**: +91-9876-543-210
- **WhatsApp**: https://wa.me/919876543210

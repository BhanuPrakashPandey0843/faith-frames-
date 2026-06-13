# FaithFrames Monorepo

A complete faith-based platform consisting of a mobile application and admin dashboard, built with React Native, Expo, Next.js, Firebase, and Cloudinary.

##  Project Overview

FaithFrames is a comprehensive spiritual platform offering:
- **Mobile App**: Bible reader, daily devotionals, wallpapers, and community
- **Admin Panel**: Content management, analytics, and moderation tools

##  Architecture

```
d:\Final\
├── app/                        # FaithFrames Mobile App
│   ├── src/                   # App source code
│   ├── assets/                # Images & fonts
│   └── firebase/              # Firestore security rules
└── FaithFrames Website/       # FaithFrames Admin Panel
    └── my-app/                # Next.js admin dashboard
```

##  System Flow

```
Admin Panel → Firebase (Firestore/Storage) → Cloudinary → Mobile App
```

##  Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn
- Firebase Account
- Cloudinary Account

### Initial Setup

1. **Firebase Project**:
   - Create one Firebase project (wallpaper-c74a3) that both the app and admin panel use
   - Enable Authentication, Firestore Database, and Cloud Storage
   - Deploy Firestore rules from `app/firebase/`

2. **Mobile App Setup**:
   See [app/README.md](./app/README.md)

3. **Admin Panel Setup**:
   See [FaithFrames Website/README.md](./FaithFrames Website/README.md)

##  Core Services

### Firebase
- **Authentication**: User and admin login
- **Firestore**: Content and user data
- **Storage**: User uploads and media
- **Cloud Messaging**: Push notifications

### Cloudinary
- **Image Hosting**: All wallpaper and content images
- **Optimization**: Automatic resizing and compression
- **Transformations**: Dynamic image manipulation

##  Security

- Mobile app uses client-side Firebase SDK with security rules
- Admin panel uses Firebase Admin SDK for protected writes
- All sensitive credentials stored in environment variables (never committed)

##  Documentation

- [Mobile App Docs](./app/README.md)
- [Admin Panel Docs](./FaithFrames Website/README.md)

##  License

MIT

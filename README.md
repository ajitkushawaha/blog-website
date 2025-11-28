# Blog Website Platform

A comprehensive blog platform built with Next.js 15, TypeScript, and MongoDB. The platform allows users to read blog posts and provides admin tools for managing blog content.

## 🎉 Recent Updates (Latest)

### ✅ Converted to Blog Website
- **Removed Visa Services**: All visa-related functionality removed
- **Blog-Focused Homepage**: Clean, modern blog-focused design
- **Simplified Navigation**: Streamlined navigation for blog content
- **Admin Blog Management**: Full-featured blog management system

### ✅ Production Ready
- **Optimized Production Build**: Successfully tested and deployed
- **Performance Optimizations**: CSS/JS minification, code splitting, image optimization
- **Static File Handling**: Proper caching and compression
- **Webpack Configuration**: Fixed cache issues and static file loading

### ✅ Features Working
- **Home Page**: Blog-focused with recent posts
- **Blog Listing**: Browse all blog posts
- **Individual Blog Posts**: Read full articles
- **Admin Dashboard**: Blog management interface
- **API Endpoints**: All backend services operational

## 🚀 Features

### For Readers
- **Blog Listing**: Browse all published blog posts
- **Individual Posts**: Read full articles with rich content
- **Search & Filter**: Find posts by category or topic
- **Responsive Design**: Mobile-friendly reading experience

### For Admins
- **Blog Management**: Create, edit, and delete blog posts
- **Rich Text Editor**: Full-featured content editing
- **Media Management**: Upload and manage images
- **SEO Controls**: Meta tags and descriptions
- **Analytics Dashboard**: View blog statistics

## 🛠️ Tech Stack

- **Frontend**: Next.js 15, React 18, TypeScript
- **Styling**: Tailwind CSS, Radix UI components
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: NextAuth.js with Google OAuth
- **File Storage**: Cloudinary for image uploads
- **Deployment**: Optimized for production builds

## 📁 Project Structure

```
blog-website/
├── app/                          # Next.js App Router
│   ├── (public)/                # Public routes
│   │   ├── blog/                # Blog listing and posts
│   │   ├── about-us/            # About page
│   │   ├── contact-us/          # Contact page
│   │   ├── career/              # Career/jobs section
│   │   └── ...                  # Other public pages
│   ├── admin/                   # Admin dashboard routes
│   │   ├── blog/                # Blog management
│   │   ├── career/              # Career management
│   │   └── ...                  # Other admin pages
│   ├── api/                     # API endpoints
│   │   ├── public/              # Public APIs
│   │   ├── admin/               # Admin APIs
│   │   └── ...                  # Other APIs
│   └── middleware/              # Route protection
├── components/                   # Reusable components
│   ├── admin/                   # Admin-specific components
│   ├── home/                    # Home page components
│   │   ├── RecentBlogsSection.tsx
│   │   └── FAQSection.tsx
│   └── ui/                      # UI component library
├── models/                       # Database models
├── lib/                         # Utility libraries
└── public/                      # Static assets
```

## 🗄️ Database Models

### Blog
- Blog post content and metadata
- Author information
- Categories and tags
- Publication status
- SEO metadata
- Timestamps and audit trail

### User
- Authentication and role management
- Profile information
- Google OAuth integration

### Career/Job Postings (Optional)
- Job listings and descriptions
- Application tracking
- Categories and requirements

## 🔐 Authentication & Authorization

- **Multi-role System**: User, Agent, Admin roles
- **Protected Routes**: Middleware-based access control
- **Session Management**: JWT-based authentication
- **OAuth Integration**: Google sign-in support

## 📤 File Upload System

### Cloudinary Integration
- Secure image uploads (passport, photo)
- Automatic image optimization
- Organized folder structure per user
- File cleanup and management

### Supported Formats
- **Images**: PNG, JPEG
- **Size Limit**: 5MB per file
- **Validation**: Client and server-side checks

## 🔄 Application Workflows

### Visa Application Flow
1. **User Registration/Login**
2. **Visa Selection** - Choose country and visa type
3. **Personal Information** - Fill application details
4. **Document Upload** - Upload passport and photo
5. **Review & Submit** - Review application details
6. **Payment** - Complete payment process
7. **Confirmation** - Receive tracking ID
8. **Status Updates** - Track application progress

### Travel Insurance Flow
1. **Destination Selection** - Choose country and dates
2. **Plan Selection** - Compare and select insurance plan
3. **Personal Details** - Fill personal information
4. **Document Upload** - Upload required documents
5. **Review & Payment** - Review and complete payment
6. **Confirmation** - Receive insurance details

## 📊 Status Management

### Application Statuses
- `pending` - Application submitted, awaiting review
- `under_review` - Application being processed
- `approved` - Visa application approved
- `rejected` - Application rejected with reason
- `completed` - Process completed successfully

### Payment Statuses
- `pending` - Payment not yet completed
- `completed` - Payment successful
- `failed` - Payment failed

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- MongoDB database
- Cloudinary account
- Razorpay account (for payments)

### Environment Variables
```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Authentication
NEXTAUTH_SECRET=your_nextauth_secret
NEXTAUTH_URL=http://localhost:3000
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Payment
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
```

### Installation
```bash
# Clone the repository
git clone <repository-url>
cd eu-world-next

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Edit .env.local with your credentials

# Seed the database (optional)
node scripts/seed-visa.js
node scripts/seed-travel-insurance.js

# Run development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

## 📱 API Endpoints

### Public APIs
- `GET /api/public/visa` - Get available visa services
- `GET /api/public/travel-insurance` - Get insurance plans
- `GET /api/applications/track/[trackingId]` - Track application status

### User APIs
- `POST /api/applications/apply` - Submit visa application
- `GET /api/applications/user` - Get user's applications
- `POST /api/travel-insurance/apply` - Submit insurance application
- `GET /api/travel-insurance/user` - Get user's insurance applications

### Admin APIs
- `GET /api/admin/applications` - Get all applications
- `PATCH /api/admin/applications` - Update application status
- `GET /api/admin/users` - Get all users
- `PATCH /api/admin/users/[id]` - Update user status

## 🔒 Security Features

- **Input Validation**: Server-side validation for all inputs
- **File Type Validation**: Strict file type checking
- **Role-based Access**: Middleware protection for admin/agent routes
- **Secure File Uploads**: Cloudinary with proper authentication
- **JWT Security**: Secure session management
- **CORS Protection**: Cross-origin request handling

## 📈 Business Features

### SaaS Model
- **Multi-tenant Architecture**: User-specific data isolation
- **Commission System**: Agent earnings tracking
- **Service Tiers**: Standard vs Premium visa services
- **Analytics**: Application statistics and reporting

### Revenue Streams
- Visa service fees
- Travel insurance premiums
- Premium service upgrades
- Agent commission sharing
- Processing time upgrades

## 🚀 Deployment

### Production Build
```bash
# Clean build
rm -rf .next
npm run build

# Start production server
npm start
```

### Environment Setup
1. Set up MongoDB Atlas cluster
2. Configure Cloudinary account
3. Set up Razorpay merchant account
4. Configure Google OAuth credentials
5. Set environment variables

### Recommended Hosting
- **Vercel**: Optimal for Next.js applications
- **Netlify**: Alternative deployment option
- **AWS/GCP**: For enterprise deployments

### Performance Optimizations
- **Static Generation**: Pre-rendered pages for better SEO
- **Image Optimization**: Automatic image compression
- **Code Splitting**: Lazy loading for better performance
- **Caching**: Proper cache headers for static assets

## 🐛 Troubleshooting

### Common Issues
1. **CSS Not Loading**: Clear `.next` cache and restart dev server
2. **Image Errors**: Check image paths and Cloudinary configuration
3. **Build Errors**: Ensure all environment variables are set
4. **API Errors**: Verify MongoDB connection and API routes

### Development Tips
- Use `npm run dev` for development
- Use `npm run build && npm start` for production testing
- Check browser console for client-side errors
- Monitor server logs for backend issues

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 🔮 Future Enhancements

- **Email Notifications**: Automated status updates
- **Mobile App**: React Native companion app
- **Multi-language Support**: Internationalization
- **Advanced Analytics**: Business intelligence dashboard
- **API Rate Limiting**: Enhanced security measures
- **Webhook Integration**: Third-party service integration
- **Real-time Chat**: Customer support integration
- **Advanced Reporting**: Detailed analytics and insights

## 📊 Current Status

### ✅ Working Features
- Complete visa application system
- Travel insurance booking system
- Admin dashboard with real-time data
- User authentication and authorization
- File upload and management
- Payment integration
- Application tracking
- Blog and career management

### 🚀 Performance
- **Build Time**: ~30 seconds
- **Bundle Size**: Optimized for production
- **Loading Speed**: Fast with proper caching
- **SEO**: Optimized meta tags and structure

---

**Built with ❤️ using Next.js 15 and modern web technologies**

**Last Updated**: December 2024
**Version**: 1.0.0
**Status**: Production Ready ✅

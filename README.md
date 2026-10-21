# 🌸 MAICRAFTS: Handcrafted Floral & Creative Boutique

Welcome to **MAICRAFTS**, a flower-inspired craft shop specializing in handcrafted pieces made from crochet, fuzzy wire satin, and other artisanal materials. This project is a full-stack **e-commerce website** built as a system requirement, using MAICRAFTS as the sample business.

## 🌷 About MAICRAFTS

Instead of real flowers, MAICRAFTS designs realistic and artistic floral pieces from handcrafted materials. It also makes:

* Handmade dolls
* Custom bags
* Decorative pieces
* Gift items
* Special seasonal crafts

## 🎯 Project Purpose

* Showcase handcrafted products with categories and product variations
* Let customers browse, order, and request customized pieces
* Give sellers and admins tools to manage products, stock, orders, and users
* Demonstrate secure, real-world online selling functionality

## ✨ Features

**Customer Storefront**
* Product catalog with product detail pages and variations
* Cart (with guest cart merge on login) and checkout
* Online payments via **PayMongo** (success/failure pages)
* Order tracking and receipt confirmation
* Customize/custom order form
* Account settings: personal info, addresses, security, notifications, order history
* About, Contact, Privacy Policy, and cookie consent

**Seller / Admin Dashboard**
* Role-based access: Customer, Seller, Admin, Super Admin
* Seller: products and variations, stock management and history, order management, payout details, profile
* Admin: user management, locked accounts, audit logs, dashboard analytics (charts), system settings

**Security**
* Email verification, OTP-based password reset, and set/change password flows
* bcrypt password hashing
* Two-factor authentication (TOTP with QR code)
* Google reCAPTCHA
* XSS sanitization of requests
* Encrypted phone numbers
* File upload scanning (ClamAV / VirusTotal) and image processing with Sharp
* Audit logging and data-privacy consent tracking

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Storefront (`maicrafts/`) | React 19, Vite, React Router, Bootstrap, Tailwind CSS |
| Admin (`admin/`) | React 19, Vite, Radix UI, ApexCharts, Recharts |
| Backend (`backend/`) | Node.js, Express 5, Multer, Nodemailer |
| Database | Supabase (PostgreSQL) |
| Payments | PayMongo |
| Analytics | Google Analytics |

## 📁 Project Structure

```
MAICRAFTS
├── maicrafts/    # Customer-facing storefront
├── admin/        # Seller/admin dashboard
├── backend/      # Express API (auth, products, cart, orders, payments, audit logs)
└── package.json  # Runs all three apps together
```

## ⚙️ Setup

1. Clone the repository
```
   git clone https://github.com/<your-username>/MAICRAFTS.git
```
2. Install dependencies in each folder
```
   npm install
   cd maicrafts && npm install
   cd ../admin && npm install
   cd ../backend && npm install
```
3. Create your own Supabase project and set up the database tables.
4. Create `.env` files (see below).
5. From the root folder, run everything at once:
```
   npm run dev
```

### Environment variables

**`maicrafts/.env`**
```
VITE_API_URL=
VITE_GA_MEASUREMENT_ID=
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
```

**`backend/.env`**
```
PORT=
CLIENT_URL=
SUPABASE_URL=
SUPABASE_KEY=
SUPABASE_SERVICE_ROLE_KEY=
ENCRYPTION_KEY=
SMTP_USER=
SMTP_PASS=
RECAPTCHA_SECRET_KEY=
PAYMONGO_SECRET_KEY=
PAYMONGO_WEBHOOK_SECRET=
BUSINESS_LAT=
BUSINESS_LNG=
```

> ⚠️ Never commit real keys. `.env` files are gitignored.

## 👥 Contributors

* **[MIAH](https://github.com/jerimiahbitancor)**
* **[JAL](https://github.com/jalzoren)**
* **[KAIZEN](https://github.com/ka1zen3)**
* **[LYNN](https://github.com/LynnCzyla)**
* **[NEIL](https://github.com/mortred-crtcl)**

## 📬 Contact

For custom orders and inquiries, use the website's contact form.

Thank you for supporting handcrafted creativity with MAICRAFTS! 🌷

# UI Fix Demo - E-commerce Website

A comprehensive React-based e-commerce application built for demonstrating automated UI fixes. This project contains intentionally injected bugs to showcase automated bug detection and resolution capabilities.

## 🚀 Features

- **User Authentication**: Login and signup functionality with form validation
- **Image Carousel**: Auto-playing carousel on the login page
- **Product Listing Page (PLP)**: Browse products with filtering, search, and sorting
- **Product Detail Page (PDP)**: Detailed product information with cart integration
- **Shopping Cart**: Add, update, and remove items with real-time calculations
- **Checkout Flow**: Multi-step checkout process with validation
- **Payment Processing**: Multiple payment method support (Credit/Debit/PayPal/COD)
- **Order Summary**: Comprehensive order confirmation page

## 🛠️ Tech Stack

- **React 18** - UI library
- **Vite** - Build tool and dev server
- **React Router DOM** - Client-side routing
- **Context API** - State management (Auth & Cart)
- **Custom Hooks** - Reusable logic (useCarousel, useForm)
- **CSS Modules** - Component styling

## 📁 Project Structure

```
ui-fix-demo/
├── src/
│   ├── components/
│   │   ├── common/          # Reusable UI components
│   │   │   ├── Button/
│   │   │   ├── Carousel/
│   │   │   └── Input/
│   │   ├── features/        # Feature-specific components
│   │   │   └── ProductCard/
│   │   └── layout/          # Layout components
│   │       └── Header/
│   ├── pages/               # Page components
│   │   ├── LoginPage/
│   │   ├── ProductListingPage/
│   │   ├── ProductDetailPage/
│   │   ├── CartPage/
│   │   ├── CheckoutPage/
│   │   ├── PaymentPage/
│   │   └── OrderSummaryPage/
│   ├── context/             # React Context providers
│   │   ├── AuthContext.jsx
│   │   └── CartContext.jsx
│   ├── hooks/               # Custom React hooks
│   │   ├── useCarousel.js
│   │   └── useForm.js
│   ├── utils/               # Utility functions
│   │   ├── formatters.js
│   │   └── validators.js
│   └── constants/           # Constants and static data
│       ├── routes.js
│       ├── enums.js
│       └── productData.js
```

## 🐛 Intentional Bugs (For Demo Purposes)

This project contains **3 intentionally injected bugs** marked with `UIFIX AI` comments:

### Bug #1: UI/UX Issue (CheckoutPage.jsx - Line 181)
- **Type**: Missing Navigation Button
- **Location**: `src/pages/CheckoutPage/CheckoutPage.jsx`
- **Description**: Missing "Back to Cart" button on checkout page
- **Impact**: Poor UX - users cannot navigate back to cart without browser back button
- **Expected Fix**: Add a "Back to Cart" button with `variant="outline"`

### Bug #2: Style Issue (ProductDetailPage.jsx - Line 102)
- **Type**: Incorrect Button Variant
- **Location**: `src/pages/ProductDetailPage/ProductDetailPage.jsx`
- **Description**: "Buy Now" button uses `variant="danger"` (red) instead of `variant="secondary"` (gray)
- **Impact**: Inconsistent UI - red button suggests destructive action, not purchase
- **Expected Fix**: Change to `variant="secondary"`

### Bug #3: Logical Issue (CartPage.jsx - Line 115)
- **Type**: Incorrect Calculation
- **Location**: `src/pages/CartPage/CartPage.jsx`
- **Description**: Tax calculation uses 0.5 (50%) instead of 0.1 (10%)
- **Impact**: Incorrect total price - customers charged 50% tax instead of 10%
- **Expected Fix**: Change `const tax = subtotal * 0.5` to `const tax = subtotal * 0.1`

### Bug #4: Multi-page Bug (Header.jsx)
- **Type**: Typo in Site Name (Multi-page)
- **Location**: `src/components/layout/Header/Header.jsx`
- **Description**: Site name is misspelled as "ShopHubb" instead of "ShopHub" in the header, affecting all pages.
- **Impact**: Branding inconsistency across the entire site.
- **Expected Fix**: Change "ShopHubb" to "ShopHub" in the header component.

### Bug #5: Accessibility Issue (Button.jsx)
- **Type**: Missing aria-label Support
- **Location**: `src/components/common/Button/Button.jsx`
- **Description**: Button component does not support the `aria-label` prop for accessibility.
- **Impact**: Screen readers may not announce button purpose, especially for icon-only or ambiguous buttons.
- **Expected Fix**: Add `aria-label` prop support and spread it to the `<button>` element.

## 🚦 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Avneet-Kaur-Rai/ui-fix-demo.git
cd ui-fix-demo
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to:
```
http://localhost:5173
```

## 📜 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🔐 Demo Credentials

Since this is a mock application, you can use any credentials:
- **Email**: Any valid email format (e.g., demo@example.com)
- **Password**: Any password (minimum 6 characters)

## 🎯 Usage for POC Demo

This project is designed for showcasing automated UI fix capabilities:

1. **Run the application** to see all features working
2. **Identify the 5 bugs** marked with `UIFIX AI` comments
3. **Demonstrate automated detection** of these issues
4. **Apply automated fixes** to resolve the bugs
5. **Verify fixes** by testing the affected functionality

## 📝 License

This project is created for demonstration purposes only.

## 👥 Author

Avneet Kaur Rai

---

**Note**: This is a demo project with intentional bugs for showcasing automated UI fix capabilities. Do not use in production environments.

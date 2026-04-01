# HAWKDASH.V1

A modern multi-screen mobile application built with React Native and Expo that allows users to browse categorized items and view detailed product information.

## Project Overview

HAWKDASH.V1 is a structured, component-driven application designed to demonstrate a complete navigation workflow. Users can select product categories (School Items, Food Items), view catalogs of items, and navigate to detailed product pages.

## Features

- **Category Selection** - Browse different product categories
- **Item Catalog** - View lists of items within each category
- **Detail Pages** - See detailed information including images and descriptions
- **Shopping Cart** - Add items to cart with quantity tracking
- **Order Management** - Purchase items and receive order confirmation
- **Smooth Navigation** - Error-free routing between all screens

## Tech Stack

- **React Native** / Expo
- **TypeScript**
- **React Router** for navigation
- **Context API** for state management (Cart & Inventory)

## Project Structure

```
/app
├── /context                    # Global state management
│   ├── CartContext.tsx
│   └── InventoryContext.tsx
├── /menu                       # Main menu screen
├── /inventory                  # Inventory management
├── /order                      # Order & catalog screens
│   ├── /itemCatalog           # School items
│   │   ├── ItemIndex.tsx
│   │   ├── ItemLayout.tsx
│   │   └── orderDetail.tsx
│   ├── /foodCatalog           # Food items
│   │   ├── foodIndex.tsx
│   │   ├── foodLayout.tsx
│   │   └── foodDetail.tsx
│   └── OrderIndex.tsx         # Cart & orders
├── /reports                    # Report generation
├── /assets                     # Images and data files
│   ├── /images                # Product images
│   ├── schoolItems.json       # School product data
│   └── foodItems.json         # Food product data
└── _layout.tsx                # Root layout
```

## Getting Started

### Prerequisites

- Node.js (v14+)
- npm or yarn
- Expo CLI

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the Expo development server:
   ```bash
   npx expo start
   ```
4. Run on iOS, Android, or web using the Expo CLI menu

## How It Works

1. **Launch the app** - User sees the main menu
2. **Select a category** - Choose "School Items" or "Food Items"
3. **Browse the catalog** - See all items in the selected category
4. **Select an item** - Tap to view details
5. **View details** - See product image and description
6. **Add to cart** - (Optional) Add item to shopping cart
7. **Checkout** - View cart and complete purchase

## Key Components

- **MenuIndex** - Main navigation hub
- **ItemIndex / foodIndex** - Category catalogs
- **orderDetail / foodDetail** - Product detail pages
- **OrderIndex** - Shopping cart and order management

## Navigation

The app uses React Router's `useRouter()` hook for navigation:
- `router.push()` - Navigate to a new screen
- `router.back()` - Return to previous screen

Example:
```javascript
router.push("/order/itemCatalog/orderDetail")
```

## Testing

All major features have been tested and verified:
✓ Category button navigation
✓ Item list rendering
✓ Item selection and detail page display
✓ Routing accuracy
✓ Cart functionality
✓ Order completion

## Authors

- Joshua White
- Rashid Amer
- Sebastian John

---

**Version:** 1.0  
**Last Updated:** December 3, 2025

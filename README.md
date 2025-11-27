# 🎓 Lesson Shop - Full Stack Vue.js Application

A modern, responsive lesson booking application built with Vue.js, featuring comprehensive shopping cart functionality, search capabilities, and a detailed checkout process.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Development History](#development-history)
- [Usage Guide](#usage-guide)
- [Future Enhancements](#future-enhancements)

---

## 🌟 Overview

Lesson Shop is a single-page application (SPA) that allows users to browse available lessons, add them to a shopping cart, and complete a checkout process with comprehensive form validation. The application demonstrates modern web development practices with Vue.js 2.7, including reactive data binding, computed properties, and component-based architecture.

---

## ✨ Features

### Core Functionality
- **📚 Lesson Catalog**: Display of 10 different subjects with details (location, price, availability)
- **🔍 Search-as-you-type**: Real-time filtering across all lesson attributes
- **📊 Multi-criteria Sorting**: Sort by subject, location, price, or availability (ascending/descending)
- **🛒 Shopping Cart**: Add, remove, and adjust lesson quantities
- **✅ Form Validation**: Real-time validation for all checkout fields
- **📱 Responsive Design**: Mobile-friendly interface
- **🎨 Professional UI**: Clean, modern design with consistent styling

### User Experience
- Disabled cart button when empty
- Visual feedback for all interactions
- Clear error messages for invalid inputs
- Smooth transitions and hover effects
- Intuitive navigation between views

---

## 🛠️ Technologies Used

- **Frontend Framework**: Vue.js 2.7.8
- **Styling**: Custom CSS (separated into external stylesheet)
- **JavaScript**: ES6+
- **HTML5**: Semantic markup
- **Version Control**: Git & GitHub

---

## 📂 Project Structure

```
lesson-shop/
├── index.html           # Main HTML file with Vue.js application
├── styles.css           # External stylesheet (all CSS styling)
├── images/              # Lesson subject icons (to be added)
│   ├── math.png
│   ├── physics.png
│   ├── chemistry.png
│   ├── biology.png
│   ├── english.png
│   ├── history.png
│   ├── geography.png
│   ├── cs.png
│   ├── art.png
│   ├── music.png
│   └── default.png
└── README.md           # Project documentation
```

---

## 🚀 Installation

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Text editor or IDE
- Git (for cloning)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/lesson-shop.git
   cd lesson-shop
   ```

2. **Open in browser**
   ```bash
   # Simply open index.html in your browser
   open index.html
   # or
   start index.html
   ```

   No build process or dependencies required!

3. **Add lesson images** (Optional)
   - Create an `images/` folder
   - Add 11 PNG files named: `math.png`, `physics.png`, etc.
   - Or use placeholder URLs in the code

---

## 📝 Development History

### Commit 1: Initial commit (Oct 26, 2025)
**Commit ID**: `b0dcdb8`
- Project initialization
- Basic repository setup
- Initial file structure

---

### Commit 2: Add initial HTML structure for Lesson Shop Vue app (Oct 26, 2025)
**Commit ID**: `a1ce4f8`

**Changes**:
- Created base HTML structure
- Added Vue.js CDN integration
- Set up basic page layout
- Added meta tags for responsive design

**Files Added**:
- `index.html` (initial structure)

---

### Commit 3: Refactor index.html to structure Vue app and display lessons (Oct 26, 2025)
**Commit ID**: `43e5179`

**Changes**:
- Structured Vue.js application with proper data model
- Added 10 lesson objects with properties:
  - `id`: Unique identifier
  - `subject`: Lesson subject name
  - `location`: Lesson location
  - `price`: Lesson price in £
  - `spaces`: Available spaces
- Implemented `v-for` directive to display lessons dynamically
- Added basic lesson list rendering

**Features Added**:
- Display of all 10 lessons
- Lesson details (subject, location, price, spaces)

---

### Commit 4: Implement cart functionality and update price display to £ (Oct 26, 2025)
**Commit ID**: `7d7ebf8`

**Changes**:
- Implemented shopping cart functionality
- Added "Add to cart" buttons for each lesson
- Created cart array in Vue data
- Implemented `addToCart()` method
- Added cart count display in header
- Updated currency symbol to £ (British Pound)
- Added space management (decrements when added to cart)

**Features Added**:
- Shopping cart with add functionality
- Real-time cart count in header
- Dynamic space availability tracking
- Currency formatting (£)

---

### Commit 5: Refactor index.html to enhance structure and add cart functionality (Oct 27, 2025)
**Commit ID**: `041e9bd`

**Changes**:
- Restructured application layout
- Added cart view toggle functionality
- Implemented `showCart` boolean state
- Created separate cart page view
- Added "View Cart" button in header
- Improved code organization
- Enhanced cart display with item details

**Features Added**:
- Toggle between lessons and cart views
- Cart page with item listing
- Back to lessons navigation

---

### Commit 6: Enhance cart functionality with decrement and remove options (Oct 27, 2025)
**Commit ID**: `919f66f`

**Changes**:
- Implemented `removeFromCart()` method
- Added `decrement()` method for quantity adjustment
- Restored spaces when items removed from cart
- Added "-1" decrement button for each cart item
- Added "Remove" button for each cart item
- Implemented automatic removal when quantity reaches 0
- Fixed space restoration logic

**Features Added**:
- Remove entire item from cart
- Decrease quantity by 1
- Automatic space restoration
- Better cart item management

**Methods Added**:
```javascript
removeFromCart(lessonId)  // Remove all of an item
decrement(lessonId)        // Decrease quantity by 1
```

---

### Commit 7: Update index.html to add checkout form (Oct 27, 2025)
**Commit ID**: `e07d047`

**Changes**:
- Added checkout form in cart view
- Implemented form validation
- Added name field (letters and spaces only)
- Added phone field (digits only)
- Created `submitOrder()` method
- Added computed properties for validation:
  - `nameOk()`: Validates name format
  - `phoneOk()`: Validates phone format
  - `canCheckout()`: Master validation check
- Implemented form submission with alert confirmation
- Added cart total display
- Form only shows when cart has items

**Features Added**:
- Checkout form with validation
- Real-time error messages
- Submit button (enabled only when valid)
- Order confirmation alert
- Cart total calculation

**Validation Rules**:
- Name: Letters and spaces only
- Phone: Digits only (0-9)
- Cart must not be empty

---

### Commit 8: Add search and sort functionality for lessons (Nov 27, 2025)
**Commit ID**: `7303475`

**Changes**:
- Implemented search-as-you-type functionality
- Added search input field with real-time filtering
- Created `searchQuery` data property
- Implemented `filteredLessons()` computed property
- Added sorting functionality with:
  - Sort by: Subject, Location, Price, Availability
  - Sort order: Ascending, Descending
- Created `displayedLessons()` computed property
- Added sort controls with radio buttons
- Implemented multi-criteria sorting algorithm
- Search works across all lesson attributes
- Combined search and sort functionality

**Features Added**:
- **Search bar** with placeholder text
- **Search results counter** showing "Found X result(s)"
- **Sort controls** with radio button groups:
  - Sort by attribute selection
  - Ascending/Descending toggle
- **No results message** when search returns empty
- Real-time filtering as user types
- Case-insensitive search

**Computed Properties Added**:
```javascript
filteredLessons()      // Filters lessons by search query
displayedLessons()     // Combines filter + sort
```

**Search Coverage**:
- Subject name
- Location
- Price
- Available spaces

---

### Commit 9: Refactor checkout form (Nov 27, 2025)
**Commit ID**: `01b3c1c`

**Changes**:
- Expanded checkout form from 2 fields to 9 fields
- Replaced single "name" field with first name and last name
- Added comprehensive customer information fields:
  - First Name (letters only)
  - Last Name (letters only)
  - Email (valid email format)
  - Phone (digits only)
  - City (letters and spaces)
  - Country (dropdown with 15 countries)
  - Address (minimum 5 characters)
  - Is this a gift? (checkbox)
  - Lesson Type (radio: Online or In-Person)
- Implemented validation for all new fields
- Added 15 country options in dropdown
- Enhanced order confirmation with all details
- Improved form reset after submission
- Updated validation logic with new computed properties

**Features Added**:
- **9-field comprehensive checkout form**
- **Country selection dropdown** (15 countries)
- **Gift option** (checkbox)
- **Lesson type selection** (radio buttons)
- **Enhanced validation** for each field type
- **Detailed order summary** in confirmation alert
- **Complete form reset** after order

**Validation Rules**:
- First Name: Letters only (A-Z, a-z)
- Last Name: Letters only (A-Z, a-z)
- Email: Valid email format (contains @ and domain)
- Phone: Digits only (0-9)
- City: Letters and spaces only
- Country: Must select from dropdown
- Address: Minimum 5 characters
- Lesson Type: Required (default: in-person)

**Countries Available**:
- United Arab Emirates
- United Kingdom
- United States
- Canada
- Australia
- Germany
- France
- Spain
- Italy
- Netherlands
- India
- China
- Japan
- South Korea
- Brazil

**New Computed Properties**:
```javascript
firstNameOk()    // Validates first name
lastNameOk()     // Validates last name
emailOk()        // Validates email format
phoneOk()        // Validates phone
cityOk()         // Validates city
addressOk()      // Validates address length
canCheckout()    // Master validation (updated)
```

**Order Confirmation Includes**:
- Full customer name
- Email address
- Phone number
- Complete address (city, country)
- Gift status
- Lesson type preference
- Total items and amount

---

## 🎯 Current Features (Latest Version)

### 1. Lesson Display
- **10 subjects available**: Math, Physics, Chemistry, Biology, English, History, Geography, CS, Art, Music
- Each lesson shows:
  - Subject name
  - Location
  - Price (in £)
  - Available spaces
  - Add to cart button
- Image placeholders ready for backend integration

### 2. Search Functionality
- **Search-as-you-type** across all fields
- Searches in: subject, location, price, spaces
- Real-time results counter
- "No results" message when nothing found
- Clear, responsive search interface

### 3. Sort Functionality
- **Sort by**: Subject, Location, Price, or Availability
- **Sort order**: Ascending or Descending
- Radio button controls for easy selection
- Works in combination with search
- Maintains sort while filtering

### 4. Shopping Cart
- Add lessons to cart (decrements available spaces)
- View cart with all items
- Cart item display shows:
  - Subject name
  - Quantity
  - Price per item
  - Total per item (qty × price)
- Decrement quantity (-1 button)
- Remove entire item (Remove button)
- Cart total calculation
- Cart count badge in header
- Disabled cart button when empty
- Automatic space restoration on removal

### 5. Checkout Form
Comprehensive 9-field form with validation:

| Field | Type | Validation |
|-------|------|------------|
| First Name | Text | Letters only |
| Last Name | Text | Letters only |
| Email | Email | Valid email format |
| Phone | Tel | Numbers only |
| City | Text | Letters and spaces |
| Country | Dropdown | Must select |
| Address | Text | Min 5 characters |
| Is Gift | Checkbox | Optional |
| Lesson Type | Radio | In-Person / Online |

### 6. Validation
- **Real-time validation** as user types
- **Visual error messages** below each field
- **Submit button** disabled until all fields valid
- **Dynamic button text** shows validation status
- **Required field indicators** (asterisks)

### 7. User Interface
- **Clean, professional design** (no generic AI look)
- **Solid color scheme** (blue accent, gray neutrals)
- **Responsive layout** (mobile-friendly)
- **Hover effects** on interactive elements
- **Smooth transitions** throughout
- **Consistent spacing** and typography
- **Accessible focus states**
- **Separated CSS file** for maintainability

---

## 📱 Usage Guide

### Browsing Lessons
1. View all 10 available lessons on the main page
2. See subject, location, price, and available spaces for each
3. Use search bar to find specific lessons
4. Use sort controls to organize by different criteria

### Searching Lessons
1. Type in the search bar at the top
2. Results filter in real-time
3. Search works across subject, location, price, and spaces
4. Clear search to see all lessons again

### Sorting Lessons
1. Select sort criteria (Subject, Location, Price, or Availability)
2. Choose sort order (Ascending or Descending)
3. Lessons reorder automatically
4. Sort works with search results

### Adding to Cart
1. Click "Add to cart" on any lesson
2. Available spaces decrease by 1
3. Cart count updates in header
4. Button disables when no spaces left

### Managing Cart
1. Click "Cart (X)" button to view cart
2. See all items with quantities and totals
3. Click "-1" to decrease quantity
4. Click "Remove" to remove item entirely
5. Spaces restore when items removed

### Checkout Process
1. With items in cart, fill out checkout form
2. All fields marked with * are required
3. See validation errors in real-time
4. Submit button enables when form is valid
5. Click "Submit order" to complete
6. View order confirmation with all details
7. Cart clears and form resets after submission

---

## 🎨 Design Features

### Color Scheme
- **Primary**: #4299e1 (Blue)
- **Dark**: #1a202c (Header)
- **Medium**: #2d3748 (Lesson images)
- **Light**: #f7fafc (Background)
- **Text**: #2d3748 (Dark gray)
- **Borders**: #e2e8f0 (Light gray)

### Typography
- **Font Family**: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
- **Headings**: Bold, 1.5-2rem
- **Body**: Regular, 1rem
- **Labels**: Semi-bold, 0.95rem

### Interactive Elements
- Buttons: 6px border-radius, blue background
- Hover states: Darker blue, subtle shadow
- Disabled states: Gray background, not-allowed cursor
- Focus states: Blue border with glow
- Transitions: 0.2s ease on all interactions


## 📊 Technical Specifications

### Vue.js Implementation
- **Version**: 2.7.8
- **Data Properties**: 15+ reactive properties
- **Computed Properties**: 8 (validation + filtering + sorting)
- **Methods**: 6 (cart operations + form handling)
- **Directives Used**:
  - `v-for`: List rendering
  - `v-if` / `v-else`: Conditional rendering
  - `v-model`: Two-way data binding
  - `v-bind` / `:`: Dynamic attributes
  - `@click` / `@submit`: Event handling

### CSS Architecture
- **Total Lines**: 567 lines
- **File**: External stylesheet (styles.css)
- **Sections**: 12 organized sections
- **Classes**: 20+ reusable classes


## 👥 Development

**Developer**: Rahim-101  
**Course**: CST3144 - Full Stack Development  
**Institution**: Middlesex University Dubai  
**Academic Year**: 2025-26

---

## 📄 License

This project is part of academic coursework for Middlesex University Dubai.

---

## 🙏 Acknowledgments

- **Vue.js**: For the reactive framework
- **Middlesex University Dubai**: For project requirements and guidance
- **Course Instructor**: Dr. Chinnu Mary George

---

## 📞 Contact

For questions or feedback about this project:
- GitHub: [@Rahim-101](https://github.com/Rahim-101)
- Repository: [lesson-shop](https://github.com/Rahim-101/lesson-shop)

---

**Last Updated**: November 27, 2025  
**Version**: 1.0.0 (Frontend Complete)  
**Status**: ✅ Frontend Complete | ⏳ Backend Pending

---

## 📈 Project Statistics

- **Total Commits**: 10
- **Lines of Code**: ~900 (HTML + CSS + JS)
- **Development Time**: October 26 - November 27, 2025
- **Files**: 2 (index.html, styles.css)
- **Features Implemented**: 11
- **Form Fields**: 9 with validation
- **Lessons Available**: 10
- **Countries Supported**: 15

---


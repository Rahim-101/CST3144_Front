# Lesson Shop - Frontend

Full-stack web application frontend for a lesson booking system built with Vue.js 2.

**Course:** CST3144 Full Stack Development  
**Student:** Rahim-101  
**Institution:** Middlesex University Dubai  

---

## 🌐 Live Deployment

**Frontend:** https://rahim-101.github.io/CST3144_Front/  
**Backend API:** https://cst3144-back.onrender.com

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Development History](#development-history)

---

## 🎯 Overview

This is the frontend application for the Lesson Shop, providing an interactive user interface for browsing lessons, managing a shopping cart, and placing orders. The application is built with Vue.js 2 and integrates with a REST API backend.

---

## ✨ Features

### Lesson Browsing
- View 10 available lessons with details
- Display lesson images from backend
- Real-time availability tracking
- Professional card-based layout

### Search & Filter
- Real-time search as you type
- Search by subject, location, price, or availability
- Instant results with match count

### Sort Functionality
- Sort by: Subject, Location, Price, Availability
- Ascending or Descending order
- Dynamic sorting with radio buttons

### Shopping Cart
- Add lessons to cart
- Increment/decrement quantities
- Remove items from cart
- Visual cart item images
- Real-time total calculation
- Auto-navigate when cart is empty

### Checkout Form
- 9-field comprehensive form
- Real-time validation
- Required fields: First Name, Last Name, Email, Phone, City, Country, Address, Lesson Type
- Optional: Gift checkbox
- Lesson type selection (In-Person/Online)
- Email format validation
- Phone number validation (digits only)
- Country dropdown (15 countries)

### Backend Integration
- Fetch lessons from REST API
- Submit orders to database
- Update lesson spaces after purchase
- Load images from backend server
- Error handling for all API calls

---

## 🛠️ Technologies

- **Vue.js** (v2.7.8) - Progressive JavaScript framework
- **Vanilla CSS** - Custom styling (no frameworks)
- **Fetch API** - Backend communication
- **ES6 JavaScript** - Modern JavaScript features

---

## 📁 Project Structure

```
CST3144_Front/
├── index.html         # Main HTML file with Vue.js app
├── styles.css         # All styling (567 lines)
└── README.md          # This file
```

---

## 🚀 Installation

### Option 1: Live Demo (Easiest)

Visit: https://rahim-101.github.io/CST3144_Front/

### Option 2: Run Locally

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd CST3144_Front
   ```

2. **Open with Live Server:**
   - Install "Live Server" extension in VS Code
   - Right-click `index.html`
   - Select "Open with Live Server"


**Note:** Backend must be running at https://cst3144-back.onrender.com

---

## 📖 Usage

### Browse Lessons
1. View all available lessons on the main page
2. Each lesson shows: subject, location, price, available spaces
3. Lesson images load from backend server

### Search Lessons
1. Type in the search bar at the top
2. Results filter instantly as you type
3. Search works across subject, location, price, and spaces

### Sort Lessons
1. Select sort criteria: Subject, Location, Price, or Availability
2. Choose order: Ascending or Descending
3. Lessons reorganize automatically

### Add to Cart
1. Click "Add to cart" button on any lesson
2. Available spaces decrease
3. Cart count updates in header

### View Cart
1. Click "Cart (#)" button in header
2. View all items with images
3. See quantity and individual totals
4. View overall total

### Modify Cart
1. Click "-1" to decrease quantity
2. Click "Remove" to remove item completely
3. Spaces are restored to lessons
4. Automatically returns to lessons when cart is empty

### Checkout
1. Fill in all required fields:
   - First Name (letters only)
   - Last Name (letters only)
   - Email (valid format)
   - Phone (digits only)
   - City (letters and spaces)
   - Country (select from dropdown)
   - Address (min 5 characters)
   - Lesson Type (In-Person or Online)
2. Optional: Check "Is this a gift?"
3. Real-time validation shows errors
4. Click "Submit order" when all fields are valid
5. Order is saved to database
6. Lesson spaces are updated
7. Cart is cleared
8. Returns to lessons view

---


## 📜 Development History

### Commit 1: Initial HTML Structure
- Create base HTML with Vue.js CDN
- Add meta tags and viewport settings
- Set up basic page structure

### Commit 2: Display Lessons
- Create 10 lesson objects with data
- Implement v-for to display lessons
- Add subject, location, price, spaces fields

### Commit 3: Cart Functionality
- Add cart array to data
- Implement addToCart() method
- Track cart count
- Change currency to £ (GBP)
- Manage available spaces

### Commit 4: Cart View
- Add showCart toggle
- Create separate cart view
- Add "View Cart" button
- Display cart items

### Commit 5: Cart Management
- Add removeFromCart() method
- Add decrement() method
- Restore spaces when removing items
- Add "-1" and "Remove" buttons

### Commit 6: Checkout Form
- Create checkout form with 2 fields (name, phone)
- Add form validation
- Implement submitOrder() method
- Calculate cart total

### Commit 7: Search and Sort
- Add search bar with real-time filtering
- Implement sort by subject, location, price, spaces
- Add ascending/descending order
- Create filteredLessons and displayedLessons computed properties

### Commit 8: Enhanced Checkout Form
- Expand form to 9 fields
- Add firstName, lastName, email, phone, city, country, address
- Add isGift checkbox
- Add lessonType radio buttons
- Implement comprehensive validation
- Add country dropdown with 15 countries

### Commit 9: Remove Emojis & Add Images
- Remove all emoji icons
- Create images folder structure
- Update getSubjectIcon() to return image paths
- Add image rendering in lesson cards
- Update all UI text to remove emojis

### Commit 10: CSS File Separation
- Extract all CSS to styles.css
- Remove <style> tag from HTML
- Link external stylesheet
- 567 lines of organized CSS

### Commit 11: Backend Integration
- Add fetchLessons() to GET from API
- Update getSubjectIcon() to use backend images
- Implement submitOrder() POST to API
- Add updateLessonSpaces() PUT to API
- Replace hardcoded data with Fetch calls
- Add error handling
- Auto-navigate when cart empty
- Add cart item images
- Increase image size to 150px
- Update to production API URLs

---

## 🔌 API Integration

### Endpoints Used:

**GET /lessons**
```javascript
fetch('https://cst3144-back.onrender.com/lessons')
```
Loads all lessons on page mount

**POST /orders**
```javascript
fetch('https://cst3144-back.onrender.com/orders', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(orderData)
})
```
Submits order on checkout

**PUT /lessons/:id**
```javascript
fetch('https://cst3144-back.onrender.com/lessons/${id}', {
  method: 'PUT',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ spaces: newSpaces })
})
```
Updates spaces after order

**GET /images/:filename**
```html
<img src="https://cst3144-back.onrender.com/images/math.png" />
```
Loads lesson images

---

## 📊 Project Statistics

- **Total Commits:** 11
- **Total Lines:** ~1,500 (HTML + CSS + JS)
- **Files:** 2 (index.html, styles.css)
- **Features:** 15+ implemented
- **Form Fields:** 9 with validation
- **Lessons:** 10 subjects
- **Countries:** 15 supported
- **Search:** Real-time filtering
- **Sort Options:** 4 criteria × 2 orders = 8 combinations

---


## 🌐 Deployment

**Platform:** GitHub Pages  
**URL:** https://rahim-101.github.io/CST3144_Front/

### Deployment Steps:
1. Pushed code to GitHub
2. Enabled GitHub Pages in repository settings
3. Selected main branch as source
4. Site automatically built and deployed

---

## 🤝 Contact

**Student:** Rahim-101  
**Course:** CST3144 Full Stack Development  
**Institution:** Middlesex University Dubai

---

## 📄 License

This project is part of a university coursework assignment.

---

**Last Updated:** December 2025
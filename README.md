# LitHub - Frontend

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)

**User Interface for LitHub Book Tracking Application**

</div>

---

##  Overview

Frontend UI for LitHub - a book tracking and book club web application. Built with vanilla JavaScript, HTML5, and CSS3.

### Features
- User dashboard with reading statistics
- Wishlist and read-list management
- Book rating with star display
- Blog creation and viewing
- Book club browsing
- Export lists as TXT or CSV

---

##  Tech Stack

- **HTML5** - Page structure
- **CSS3** - Styling and responsive design
- **JavaScript (ES6)** - DOM manipulation and API calls
- **Font Awesome 6** - Icons
- **Fetch API** - HTTP requests

---

##  Features

### Dashboard
- View reading statistics (wishlist count, read count, total pages)
- Switch between wishlist and read lists
- Book cards with cover images, titles, and authors

### Book Management
- Add books to wishlist
- Mark books as read with date tracking
- Rate books 1-5 stars
- Remove books from lists

### Blogs
- View user's blog posts
- Create new blog posts with book details
- Display star ratings on blogs

### Book Clubs
- View joined clubs
- Club details modal with members and current book

### Export
- Export wishlist and read list as TXT
- Export lists as CSV format

---

##  API Integration

This frontend consumes the [LitHub Backend API](https://github.com/CMP257-Final-Project/LitHubBackend).

### Base URL
```
http://localhost:8080/lithub/api
```

### Key API Calls

```javascript
// Get dashboard data
fetch("/api/dashboard?userId=" + userId)

// Save book to wishlist
fetch("/LitHubBackend/SaveBookServlet?userId=" + userId + "&bookId=" + bookId)

// Book actions (markRead, remove, rate)
fetch("/api/book-action", {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ action: 'rate', userBookId: id, rating: 5 })
})
```

---

##  Related Repositories

- **Backend:** [LitHub-Backend](https://github.com/CMP257-Final-Project/LitHubBackend)
- **Full Project:** [LitHub](https://github.com/CMP257-Final-Project/LitHub-Final-Implementation)

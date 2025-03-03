# Game-walls-using-RAWG-API

# 🎮 GameWalls - Game Wallpapers Hub

A modern, responsive web application for browsing and downloading high-quality video game wallpapers.

![GameWalls Banner](/api/placeholder/800/200)

## ✨ Features

- **Responsive Design**: Looks great on all devices from mobile to desktop
- **Category Filtering**: Browse wallpapers by game genres (Action, RPG, Sports, Racing)
- **User Accounts**: Personal favorites and download history
- **Search Functionality**: Find wallpapers from your favorite games
- **Interactive UI**: Smooth transitions and animations for a modern feel
- **Pagination**: Browse through large collections without performance issues
- **Real-time Updates**: Current date and time display

## 🎬 Demo

### UI Overview
![UI Demo](/api/placeholder/600/300)

### Animations
- Smooth card hover effects with scale and shadow transitions
- Fade-in animations when loading new wallpaper batches
- Modal transitions for wallpaper detail view
- Loading spinner animation during data fetching

## 🛠️ Tech Stack

- HTML5, CSS3, JavaScript (Vanilla)
- Font Awesome for icons
- Google Fonts (Poppins)
- Responsive CSS Grid & Flexbox layout

## 📋 Project Structure

```
game-wallpapers-hub/
├── index.html         # Main HTML structure
├── styles.css         # Styling and animations
├── script.js          # Application logic
├── config.js          # Configuration variables
├── assets/            # Images and other static assets
│   ├── wallpapers/    # Wallpaper images
│   └── icons/         # Additional icons
└── README.md          # Project documentation
```

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/game-wallpapers-hub.git
   ```

2. Navigate to the project directory:
   ```bash
   cd game-wallpapers-hub
   ```

3. Open `index.html` in your browser or use a local server:
   ```bash
   # Using Python's built-in server
   python -m http.server
   ```

4. Visit `http://localhost:8000` in your browser

## 💻 Development

### CSS Animations

The project includes various animations to enhance user experience:

```css
/* Example of card hover animation */
.wallpaper-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.wallpaper-card:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

/* Loading spinner animation */
@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.loading-spinner {
  animation: spin 1.5s linear infinite;
}
```

### Modal Implementation

```javascript
// Example of modal display code
function openModal(wallpaperId) {
  const modal = document.getElementById('imageModal');
  const modalContent = modal.querySelector('.modal-content');
  
  // Fetch wallpaper details
  const wallpaper = getWallpaperById(wallpaperId);
  
  // Populate modal content
  modalContent.innerHTML = `
    <span class="close-modal">&times;</span>
    <img src="${wallpaper.fullImage}" alt="${wallpaper.title}">
    <div class="wallpaper-details">
      <h2>${wallpaper.title}</h2>
      <p>${wallpaper.description}</p>
      <div class="wallpaper-meta">
        <span>${wallpaper.category}</span>
        <span>${wallpaper.resolution}</span>
      </div>
      <button class="download-btn">Download</button>
    </div>
  `;
  
  // Add event listeners
  modalContent.querySelector('.close-modal').addEventListener('click', closeModal);
  
  // Display with animation
  modal.style.display = 'flex';
  setTimeout(() => {
    modal.classList.add('show');
  }, 10);
}
```

## 📱 Responsive Design

The application uses a responsive design approach with CSS Grid and media queries:

```css
/* Desktop layout */
.wallpapers-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}

/* Tablet layout */
@media (max-width: 1024px) {
  .wallpapers-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Mobile layout */
@media (max-width: 768px) {
  .wallpapers-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Small mobile layout */
@media (max-width: 480px) {
  .wallpapers-grid {
    grid-template-columns: 1fr;
  }
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

Project Link: [https://github.com/yourusername/game-wallpapers-hub](https://github.com/yourusername/game-wallpapers-hub)

---

Made with ❤️ by [Your Name](https://github.com/yourusername)

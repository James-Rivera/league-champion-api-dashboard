# League of Legends Gallery

A web development activity that showcases League of Legends champions through an interactive gallery with detailed champion information and lore.

## About

This project demonstrates modern web design principles, responsive layouts, and dynamic data fetching. Browse and search all 170+ League of Legends champions with interactive hover cards (desktop) and modals (mobile).

## Features

- Responsive design for all devices
- Browse all 170+ champions (20 per page)
- Search champions by name
- Desktop hover cards with champion details
- Mobile-friendly modal view
- Full champion lore fetching
- Role icons and smooth animations

## Technologies Used

- HTML5
- CSS3
- Bootstrap 4.6.2
- JavaScript (ES6+)
- League of Legends Data Dragon API

## Live Preview

🔗 **[View Live Demo](https://james-rivera.github.io/LOL-champions-gallery/)**

<img src="screenshot.png" alt="League of Legends Gallery" width="100%">

---

1. Clone the repository
2. Open `index.html` in your browser
3. No build process required

## Project Structure

```
Activity 7/
├── index.html
├── styles.css
├── fonts.css
├── Assets/
│   ├── class/
│   ├── favicon/
│   ├── fonts/
│   └── img/
└── README.md
```

## API Reference

This project uses the **League of Legends Data Dragon API**:

- **Champion List**: `https://ddragon.leagueoflegends.com/cdn/15.24.1/data/en_US/champion.json`
- **Champion Details**: `https://ddragon.leagueoflegends.com/cdn/15.24.1/data/en_US/champion/{championId}.json`
- **Loading Images**: `https://ddragon.leagueoflegends.com/cdn/img/champion/loading/{championId}_0.jpg`
- **Role Icons**: Local assets in `Assets/class/`

See the [official League of Legends Champions page](https://www.leagueoflegends.com/en-ph/champions/) for reference.

## Developer Documentation

### Main Functions

- **`getChampions()`** - Fetches all champions from API
- **`showPage(pageNumber)`** - Renders champions for current page
- **`attachHoverEvents()`** - Handles hover/click interactions with viewport boundary detection
- **`showChampionModal(card)`** - Displays champion modal on mobile
- **`getFullLore(id)`** - Fetches full lore (cached for performance)
- **`setupSearch()`** - Real-time champion search
- **`setupPaginationButtons()`** - Page navigation controls

### Key Features

**Viewport Boundary Detection** (lines 328-360):
Ensures hover cards stay visible by flipping position when near screen edges.

**Responsive Design**:
- Desktop (>991px): Hover cards
- Mobile/Tablet (≤991px): Click-to-modal

**Performance**:
- Lazy loading images
- Lore caching to prevent duplicate API calls
- Client-side search filtering

## Credits

Created by James Carlo for Web Development coursework.

### References & Resources

- [League of Legends Official Champions Page](https://www.leagueoflegends.com/en-ph/champions/)
- [Riot Games Developer Portal](https://developer.riotgames.com/)
- [Data Dragon Documentation](https://developer.riotgames.com/docs/lol#data-dragon)

---

*This website is a student project created for educational purposes only and is not affiliated with Riot Games.*

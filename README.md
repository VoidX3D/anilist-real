# Anime Tracker - Personal Anime List Manager

A personalized anime tracking website built with React, Next.js, and Styled-JSX, featuring AniList-style design and functionality for managing personal anime lists.

## Features

### 🎯 Core Features
- **Personal Anime Lists**: Track anime for up to 5 users
- **AniList-Style Design**: Beautiful, responsive UI matching AniList's aesthetic
- **Anime Detail Pages**: Comprehensive information pages with all anime details
- **Search Functionality**: Search anime by title, genres, and more
- **Rating System**: Rate anime with a 1-10 scale and detailed descriptions
- **Status Tracking**: Mark anime as Watching, Completed, Planning, Paused, or Dropped
- **Episode Progress**: Track episodes watched for ongoing series
- **User Profiles**: Individual profile pages showing anime lists and statistics

### 🎨 Design Features
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- **AniList Layout**: Same card format and detail page layout as AniList
- **Modern UI**: Clean, modern interface with smooth animations
- **Dark/Light Theme Support**: CSS variables for easy theming

### 📊 Data Management
- **Local Data Storage**: All data stored locally in JSON files
- **No External APIs**: Completely self-contained after initial setup
- **Scalable Structure**: Support for up to 500 anime entries
- **Season Support**: Different entries for different seasons of the same anime

## Project Structure

```
ANI_TRACK/
├── components/          # React components
│   ├── anime/          # Anime detail page components
│   ├── rootRoute/      # Homepage components
│   ├── UserRating.js   # User rating component
│   ├── mediaCard.js    # Anime card component
│   ├── navbar.js       # Navigation bar
│   └── layout.js       # Main layout component
├── data/               # Local data files
│   ├── anime_1.json    # Anime database part 1 (entries 1-10)
│   ├── anime_2.json    # Anime database part 2 (entries 11-20)
│   ├── anime_3.json    # Anime database part 3 (entries 21-30)
│   ├── ...             # Continue for up to 50 files (500 entries)
│   ├── anime_template.json  # Template for adding new anime
│   └── users.json      # User data and anime lists
├── lib/                # Utility functions
│   ├── localDataService.js  # Data management service
│   └── useWindowDimensions.js
├── pages/              # Next.js pages
│   ├── index.js        # Homepage
│   ├── anime/[id].js   # Anime detail pages
│   └── user/[id].js    # User profile pages
└── public/             # Static assets
    └── images/         # Anime cover images
```

## Setup Instructions

### Prerequisites
- Node.js (version 14 or higher)
- npm or yarn

### Installation

1. **Clone or download the project**
   ```bash
   cd ANI_TRACK
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Data Setup

The project comes with sample data for 20 anime entries split across multiple files. To add your own anime:

1. **Edit the anime database files**
   - `data/anime_1.json` contains entries 1-10
   - `data/anime_2.json` contains entries 11-20
   - Create `data/anime_3.json`, `data/anime_4.json`, etc. for more entries
   - Use `data/anime_template.json` as a template for new entries
   - Each anime needs: id, title, coverImage, genres, meanScore, etc.

2. **Update the data service**
   - Edit `lib/localDataService.js` to import new anime files
   - Add `import animeData3 from '../data/anime_3.json';` for new files
   - Update the `currentAnimeData` array to include new data

3. **Edit `data/users.json`**
   - Modify user information and anime lists
   - Add anime to user lists with status, score, and notes

## Usage

### Homepage
- Browse featured anime sections
- Search for anime using the search bar
- Click on anime cards to view details

### Anime Detail Pages
- View comprehensive anime information
- Select a user from the dropdown
- Add anime to your list with status and rating
- Track episode progress

### User Profiles
- Navigate to `/user/1` through `/user/5` to view user profiles
- Filter anime by status (Completed, Watching, etc.)
- Sort by different criteria (Title, Score, Date Added)
- View user statistics and anime lists

### Rating System
- Rate anime from 1-10 with descriptions
- Add personal notes and thoughts
- Track watching progress
- Mark anime as completed, dropped, etc.

## Data Structure

### Anime Entry Format
```json
{
  "id": 1,
  "title": {
    "english": "Death Note",
    "romaji": "Death Note",
    "native": "デスノート"
  },
  "coverImage": {
    "extraLarge": "/images/anime/death-note.jpg",
    "large": "/images/anime/death-note.jpg",
    "medium": "/images/anime/death-note.jpg",
    "color": "#2e51a2"
  },
  "genres": ["Mystery", "Psychological", "Supernatural"],
  "meanScore": 85,
  "popularity": 1000000,
  "format": "TV",
  "episodes": 37,
  "season": "FALL",
  "seasonYear": 2006,
  "status": "FINISHED",
  "description": "Anime description..."
}
```

### User Anime List Entry
```json
{
  "animeId": 1,
  "status": "COMPLETED",
  "score": 9,
  "episodesWatched": 37,
  "notes": "Amazing psychological thriller!",
  "dateAdded": "2024-01-15",
  "dateCompleted": "2024-01-20"
}
```

## Customization

### Adding More Anime
1. Edit `data/anime.json`
2. Add new entries following the existing format
3. Include cover images in `public/images/anime/`
4. Update user lists in `data/users.json`

### Modifying Users
1. Edit `data/users.json`
2. Change usernames, display names, and avatars
3. Add/remove anime from user lists
4. Update ratings and status

### Styling Changes
- Modify CSS in component files
- Update color variables for theming
- Adjust responsive breakpoints

## Technologies Used

- **Frontend**: React 16.13.1, Next.js 9.4.4
- **Styling**: Styled-JSX (CSS-in-JS)
- **Data**: Local JSON files
- **Routing**: Next.js file-based routing
- **State Management**: React hooks (useState, useEffect)

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Performance

- Optimized for fast loading
- Responsive images
- Efficient data queries
- Minimal external dependencies

## Future Enhancements

- [ ] Add more anime entries (up to 500)
- [ ] Season-specific anime entries
- [ ] Advanced filtering options
- [ ] Export/import functionality
- [ ] Dark mode toggle
- [ ] Mobile app version

## Contributing

This is a personal project, but suggestions and improvements are welcome!

## License

This project is for personal use and learning purposes.

---

**Note**: This project uses local data storage and doesn't require any external APIs or databases. All anime information is stored locally in JSON files for complete privacy and offline functionality. "# anilist-real" 

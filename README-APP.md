# Mushroom Spot Clone

A fully functional mushroom foraging app inspired by MushroomSpot.io. Find, track, and identify mushrooms with an interactive map, species guide, and private spot tracker.

## Features ✨

### 🗺️ **Interactive Map**
- Community finds from other foragers (sample data)
- Your private spots saved in browser
- Click any marker to see details
- Find your current location
- Zoom controls

### 🍄 **Species Guide**
- Browse 10+ mushroom species
- Edibility status (Edible, Toxic, Inedible)
- Habitat information
- Latin names

### 📅 **Seasonality Calendar**
- See when each species is in season
- Month-by-month availability
- Currently active species highlighted with 🔥

### 📍 **My Spots Tracker**
- Save mushroom finds with location
- Add quantity and notes
- Stores locally in your browser
- Persists between sessions
- Delete individual spots

### 🔍 **Search**
- Search community finds by species name
- Real-time filtering

## How to Use

1. **Open the app**: Open `mushroom-app.html` in your browser
   - Direct: `file:///path/to/mushroom-app.html`
   - Or serve with: `python -m http.server 8000`

2. **View Community Finds**: The map shows where other foragers found mushrooms (sample data)

3. **Browse Species**: Click "Species" tab to see the species guide with info and edibility

4. **Check Seasons**: Click "Season" tab to see when mushrooms are available year-round

5. **Save Your Spots**:
   - Click "My Spots" tab
   - Center the map where you found mushrooms
   - Fill in the form with species, quantity, and notes
   - Click "Save Location"
   - Your spot will appear on the map in blue

## Data Storage

- **Community finds**: Hardcoded sample data (can be replaced with API)
- **Your spots**: Saved in browser's localStorage (survives page reloads, clearing browser data will delete)

## Customization

### Add Real Community Data
Replace the `SAMPLE_FINDS` array with data from:
- iNaturalist API (free)
- Your own backend database
- CSV/JSON import

### Add More Species
Edit the `MUSHROOM_SPECIES` array in the HTML file:
```javascript
{ name: "Species Name", latin: "Latin name", edibility: "edible|toxic|inedible", season: [1,2,3...], ... }
```

### Connect a Backend
Currently works standalone. To add backend:
1. Set up a database (Firebase, Supabase, MongoDB)
2. Replace localStorage with API calls
3. Add user authentication
4. Share finds with the community

## Files

- **mushroom-app.html** - Main app (all-in-one file)
- **index.html** - Original Mushroom Radar (still available)
- **script.js** - Mushroom Radar JavaScript
- **style.css** - Mushroom Radar styles
- **sw.js** - Service worker for offline support
- **manifest.webmanifest** - PWA configuration

## Tech Stack

- Leaflet.js for mapping
- Vanilla JavaScript (no frameworks)
- LocalStorage for persistence
- Responsive CSS Grid layout

## Next Steps

- [ ] Add photo upload/camera integration
- [ ] AI identification (Vision API)
- [ ] Backend database
- [ ] User authentication
- [ ] Community sharing
- [ ] Notifications for best seasons
- [ ] Weather integration
- [ ] Offline map tiles

## License

Free to use and modify!

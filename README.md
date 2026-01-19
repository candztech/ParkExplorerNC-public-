# Park Explorer

A comprehensive iOS app for exploring and tracking visits to state parks. Browse parks, view detailed information, track your visits, and discover trails.

## Features

### 📊 Overview Dashboard
- Quick statistics on total parks, visited parks, and favorites
- Progress tracking with visual indicators
- Milestone achievements for exploration goals
- At-a-glance summary of your park exploration journey

### 📋 Parks List
- Browse all available state parks
- Search and filter functionality
- Sort by various criteria (name, acreage, region, etc.)
- Quick access to park details
- Mark parks as favorites or visited directly from the list

### 🗺️ Interactive Map
- View all parks on an interactive map
- Tap park markers to see quick details
- Navigate to park locations
- Visual overview of park distribution across regions

### ✓ Visited Parks Tracker
- Track which parks you've visited
- View visit history with dates
- Manage your visited parks collection
- Progress toward visiting all parks

### ℹ️ Park Details
- Comprehensive information for each park including:
  - Location and contact details
  - Acreage and region information
  - Available trails with difficulty ratings
  - Website links for additional information
  - Directions and navigation support

### 🥾 Trail Information
- Detailed trail data for each park
- Trail length and difficulty ratings
- Trail types (loop, out-and-back, etc.)
- Trailhead locations with map integration

## Technical Details

### Architecture
- **SwiftUI** for modern, declarative UI
- **MVVM Pattern** with observable data management
- **MapKit** integration for mapping features
- **Combine** framework for reactive data flow
- **UserDefaults** for lightweight persistence

### Data Management
- CSV-based data storage for parks and trails
- Efficient parsing and caching
- Real-time status tracking (favorites, visits)
- Error handling with retry capabilities

### Code Organization
```
├── Views/
│   ├── ContentView.swift          # Main tab view
│   ├── OverviewView.swift         # Dashboard
│   ├── ParksListView.swift        # Park listing
│   ├── ParksMapView.swift         # Map interface
│   ├── VisitedParksView.swift     # Visit tracking
│   └── InfoView.swift             # App information
├── Data/
│   ├── ParksDataManager.swift     # Data management
│   ├── CSVParser.swift            # Data parsing
│   └── Models.swift               # Data models
└── Resources/
    └── CSV data files
```

## Requirements

- iOS 17.0+
- Xcode 15.0+
- Swift 5.9+

## Installation

1. Clone the repository
2. Open the `.xcodeproj` file in Xcode
3. Build and run on your iOS device or simulator

## Data Structure

### Park Data
The app expects park data with the following fields:
- Name
- Location (latitude, longitude, address)
- Contact information (phone, website)
- Park characteristics (acreage, region, county)
- Metadata (IDs, last updated)

### Trail Data
Trail information includes:
- Associated park name
- Trail name and length
- Difficulty level
- Trail type
- Trailhead coordinates
- Metadata

## Usage

### Marking Parks as Visited
1. Navigate to a park in any view
2. Tap the checkmark icon to mark as visited
3. Visit date is automatically recorded
4. Track your progress in the Overview tab

### Adding Favorites
1. Browse to any park
2. Tap the heart icon to add to favorites
3. Quickly access favorites from filtered lists

### Exploring Trails
1. Select a park from the list or map
2. View detailed park information
3. Browse available trails with difficulty ratings
4. Access trailhead locations on the map

### Tracking Progress
- View overall statistics in the Overview tab
- Monitor milestone achievements (25%, 50%, 75%, 100%)
- See visited vs. unvisited parks at a glance

## Customization

The app is designed to be easily adaptable for different park systems:

1. **Update Data Sources**: Replace CSV files with your region's park data
2. **Modify Branding**: Update app name and titles in `ContentView` and info views
3. **Adjust Fields**: Customize `Models.swift` to match your data structure
4. **Update Parser**: Modify `CSVParser.swift` for different CSV formats

## Privacy

All user data (favorites, visit tracking) is stored locally on the device using UserDefaults. No data is transmitted to external servers.

## Logging

The app uses unified logging system (OSLog) with categorized loggers:
- App lifecycle events
- Data loading and parsing
- User interactions
- Error conditions

## Performance Considerations

- Efficient CSV parsing with error handling
- Lazy loading of views and data
- Optimized map annotations
- Minimal UserDefaults usage for fast persistence

## Future Enhancements

Potential features for expansion:
- Photo uploads for visited parks
- Sharing visited parks with friends
- Offline map support
- Trail condition reports
- Park amenities database
- Weather integration
- Custom notes for each park visit

## Contributing

Contributions are welcome! Please follow these guidelines:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request with a clear description

## License

[Specify your license here]

## Credits

Park and trail data sourced from official state park systems.

## Support

For questions or issues, please [specify contact method or issue tracker].

---

Built with ❤️ using SwiftUI

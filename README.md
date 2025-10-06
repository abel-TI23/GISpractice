# Assignment 3: Coordinate Systems Comparison

## 📁 Files Created

### 1. `mercator-map.html` - Web Mercator (EPSG:3857)
- **Standard web mapping projection**
- Used by Google Maps, OpenStreetMap, most web services
- Preserves shapes locally, good for navigation
- Distorts areas significantly near poles

### 2. `epsg4326-map.html` - Geographic WGS84 (EPSG:4326)
- **Geographic coordinate system**
- Uses pure latitude/longitude coordinates
- Global coverage without coordinate distortion
- May appear "stretched" horizontally (this is normal!)

## 🗺️ Features on Both Maps

### Data Points:
- 🏠 **Home** - Personal residence
- 🎓 **NusaPutra Campus** - Educational institution  
- 🍞 **Vos Bakery** - Local food establishment
- 🏥 **Emergency Medical Clinic** - Healthcare facility (GeoJSON point)

### Vector Data:
- **Markers** - Point locations with popups
- **Polyline** - Walking route connecting locations
- **Polygon** - Campus area boundary
- **GeoJSON** - Emergency clinic with detailed properties

## 🎯 Key Differences

### Web Mercator (EPSG:3857):
- **Coordinates**: Projected meters from equator
- **Appearance**: Normal rectangular appearance
- **Usage**: Web mapping, navigation, local analysis
- **Distortion**: Minimal locally, extreme at poles

### Geographic WGS84 (EPSG:4326):
- **Coordinates**: Decimal degrees (latitude, longitude)
- **Appearance**: May look horizontally stretched
- **Usage**: GPS, global datasets, coordinate storage
- **Distortion**: None in coordinate values, visual stretching

## 🔍 Interactive Features

- **Click any map** to see coordinates in respective projection
- **Navigation buttons** to switch between maps
- **Popups** showing projection information
- **Scale controls** for distance measurement

## 📝 Technical Notes

### EPSG:4326 Implementation:
- Uses Proj4 library for coordinate transformations
- Custom CRS (Coordinate Reference System) definition
- Proper zoom levels and bounds for geographic projection
- May appear stretched - this is correct behavior!

### Data Consistency:
- Same coordinate data used on both maps
- Coordinates automatically transformed by projection
- All features maintain spatial relationships

## 🎓 Educational Value

This comparison demonstrates:
1. **How different projections affect map appearance**
2. **Coordinate system transformations**
3. **Real-world applications of each projection**
4. **Technical implementation of custom CRS in web mapping**

## 🚀 How to Use

1. Open `mercator-map.html` to see Web Mercator version
2. Click "Switch to EPSG:4326 Map" to see geographic version
3. Click on maps to see coordinate differences
4. Compare how the same data appears in different projections

Both maps should display correctly with all features visible!

# Mapbox Tile Grabber

Generate custom map tile images with boundary box. 

Mapbox Tile Grabber was created as an internal dev utility. It is not recommended that your instance of Mapbox Tile Grabber be publicly accessible.

![Screenshot-MapboxTileGrabber.png](https://raw.github.com/sarahcassady/mapbox-tile-grabber/master/Screenshot-MapboxTileGrabber.png)

## Requirements

A Mapbox account is required in order to use the Mapbox API.

## Getting Started

### Install

`index.html` can be opened from file in a browser, but an internet connection is still required to communicate with your Mapbox account.

Mapbox Tile Grabber provides two ways to save a generated tile due to limited browser support for the javascript `download` attribute. [Check current browser suppot here.](http://caniuse.com/#feat=download)

### Configure Mapbox API

Add your map ID.

```javascript
// Mapbox Map ID
var mID = 'yourusername.yoursavedmapid';
```

### Set Map Defaults

Set the map's initial center coordinates and zoom level.

```javascript
// load map with center at lat/lng
var lat = 37.52041; 
var lng = 23.4795;
var defaultZoom = 14;
```

Set the hight and width of the `#map` element to control both the size of the map in-browser and the size of the generated PNG. 

```css
/* size of map onscreen and generated png */
#map { width: 1024px; height: 1024px; } 
```

Customize tile filename.

```javascript
// filename prefix
var filePrefix = 'Poros'
// filename format
var fileName = filePrefix+' ('+mapBounds._southWest.lng+', '+mapBounds._southWest.lat+', '+mapBounds._northEast.lng+', '+mapBounds._northEast.lat+').png';
```

## More Information

### Third Party Components

Full documentation on the libraries used to create this tool:

* [Mapbox mapping platform](https://www.mapbox.com)
* [Leaflet interactive maps library](https://github.com/Leaflet/Leaflet)
* [leaflet-image map image export library](https://github.com/mapbox/leaflet-image)

### Attribution

Mapbox Tile Grabber adheres to the attribution polices of all third part components. Read these policies before modifying this code or using any of the custom map tiles you generate with this tool.

* [Mapbox attribution policy](https://www.mapbox.com/help/attribution)
* [Leaflet attribution policy](https://github.com/Leaflet/Leaflet/blob/master/FAQ.md#commercial-use-and-licensing)
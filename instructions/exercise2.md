# Vector tiles with Mapbox GL JS
- Head to http://bit.ly/mapbox-gl-js-basic in a new tab.
- View the page’s source code: right-click anywhere, then click "View Page Source."
- You can use code you see as a guide, along with the instructions below. It's very common to look at code you already know works in order to help you solve problems when you are coding your own page!

### Initialize your first Mapbox GL JS map
1. Fire up your text editor. In the labs we have Visual Studio Code (aka “VS Code”), which we will reference here. However, you can use any editor you like at home (or on your own machine). Two we discussed in class are [Webstorm](https://www.jetbrains.com/webstorm/), which some students have liked or [Atom](https://atom.io/) + [Github desktop](https://desktop.github.com/), which Shadrock uses. Web mappers rely heavily on their text editors to get stuff done. We’re going to use ours a lot during this class.
2. If you're using Atom, then simply clone the repo. In VS Code, download the repo and add the folder to your Workspace: From the File menu, click Add Folder to Workspace, then navigate to today’s class folder on your computer and click Add.
3. Open `Mapbox-gl-js-cwm.html`
---
##### 4. Add Mapbox GL JS and CSS Files
![image](images/slide74.png)
```html
<!-- Add Mapbox GL JS JavaScript file -->
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v1.5.0/mapbox-gl.js'></script>

<!-- Add in the Mapbox GL JS CSS file -->
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v1.5.0/mapbox-gl.css' rel='stylesheet' />
```

##### 5. Set the size for map
![image](images/slide75.png)
```html
       body {
           margin: 0;
           padding: 0;
       }
       #mapId {
           position: absolute;
           top: 0;
           bottom: 0;
           width: 100%;
       }
```

##### 6. Create div element that contains the map
![image](images/slide76.png)

```html
 <div id="mapId"></div>
```
##### 7. Grab your default Mapbox Access Token [here](https://account.mapbox.com/access-tokens/)
![image](images/slide77.png)

```html
<script>
// Mapbox GL JS requires a token
mapboxgl.accessToken = 'your token goes here’;
      
// Initialize the map
var map = new mapboxgl.Map({
container: 'mapId', 
style: 'mapbox://styles/mapbox/streets-v11', 
center: [-122.420790, 37.754700], 
zoom: 14 
});
</script>
```

##### 8. Save your changes and load your page

### What’s different about Mapbox GL JS vs Leaflet?
![image](images/slide80.png)

## Additional Resources
- [Mapbox GL JS documentation](https://docs.mapbox.com/mapbox-gl-js/api/)

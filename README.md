# Assets-Preloader
Preload assets in background (only images)


# Usage
```
var assets = [ 'img001.png', 'img002.png', 'img003.png' ];

var assetsPreloader = new AssetsPreloader();                 // Single initialize
var assetsPreloader = new AssetsPreloader( assets );         // Initialize passing the assets in the constructor

assetsPreloader.loadAsset( 'img001.png' );                   // Load sigle asset
assetsPreloader.loadAssets( assets );                        // Load multiple assets

assetsPreloader.onAssetsLoaded( function ( event ) {         // On assets loaded event
    console.log('DONE!');
    console.log(assetsPreloader.downloadQueue);
    var img = assetsPreloader.getAsset( 'img003.png' );      // Get loaded asset
    document.body.appendChild( img );   
});
```
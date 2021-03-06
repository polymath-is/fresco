# fresco

Fresco is an open source [Mapbox Vector Tile Style](https://docs.mapbox.com/mapbox-gl-js/style-spec) editor that allows cartographers to craft stylesheets for use with [Mapbox GL](https://docs.mapbox.com/mapbox-gl-js/api/) maps. Unlike other style editors, Fresco does not attempt to hide the complexity of Mapbox GL Styles but rather exposes an interactive JSON code editor to allow for maximum control and flexibility. This allows the user to implement more complex styles concepts like data driven styles with [expressions](https://docs.mapbox.com/help/tutorials/mapbox-gl-js-expressions/). When using Fresco, it may be helpful to have the [Mapbox Style Spec](https://docs.mapbox.com/mapbox-gl-js/style-spec/) available as a reference.

Styles created and modified with Fresco are saved to the browser's local storage and are auto-saved on changes.

Give it a try: [https://fresco.gospatial.org/](https://fresco.gospatial.org/)

![map editing screen shot](/docs/img/osm-screenshot.png)

## Features

- Interactive JSON code editor.
- Style editor for Mapbox GL styles.
- Mapbox GL layer style expression editor.
- Auto save on changes.
- Styles persisted to local storage (in the browser).
- Mapbox GL style error parser. Displays the error at the error location in the style.
- Integrated Mapbox GL style spec attributes (info on style fields).
- Custom domain header configurations. Useful for domains which require `Authorization` headers. 

## Usage

Fresco may be used in the browser by visiting [https://fresco.gospatial.org/](https://fresco.gospatial.org/) or by downloading a pre compiled binary from the [releases](https://github.com/go-spatial/fresco/releases) page.

## Running from source

Fresco is built on top of React. To run Fresco from source use the following steps:

1. Download the latest version of [Node.js](https://nodejs.org/en/download/)
2. Clone this repository to your computer
3. Navigate to this repo on your computer
4. Run `npm install`
5. To startup, run `npm start` - Fresco should open in a browser window
6. To build Fresco for deployment run `npm run build` - the deployment files will be inside the `/build` directoty

## Hosting Fresco from a subdirectory

Fresco is able to be hosted from a subdirectory of a domain (i.e. https://yourhost.com/fresco/). To enable this functionality, modify the `package.json` file


```
{
  "name": "fresco-app",
  "version": "0.1.0",
  "private": true,
  "homepage": "/fresco",
...

```

Then use `npm run build` to build Fresco for deployment.

## Contributing

Contributions are welcome! Fork the repo and send in a PR with any bug fixes or features.

## Looking for a vector tile server?

If you're looking to create vector tiles that can be styled with Fresco, check out [tegola](https://github.com/go-spatial/tegola)!

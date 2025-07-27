# Product Feature Map Tool

This project provides an interactive "Product-Feature Relationship Map" that lets you visualize connections between products and their features. It is implemented as a single HTML file.

## Opening `index.html`

1. Clone or download this repository.
2. Open `index.html` in any modern web browser by double-clicking the file or serving it through a simple HTTP server.

The application loads libraries from CDNs, so an active internet connection is required when opening the file.

## Exporting Maps

Use the buttons in the top bar to export your map as **PNG** or **PDF**. The PDF format can be imported into tools like **Lucidchart**.

## Dependencies and Browser Requirements

The page relies on several libraries delivered via CDN:

- **vis-network** for graph visualization
- **PapaParse** for reading and writing CSV files
- **Tailwind CSS** for styling

Because the script uses modern JavaScript features such as `crypto.randomUUID()`, a recent version of Chrome, Firefox, Edge or Safari is recommended. When this API is unavailable, the tool falls back to a small helper that generates UUIDs using `crypto.getRandomValues` (or `Math.random` as a last resort). A modern browser is still advised. No additional installation is necessary beyond a web browser with internet access.

## Deploying to Heroku

This site can be served on Heroku using the [NGINX buildpack](https://github.com/heroku/heroku-buildpack-nginx). Add the buildpack and deploy with:

```bash
heroku buildpacks:set heroku-community/nginx
```

The repository already includes `config/nginx.conf.erb` with a minimal configuration. A `static.json` file is also present for compatibility with hosts that use it, but it isn't required when deploying via the NGINX buildpack.

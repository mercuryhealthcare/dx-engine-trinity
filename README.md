# dx-engine-trinity
Front-end extended assets for Trinity Health Websites


## Purpose

Allow Trinity Health Development team to ingest a private NPM repository containing both Trinity-specific and DX Engine CSS / JS assets (also known as the DX component libary).

This Github repository provides a framework for extending the DX component library and for adding new front-end components. Any distribution-ready JavaScript and CSS files should be added to the **dist** folder in the root of this repository.

Distribution-ready assets are readily available to be fetched via jsdelivr CDN and added to any Trinity website running on DX Engine.

Example jsdelivr CDN assets:

- [https://cdn.jsdelivr.net/gh/mercuryhealthcare/dx-engine-trinity@latest/dist/index.css](https://cdn.jsdelivr.net/gh/mercuryhealthcare/dx-engine-trinity@latest/dist/index.css)
- [https://cdn.jsdelivr.net/gh/mercuryhealthcare/dx-engine-trinity@latest/dist/index.js](https://cdn.jsdelivr.net/gh/mercuryhealthcare/dx-engine-trinity@latest/dist/index.js)

## JsDelivr documentation

GitHub
------
We recommend using npm for projects that support it for better UX - npm packages are searchable on our website, and package pages show additional useful information, such as descriptions and links to homepages.

We use a permanent S3 storage to ensure all files remain available even if GitHub goes down or a repository or a release is deleted by its author. Files are fetched directly from GitHub only the first time or when S3 goes down.

##### Load any GitHub release, commit, or branch:

```
/gh/user/repo@version/file
```

##### Load exact version:

```
/gh/jquery/jquery@3.1.0/dist/jquery.min.js
/gh/jquery/jquery@32b00373b3f42e5cdcb709df53f3b08b7184a944/dist/jquery.min.js
```

##### Use a version range instead of an exact version (only works with valid [semver versions][15]):

```
/gh/jquery/jquery@3/dist/jquery.min.js
/gh/jquery/jquery@3.1/dist/jquery.min.js
```
---
**NOTE**
If you use this feature and a file you requested is not available in the newest release, the link will keep working thanks to our version-fallback feature. We'll continue to serve the file from older release instead of failing with a 404 error.

---

##### Omit the version completely or use "latest" to load the latest one (only works with valid [semver versions][15]): (not recommended for production usage)

*Falls back to the `master` branch if there are no tagged releases.*

```
/gh/jquery/jquery@latest/dist/jquery.min.js
/gh/jquery/jquery/dist/jquery.min.js
```
---
**NOTE**
Requesting the latest version (as opposed to "latest major" or "latest minor") is dangerous because major versions usually come with breaking changes. Only do this if you really know what you are doing.

---


##### Add ".min" to any JS/CSS/SVG file to get a minified version - if one doesn't exist, we'll generate it for you. All generated files come with source maps and can be easily used during development:

```
/gh/jquery/jquery@3.2.1/src/core.min.js
```
---
**NOTE**
Minifying a large file can take several seconds. However, we store all generated files in our permanent storage, so this delay only applies to the first few requests.

---

##### Get a directory listing:

```
/gh/jquery/jquery@3.1.0/
/gh/jquery/jquery@3.1.0/dist/
```

##### Complete documentation for JsDeliver:

- [Documentation](https://www.jsdelivr.com/documentation)

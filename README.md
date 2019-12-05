Creating a Progressive Web App using Workbox

https://developers.google.com/web/tools/workbox/guides/generate-service-worker/cli

1. `npm install workbox-cli`
2. `workbox wizard` (setup CLI & config)
3. `workbox generateSW workbox-config.js` (generate service worker)

Add into index.html
````
<script>
    // Check that service workers are supported
    if ('serviceWorker' in navigator) {
        // Use the window load event to keep the page load performant
        window.addEventListener('load', () => {
            navigator.serviceWorker.register('/sw.js');
        });
    }
</script>
````
Create a manifest file and link it in index.html

`<link rel="manifest" href="site.webmanifest" >`

Cache the App
````
 "globPatterns": [
    "**/*.{html,js,ico,webmanifest}"
  ],
````

# learn-js-optimizations

We can divide optimizations in 2 groups: Network and Runtime

## Network Optimizations ##

1. Lazy loading

2. Minification / Dead Code Elimination (HTML, JS, CSS)

Code is minified, comments, white spaces and new lines are removed from production files.

4. Compression

Brotli, gzip

5. Pre-fetching Resources (preload, prefetch, preconnect, dns-prefetch, prerender)
- preload: download and cash asap (for resources now)
- prefetch: download and cash on idle (for next page resources)
- dns-prefetch: resolve dns before
- preconnect: connect to domain before
- prerender: asks browser load url address and prerender it on "invisible tab" (you know that user will go to this page)


6. Bundling

Reduce the number of requests that the browser needs to perform in order to deliver the application requested by the user.

7. Service workers

8. Caching

9. CDN

10. Images optimizations
- Compress
- Use SVG (Vector images (SVG) tend to be smaller than images and SVG's are responsive and scale perfectly. These images can be animated and modified by CSS)
- Set width / height
- Responsive images in according to client screen size
- Спрайты

11. Non-blocking JS
async / defer (JavaScript blocks the normal parsing of the HTML document, so when the parser reaches a `<script>` tag (particularly is inside the `<head>`), it stops to fetch and run it)
- **async**: async downloading + execute immediately (blocking html parsing)
    use when script doesn't manipulate DOM
- **defer**: async downloading + execute after parsing (after DOMContentLoaded event) (non-blocking html parsing)
    use when script manipulates DOM

12. Check dependencies size

13. Advanced preloading techniques (viewport, IntersectionObserver)


## Runtime Optimizations ##

1. Web Workers

2. Tree shaking

3. Animations
- will-change: transform
- requestAnimationFrame()

4. Reduce DOM size

5. 




## Resources
- https://3perf.com/talks/web-perf-101/
- https://habr.com/ru/articles/445264/
- https://github.com/mgechev/angular-performance-checklist
- https://nitropack.io/blog/post/critical-rendering-path-optimization
- https://deepu.tech/memory-management-in-v8/ (stack)

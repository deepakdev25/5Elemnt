# SentinelQA

SentinelQA is a static, browser-only showcase for turning acceptance criteria into UI checks against its built-in demo storefront.

## Run the demo

- Open `index.html` or `page.html` in a browser.
- For Netlify, publish the repository root; no build command or environment variables are required.
- Keep the local assets beside the HTML files: `sentinel-design.css`, `sentinel-scene.js`, `three.min.js`, and `html2canvas.min.js`.

## Try the workflows

1. Edit the sample ticket's acceptance criteria and generate checks.
2. Set a demo product price to match a price criterion, then run the checks. A mismatched price should fail; price changes are not self-healed.
3. Use **Simulate locator drift** to change the add button's ID and label. Run the tests to see an unambiguous locator repair recorded in the report.
4. Export the run report as JSON.
5. In **Bonus demos**, preview a mock Jira comment, capture and compare storefront screenshots, or run five repeated checks with optional injected intermittent failures.

## Demo limitations

The ticket, storefront, locator drift, Jira update preview, and flaky failures are all local demonstrations. No request is sent to Jira, no arbitrary external application is controlled, and no credentials are used. Visual comparison captures only the built-in storefront. Testing other projects requires a separately configured browser runner; real Jira updates require a secure integration.

Three.js and html2canvas are included as local browser assets. Their license notices are in `THREE-LICENSE.txt` and `HTML2CANVAS-LICENSE.txt`.

# Hiradparsbot Dictionary — Documentation

Hiradparsbot Dictionary is a lightweight, responsive landing page for Hiradparsbot with an embedded English–Persian and Persian–English word lookup tool. The dictionary opens in a floating panel at the bottom-right of the page, so users stay on the landing page.

## Screenshots

### Landing page
![Hiradparsbot landing page](images/hiradparsbot-home.jpg)

### Dictionary panel
![Hiradparsbot dictionary panel](images/hiradparsbot-dictionary.jpg)

## Features
- Single-page responsive design with a dark-blue and turquoise color palette.
- Floating dictionary launcher at the bottom-right corner.
- Opens and closes in place without page navigation.
- Automatic Persian/English input detection, plus a manual direction switch.
- English-to-Persian lookup with available meanings, parts of speech, definitions and examples.
- Persian-to-English lookup with selectable English matches.
- Copy results and pronunciation playback through available browser capabilities.

## Deploy with GitHub Pages
1. Keep `index.html` in the repository root.
2. Open **Settings → Pages** in the GitHub repository.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose branch `main` and folder `/(root)`, then save.
5. GitHub displays the published Pages URL in the same settings screen.

## Vocabulary source and runtime behavior
The page uses the public API of the open-source [Openjam project](https://github.com/amirj4m/openjam):

`https://openjam.amirj4m.com/v1`

The vocabulary database is not vendored into this repository. The page sends lookup requests to the public Openjam API at runtime. Dictionary availability therefore depends on the upstream API remaining online and on its service policies. Openjam's API documentation specifies a limit of 60 requests per minute per IP.

This is a word dictionary, not a general-purpose sentence translator. A lookup may return no result when a word or Persian meaning is not present in the source dataset. Translation quality and completeness depend on the upstream data.

## Requirements and costs
- No Google Cloud project, Billing setup, API key, or project-specific Cloudflare Worker is required for word lookup.
- An internet connection is required to query the public Openjam API.
- The API is operated by the Openjam project, not by this repository; uptime and limits are outside this project's control.

## License and attribution
Openjam states that its project and dataset are released under the MIT License. The source copyright notice and license text are included in [`../OPENJAM-LICENSE.txt`](../OPENJAM-LICENSE.txt). Preserve the notice and license when redistributing relevant materials.

- Upstream repository: https://github.com/amirj4m/openjam
- API integration guide: https://github.com/amirj4m/openjam/blob/main/INTEGRATION.md

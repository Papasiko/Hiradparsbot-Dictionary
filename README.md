# Hiradparsbot Dictionary

A lightweight Persian–English / English–Persian dictionary page for **Hiradparsbot**, built as a static website and designed for GitHub Pages.

**فارسی:** [راهنمای فارسی](docs/fa.md) · **English:** [English documentation](docs/en.md)

## Preview

| Landing page | Dictionary widget |
|---|---|
| ![Hiradparsbot landing page](docs/images/hiradparsbot-home.jpg) | ![Hiradparsbot dictionary widget](docs/images/hiradparsbot-dictionary.jpg) |

## Features

- Single-page, responsive landing page with a blue and turquoise visual theme.
- Floating dictionary launcher in the bottom-right corner; the dictionary opens without navigating away.
- Automatic Persian/English input detection, with a manual direction switch.
- English-to-Persian word lookup with available meanings, parts of speech, definitions, examples and pronunciation details.
- Persian-to-English lookup with selectable English matches.
- Copy results and use browser speech synthesis where supported.
- No Google Cloud Billing account, translation API key, or project-specific backend is required for dictionary lookup.

## Quick start

1. Keep `index.html` in the repository root.
2. Open **Settings → Pages** on GitHub.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`, then save.
5. Open the GitHub Pages URL shown in the Pages settings.

## Dictionary data and service

The page queries the public Openjam API at `https://openjam.amirj4m.com/v1`. It does not download the whole vocabulary database into this repository. Search results therefore depend on the availability and policies of that independent API service.

The Openjam project documents an MIT-licensed English vocabulary dataset with Persian translations. Its API documentation states a per-IP limit of 60 requests per minute. This is a word dictionary, not a general-purpose sentence translation service; results depend on the entries and translations available in the dataset.

- Dataset/API project: https://github.com/amirj4m/openjam
- API integration guide: https://github.com/amirj4m/openjam/blob/main/INTEGRATION.md
- License: see [`OPENJAM-LICENSE.txt`](OPENJAM-LICENSE.txt)

Please retain the Openjam copyright and license notice when redistributing the bundled integration or data-derived materials.

## Project structure

```text
.
├── index.html
├── README.md
├── OPENJAM-LICENSE.txt
└── docs/
    ├── en.md
    ├── fa.md
    └── images/
        ├── hiradparsbot-home.jpg
        └── hiradparsbot-dictionary.jpg
```

## License

The Hiradparsbot page code is provided for this project. The Openjam dataset/API has its own MIT license; see `OPENJAM-LICENSE.txt` and the upstream repository for attribution and terms.

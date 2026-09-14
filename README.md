# my-app

A small static web app that displays a greeting and its author. It uses only
HTML and CSS, so it can be deployed directly to Cloudflare Pages without a
build step.

## What It Shows

- **Title:** `Hello World!`
- **Text:** `I'm Hyemin Lee`

## Project Structure

```text
.
├── index.html   # The complete page: markup, styles, and explanatory comments
└── README.md    # Project notes and deployment instructions
```

## Run Locally

Because this is a static site, no package installation is required.

1. Open `index.html` directly in a browser, or
2. Start a local server from this folder:

	```bash
	python3 -m http.server 8000
	```

	Then visit <http://localhost:8000>.

## Deploy With Cloudflare Pages

After pushing this project to the GitHub `my-app` repository:

1. Open **Workers & Pages** in the Cloudflare dashboard.
2. Select **Create application** and choose **Pages**.
3. Choose **Connect to Git** and select the GitHub `my-app` repository.
4. Use these build settings:
	- **Framework preset:** None
	- **Build command:** Leave blank
	- **Build output directory:** `/`
5. Select **Save and Deploy**.

Cloudflare Pages will serve `index.html` as the site's home page. Future pushes
to the selected production branch will trigger a new deployment automatically.

## Updating the Page

The page is intentionally kept in one file so small changes are easy to make:

- Change the visible title in the `<h1>` element.
- Change the author message in the `.author` paragraph.
- Change colors and spacing in the CSS variables at the top of the `<style>` block.

The comments in `index.html` explain the purpose of each main section and the
parts most likely to be edited later.


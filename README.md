# Valerie (Yue) Deng — Personal Site

A single-page interactive resume/portfolio. An animated stage with clickable
"ticket" hotspots opens modals for Work Experience, GitHub Projects, Skills,
and Contact info.

## Stack

Plain HTML/CSS/JS, no build step. All media lives in `assets/` and is
referenced by the page — nothing is inlined.

```
index.html   # the site
assets/      # frame images (webp) + intro video (mp4)
```

## Running locally

Any static file server works, e.g.:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html`.

## Deploying (AWS Amplify)

This is a static site with no build step, so Amplify Hosting can serve it
directly:

1. Connect this repo in the Amplify console (or `amplify hosting add` if
   using the Amplify CLI).
2. Skip the build command — there isn't one. Set the build output directory
   to `/` (repo root), since `index.html` lives at the top level.
3. Deploy. Amplify will serve `index.html` and everything under `assets/`.

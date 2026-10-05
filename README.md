# Vikram Rajput site

Static rebuild of [vikramrajpoot.com](https://vikramrajpoot.com). Pages, blog posts, and the assessment form live in this repo. There is no WordPress and no plugin.

## Edit content

- Homepage copy: `src/content/home.json`
- Phone, email, social links: `src/content/settings.json`
- Pages: `src/content/pages`
- Blog posts: `src/content/posts`

After a Netlify deploy, the same files can be edited in the browser at `/admin/`. That editor (Decap CMS) saves straight to git. In the Netlify site settings, enable Identity and Git Gateway, then invite yourself. Locally, run `npm run cms` in one terminal and `npm run dev` in another, then open `http://localhost:4321/admin/`.

## Run locally

```bash
npm install
npm run dev
```

## Deploy on Netlify

1. Push this folder to GitHub.
2. In Netlify, add a new site from that repo.
3. Build command: `npm run build`. Publish directory: `dist`.
4. Enable Identity and Git Gateway so `/admin/` can publish edits.
5. Form submissions from “Book Free Assessment Call” appear under Netlify Forms.

The assessment form posts to `/thank-you/`.

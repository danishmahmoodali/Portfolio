# Danish — Data Portfolio

Personal portfolio site: projects, skills, and an interactive Power BI dashboard gallery.
Single-file static site (`index.html`), no build step, hosted on GitHub Pages.

## Deploy to GitHub Pages (5 minutes)

1. Create a new **public** repo named exactly `YOUR_USERNAME.github.io`
   (e.g. `danish-data.github.io`). This makes the site live at the root URL.
2. Upload `index.html` and this `README.md` to the repo (drag-and-drop on
   github.com works, or `git push`).
3. Go to **Settings → Pages** and confirm the source is
   `Deploy from a branch` → `main` → `/ (root)`.
4. Wait 1–2 minutes. Your site is live at `https://YOUR_USERNAME.github.io`.

> Alternative: name the repo anything (e.g. `portfolio`) and the site lives at
> `https://YOUR_USERNAME.github.io/portfolio` instead.

## Adding your Power BI dashboards (any number — 5, 10, more)

The gallery is driven by the `DASHBOARDS` array in the `<script>` block at the
bottom of `index.html`. Each dashboard is one object:

```js
{
  title: "Sales & revenue overview",
  description: "What it shows + technical highlights (DAX, modeling, etc.).",
  tags: ["DAX time intelligence", "Star schema"],
  embedUrl: ""   // paste your Publish-to-web URL here
}
```

Add or remove entries freely — the selector strip scrolls horizontally, and
only the selected dashboard's iframe is loaded, so 10 dashboards won't slow
the page down.

To get each `embedUrl`:

1. Rebuild the dashboard with **sample or synthetic data only** — never real
   company or client data, even aggregated. Good sources: Contoso,
   AdventureWorks, Kaggle datasets, or Power BI's built-in samples.
2. Publish the report to Power BI Service (app.powerbi.com), into **My workspace**.
3. In the service: **File → Embed report → Publish to web (public)**.
4. Copy only the URL from the generated iframe code
   (it looks like `https://app.powerbi.com/view?r=eyJr...`).
5. Paste it into that dashboard's `embedUrl`. The "coming soon" placeholder
   hides automatically once a URL is present.

Five example entries are pre-filled (sales, operations, HR, marketing,
finance) — rename them to match the templates you actually rebuild.

**If "Publish to web" is greyed out:** your Power BI tenant admin (e.g. the
university's) has disabled it. Options: ask the admin, use a different tenant,
or swap the iframe for a screenshot/GIF of the dashboard (replace the
`<iframe>` with an `<img>` tag).

**Important:** Publish-to-web reports are visible to anyone on the internet —
which is exactly what you want for portfolio pieces built on sample data, and
exactly why real business data must never go through it.

## Customizing

All styling lives in the `<style>` block at the top of `index.html`.
Colors are defined once as CSS variables in `:root` — change `--amber`,
`--cyan`, etc. to retheme the whole site.

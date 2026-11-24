# Danish Mahmood Ali · Data Analyst Portfolio

**Live site:** https://danishmahmoodali.github.io/Portfolio/

I'm a Data Analyst with three years of production reporting at Sead Digital, now doing an M.Sc. in Data Science at Hochschule Fulda. I'm looking for a Werkstudent role or internship in Germany.

This site shows the Power BI reports my clients used most. They are rebuilt with sample data, so no real client data or client names appear anywhere.

## What's on the site

- **Four Power BI reports:** Digital Shelf Availability, Digital Shelf Analytics, Ad Campaign Performance and GCC Ad Spend Monitoring. Each one has a short preview video that plays on hover, and you can load the live, clickable report from the same panel.
- **A case study** (`case-study.html`) on the Availability report, covering the data model, the DAX measure behind its period buttons and the results for the client.
- **Career timeline and impact numbers** from Sead Digital and EZY Business Applications, plus the JUMO team project at HS Fulda.
- **Work outside of reporting:** Geek Haven, the team behind Geek Con, and Backhaul, a co-op horror game I'm designing.
- **English and German versions**, switched with the EN / DE toggle.
- **CV download** (`cv.pdf`).

## Skills shown

Power BI (DAX, data modelling, field parameters, drill-down), SQL, Python, ETL with Microsoft Fabric, automation with Power Automate and Zapier, and machine learning. More projects are on my [GitHub profile](https://github.com/danishmahmoodali?tab=repositories).

## How it's built

It's a static site with no framework and no build step on GitHub. Fonts, styles and scripts are inlined into `index.html`, so the page loads with very few requests.

```
index.html          the main page
case-study.html     Availability report case study
profile.jpg         profile photo
cv.pdf              CV
shots/              report preview videos, poster frames and project images
```

The preview videos are motion graphics made from screen recordings of each report, cropped so no platform branding shows.

## Editing

- **Report text, links and videos:** open `index.html` and search for `const DASHBOARDS`. Each report is one entry with its title, description, tags, Power BI embed URL, poster image and video.
- **German text:** search for `const DE =` in the same file (and `const DASH_DE =` for the report descriptions). Each key matches a `data-i18n` attribute in the page.
- **Images and videos:** replace the file in `shots/` and keep the same name.

Power BI "Publish to web" links are public. Only use them for reports built on sample data.

## Contact

- Email: danishma309@gmail.com
- LinkedIn: https://www.linkedin.com/in/danish-mahmood-ali

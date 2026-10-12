# Azmith Shyne Tafalla, Portfolio

Personal portfolio of Azmith Shyne Tafalla: IT student at the Technological University
of the Philippines, co-founder of RemitWise, Bitget Web3 Builder and Stellar X Builder.

**Live site:** https://azmith-portfolio.vercel.app

A single static page. No framework, no build step, no dependencies. Everything lives in
`index.html`, with the CSS inline. The only external request is the Google Fonts stylesheet
(Archivo and JetBrains Mono).

## Run it locally

```bash
python -m http.server 4321
```

Then open http://localhost:4321. Opening `index.html` directly from the filesystem also works.

## Deploy

Vercel serves this as a static site with no configuration. From this folder:

```bash
npx vercel --prod
```

Or import the repository at https://vercel.com/new, leave the framework preset as
**Other**, leave every build setting empty, and deploy.

## Editing

| What | Where in `index.html` |
| --- | --- |
| Colours | The `:root` block at the top. It holds the dark palette; light is redefined in the two blocks below it |
| Fonts | The Google Fonts `<link>` and the `--sans` / `--mono` variables |
| Hero | `<section class="hero">` |
| RemitWise | `<section class="feature" id="work">` |
| Experience | `<section class="sec" id="experience">` |
| Education | `<section class="sec" id="education">` |
| Credentials | `<section class="sec" id="credentials">` |
| Skills | `<section class="sec" id="skills">` |
| Contact | `<section class="sec" id="contact">` |

The page follows the visitor's system light or dark setting. If you change a colour, change
it in all three places so the two themes stay in sync.

The RemitWise section is deliberately inverted (white on the dark theme, black on the light
one). It is the page's single moment of emphasis, so avoid giving other sections the same
treatment.

## Files

- `index.html`: the whole site
- `photo.png`: portrait used in the hero
- `.vercelignore`: keeps local-only files out of deployments

# What is your Flavor Profile?

A one-page personality test by Swish Robotics. Plain HTML, CSS and JS with no build step.

## Put it on GitHub Pages
1. Create a new public repo, e.g. `flavor-profile`.
2. Upload everything in this folder (`index.html`, `images/`, `fonts/`) to the repo root.
3. Go to Settings > Pages. Under "Build and deployment", choose "Deploy from a branch", then `main` and `/ (root)`. Save.
4. After about a minute the test is live at `https://<your-org>.github.io/flavor-profile/`.

## Swap in the character art
`images/` has temporary character drawings (`cucumber.svg`, `egg.svg` and so on). Replace them with your final art and keep the same names, or edit the `image:` paths in the `PROFILES` block near the top of the `<script>` in `index.html` (for example `images/cucumber.png`). Square images work best because they're cropped to a circle.

Meal pictures live in `images/meals/`. Prep times are set with `prep:` in the same `PROFILES` block.

## Edit copy
All questions, answers, traits, meals, buddies, enemies and quotes live in the `PROFILES` and `QUESTIONS` blocks at the top of the script.

## Sharing
- "Share my profile" opens the phone's share sheet. On laptops it copies a link instead.
- A shared link ends in `#cucumber`, `#egg` and so on, and opens straight to that result with a "Find my profile" button.
- `images/share-card.png` is the link preview image (1200x630). After hosting, change the `og:image` tag in `<head>` to its full URL (for example `https://<your-org>.github.io/flavor-profile/images/share-card.png`), because iMessage and Slack need the full address.

## Dietary answers
Nothing is sent anywhere. At the end of the test, the answers are kept in `window.flavorProfile` in the browser, so hooking up analytics or a form later is a small change.

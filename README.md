# Lockin feedback page

A one-page feedback form for Lockin. Responses are sent to a Google Form.

## Setup

1. Create a Google Form with these questions (choice text must match exactly):
   - Name or Telegram handle: Short answer
   - How often do you use Lockin?: Multiple choice
     `Every day`, `A few times a week`, `Tried it once or twice`, `Haven't tried it yet`
   - Which part is this about?: Checkboxes
     `Focus timer`, `Feed and posts`, `Stats and streaks`, `Leaderboard`, `Buddies and people`,
     `Live rooms`, `Timelapses`, `Design and look`, `Something new`
   - Feedback type: Multiple choice. `Bug`, `Improvement`, `New feature`
   - Suggestion: Paragraph
   - Rating: Linear scale 1 to 5
   Leave every question optional in Google Forms.

2. In the form: ⋮ > Get pre-filled link > fill every question > Get link.
   Copy the form ID (`/d/e/<ID>/viewform`) and each `entry.XXXXXXXXX` into
   the `CONFIG` block at the bottom of `index.html`.

3. Open `index.html` in a browser (or VS Code Live Server) and send a test response.
   Check the form's Responses tab to confirm it arrived.

4. Deploy: push to GitHub and import the repo on Vercel (Framework preset: Other, no build command,
   output directory: root). Or run `npx vercel --prod` from this folder.
   `vercel.json` adds security headers (CSP allows only Google Fonts and docs.google.com).
   On the live site the "Not connected" notice is hidden; it only shows on localhost.

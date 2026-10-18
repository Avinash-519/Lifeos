# LifeOS

LifeOS is a personal schedule, focus timer, Pomodoro, streak, and learning-roadmap tracker. GitHub Pages hosts the app for free; your tracker state is saved in your own browser using `localStorage`.

## Deploy

The GitHub Actions workflow builds and deploys the site whenever changes are pushed to `main`.

1. Open the repository's **Settings → Pages**.
2. Set **Build and deployment → Source** to **GitHub Actions**.
3. Push the project to the `main` branch. The workflow publishes it at <https://avinash-519.github.io/Lifeos/>.

No Supabase project, hosting account, repository secret, or paid service is required.

## Your tracker data

- Schedule, learning topic, course progress, timers, and streaks are saved in `localStorage` in the browser where you use the site.
- The data is not uploaded to GitHub or shared with other visitors. GitHub hosts the app's source and static page, not the contents of your browser storage.
- When LifeOS is open, it automatically downloads one dated `lifeos-backup-YYYY-MM-DD.json` backup per local calendar day to your browser's Downloads folder. Your browser may ask you to allow automatic downloads. The app needs to be open at least once that day for the daily file to be generated.
- Use **Export backup** for an immediate extra copy and **Import backup** to restore or move your tracker to another browser or device.
- The tracker starts with generic schedules and learning goals. Import your backup from the original tracker to restore your own course, current module, completed problems, schedule, and roadmap.
- Do not use local storage for sensitive information; anyone with access to that browser profile can access its saved tracker data.

For local development:

```bash
npm install
npm run dev
```

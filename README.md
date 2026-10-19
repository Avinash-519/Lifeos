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
- **Private Coach** provides rule-based suggestions from your local schedule, focus time, learning queue, roadmaps, and streaks. It runs in your browser; it is not a generative AI model and does not send tracker data to an AI service.
- In Chrome or Edge, select **Choose backup folder** and choose your `Tracker Backup` folder. LifeOS saves today's backup there when you select it, then saves one dated `lifeos-backup-YYYY-MM-DD.json` file on the first app open each local calendar day. Reopening the page or opening another tab that day will not trigger another automatic backup. The folder permission and handle are kept in browser storage; if permission expires, choose **Reconnect backup folder**. The once-daily marker is stored in local storage, so clearing site data or using another browser profile resets it. Browsers without folder access support use their normal Downloads folder instead.
- The app must be opened at least once that day for the automatic backup to be created. Use **Export backup** for an immediate extra download and **Import backup** to restore or move your tracker to another browser or device.
- The tracker starts with generic schedules and learning goals. Import your backup from the original tracker to restore your own course, current module, completed problems, schedule, and roadmap.
- Do not use local storage for sensitive information; anyone with access to that browser profile can access its saved tracker data.

For local development:

```bash
npm install
npm run dev
```

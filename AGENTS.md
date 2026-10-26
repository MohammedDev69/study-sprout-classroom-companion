<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- App data is mock data in src/lib/data.ts (no backend yet); quiz grading lives in src/lib/quiz.ts with tests.
- Shared app chrome (sidebar, mobile bottom nav, notification bell) is AppShell wrapping <Outlet/> in __root; notifications use an in-app context + browser Notification API.
- Offline PWA uses vite-plugin-pwa generateSW (/sw.js), registered only from src/lib/offline.ts, which refuses dev/preview/iframe hosts; pages NetworkFirst, hashed assets CacheFirst.

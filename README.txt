BATTLE ROYALE FRONTEND — connected to live backend

Files to upload to a separate GitHub repository:
- index.html
- background-music.mp3
- success-loop.mp3
- first_sound.mp3

Deploy as a Render Static Site with the repository root as the Publish Directory.
No build command is required.

After Render creates the static site, copy its public URL (https://....onrender.com).
Then update the backend Web Service environment variable FRONTEND_ORIGIN to that exact URL and redeploy the backend. Do not include a trailing slash.

The frontend submits multipart FormData to:
https://battle-royale-registration-system.onrender.com/api/registrations
and reads registration counts from /api/stats.

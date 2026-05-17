Shoaleh 70 — Video Messages
This is a fork of your party video message app with:

PIN changed to 0624.

Welcome message updated for Shoaleh's 70th birthday.

Uploads continue to use the existing Apps Script URL set in index.html.

How to publish via GitHub Desktop (step-by-step)

Install GitHub Desktop from the GitHub website and sign in.

In Finder/Explorer, create a new folder and put index.html, styles.css, and README.md inside.

Open GitHub Desktop, go to File → Add local repository → Choose…, select the project folder, then click Add repository.

In GitHub Desktop, type a commit message like "Initial commit — Shoaleh 70 app" and click Commit to main.

Click Publish repository, choose the new repo name shoaleh-70-video-messages (or accept the suggested name), set Private/Public, then click Publish repository.

(Optional) Enable GitHub Pages: on GitHub.com open the repo → Settings → Pages → Source → select branch main and folder / (root) → Save. After a minute GitHub will provide a Pages URL where the static index.html is served.

Test: open the GitHub Pages URL on a phone/tablet (camera access is required, so use HTTPS or Pages URL).

Notes about Google Drive uploads

The client-side code posts base64 chunks to the Apps Script URL defined by APPS_SCRIPT_URL in index.html. Because that endpoint is unchanged, files will continue to be saved to the same Google Drive location. If you later change the Apps Script deployment URL, update APPS_SCRIPT_URL accordingly.

Deploying Apps Script (if you need to update that)

Open the Apps Script project in script.google.com.

Deploy → New deployment → Select "Web app", set access to "Anyone" (or suitable scope), and Deploy. Copy the new URL and replace APPS_SCRIPT_URL in index.html if necessary.

Troubleshooting

If camera doesn't start, ensure the page is loaded from HTTPS and permissions are granted.

If uploads fail, test the Apps Script web app URL separately with a small POST to confirm it is still accepting chunked uploads.

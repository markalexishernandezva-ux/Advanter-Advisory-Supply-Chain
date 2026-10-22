# Deploy steps (about 15 minutes)

## 1. Private GitHub repo
1. github.com > New repository > name it `advanter-crm` > select **Private** > Create.
2. Click "uploading an existing file", drag in everything from this folder
   (index.html, contacts.json, _headers, robots.txt, .gitignore, README.md) > Commit.

## 2. Host it (pick ONE)
### Option A: Cloudflare Pages (recommended, login is free for up to 50 users)
1. dash.cloudflare.com > Workers & Pages > Create > Pages > Connect to Git > authorise and pick `advanter-crm`.
2. Framework preset: None. Build command: leave empty. Output directory: `/` (or leave blank). Deploy.
3. Custom domain: Pages project > Custom domains > add `network.yourdomain.com`.
4. LOGIN (do not skip): Zero Trust > Access > Applications > Add > Self-hosted.
   Domain = network.yourdomain.com AND also your `*.pages.dev` address (otherwise it stays open).
   Policy: Allow > Emails = your and your clients' email addresses. They get a one-time code by email.

### Option B: Netlify
1. app.netlify.com > Add new site > Import from Git > pick `advanter-crm`. No build command, publish directory `.`
2. Site configuration > Domain management > add network.yourdomain.com.
3. LOGIN: Site configuration > Access & security > Visitor access > Password protection.
   (This needs a paid Netlify plan. On the free plan use Option A.)

## 3. Test before sharing
- Open the site in a private/incognito window: it must ask for login.
- Open https://network.yourdomain.com/contacts.json in incognito: it must ALSO ask for login.
  If you can see the data, the login is not covering the site. Fix this before sharing the link.

# ADVANTER Network CRM: self-hosted package

Files
- index.html: the app (dashboard, search, pipeline, numbered pages).
- contacts.json: your 15,927 contacts. Row format: [source row, first, last, title, company, function, seniority, industry, linkedin url, relationship, relevance, notes, stage].

Deploy
1. Upload index.html and contacts.json to the same folder on your web host (any static host works).
2. Put the folder behind your own login (for example your client portal, basic auth, or your host's access control).
   IMPORTANT: contacts.json holds every contact. If the folder is public, anyone with the address can download it.
3. Give clients the branded address of your own site (for example network.yourdomain.com).

What works here
- Dashboard, search, filters, pipeline view, paging.
- Stage, relevance and note edits are saved per browser only (localStorage). They are not shared between people.
- The "+ Add contact" button is hidden: adding shared contacts needs a database.

To get shared edits and add-contact on your own site, your developer needs to connect a database and login system.
The claude.ai version already has these.

Updating data: replace contacts.json with a new export in the same row format. Contacts added in the claude.ai version are not in this file.

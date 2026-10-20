# Heaven Reign Transformation Ministry — Website

Everything the site needs is in this folder:

| File | What it is |
|---|---|
| `index.html` | The whole website: Home, Media and Connect pages |
| `images/` | The 5 photos, resized for fast loading |
| `calendar.ics` | Weekly gatherings for the "Add to calendar" button |
| `LAUNCH-CHECKLIST.md` | What to confirm before sharing the site publicly |

## Technology used (all free)

- **Website:** one HTML page with built-in CSS and JavaScript. No WordPress, no database, nothing to update or patch.
- **Hosting:** Netlify free plan, with HTTPS (the padlock) included.
- **Free address:** `your-name.netlify.app`.
- **Contact and prayer forms:** Netlify Forms. Free plan includes 100 submissions a month, with email alerts.
- **Event calendar:** computed live in Central Time, plus `calendar.ics` that works with iPhone, Google and Outlook calendars.
- **Sermons:** link to YouTube, Facebook or SoundCloud (free hosting for audio and video).
- **Online giving:** Tithe.ly, PayPal Giving or Zelle links.
- **Fonts:** Google Fonts (free).

## Put the site online for free (about 10 minutes)

1. Fill in the settings first (see "Editing" below), or do it later and re-upload.
2. Go to **https://app.netlify.com/signup** and create a free account (email or GitHub).
3. Go to **https://app.netlify.com/drop** and drag this whole folder onto the page.
4. Netlify gives the site a random name. Open **Site configuration → Change site name** and type `heavenreign` (or another free name). The address becomes `https://heavenreign.netlify.app`.
5. Turn on the forms: **Forms → Enable form detection**. Then drag the folder onto the site's **Deploys** page once more so Netlify finds the two forms.
6. Get form messages by email: **Site configuration → Notifications → Emails and webhooks → Form submission notifications → Add notification → Email**. Enter the ministry email.
7. Test it: open the live site, send a test prayer request and a test message, and check that the emails arrive.

## Editing

Open `index.html` in any text editor (Notepad, TextEdit, VS Code). Near the bottom, find **SITE SETTINGS**:

```js
email:"info@example.org",
phone:"(918) 555-0123",
leaderTitle:"Senior Pastor",
serviceLocation:"123 Main St, Tulsa, OK",
routingNumber:"",
giving:{ tithely:"https://tithe.ly/give?c=…", paypal:"", zelle:"" },
sermons:[
  {date:"2026-10-18", title:"Equipped to Go", service:"Empowerment Hours",
   scripture:"Ephesians 4:11-16", video:"https://youtube.com/…", audio:""}
]
```

Anything left as `""` stays hidden. Save, then drag the folder onto the site's **Deploys** page to publish the change.

**Changing photos:** save the new photo into `images/` under the same file name as the one it replaces (for example `feeding-children.jpg`), or add a new `<figure>` line in the Gallery section of `index.html`.

**Custom domain and forms:** if you connect your own domain, add `<script>window.HRTM_FORMS_LIVE=true</script>` just above the SITE SETTINGS block so the forms send there too.

## A custom domain later (optional, about $10–15 a year)

1. Buy a name such as `heavenreign.org` from Namecheap, Porkbun or Cloudflare.
2. In Netlify: **Domain management → Add a domain**, then follow its instructions to point the domain to Netlify.
3. Netlify adds free HTTPS automatically. The old `.netlify.app` address keeps working.

## Other free hosts (forms will not work there)

GitHub Pages and Cloudflare Pages also host this site for free. The contact and prayer forms rely on Netlify, so use Netlify unless you connect another form service.

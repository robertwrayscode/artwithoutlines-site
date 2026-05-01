# Uploading to Bluehost — Art Without Lines

You have everything you need in this folder. Easiest path is the zip file plus Bluehost's File Manager.

## Quickest path (~5 minutes)

1. **Log into Bluehost** at bluehost.com → My Sites or Hosting.
2. Open **cPanel** → **File Manager** (or "Advanced" → "File Manager").
3. Navigate to **`public_html`**. If you have multiple domains, go to **`public_html/artwithoutlines.org`** instead.
4. **Important:** if there's an existing `index.html` (a Bluehost placeholder), delete or rename it.
5. Click **Upload** in the toolbar and upload `artwithoutlines-site.zip`.
6. Back in File Manager, right-click the zip → **Extract** → confirm.
7. Delete the zip file once extracted.
8. Visit **artwithoutlines.org** in your browser — the site should be live within a minute or two.

## Files you're uploading

```
index.html         ← homepage
about.html         ← About page
mission.html       ← Mission page
get-involved.html  ← Get Involved page
contact.html       ← Contact page
styles.css         ← shared stylesheet (don't rename)
```

## If you'd rather upload files individually

Same as above but skip the zip — just upload the 6 files directly into `public_html` (or `public_html/artwithoutlines.org`).

## DNS / domain notes

If `artwithoutlines.org` is registered with Bluehost AND you're using their hosting, there's nothing to configure — the domain already points at `public_html` for your account. If the domain is registered elsewhere, make sure its nameservers point at Bluehost (`ns1.bluehost.com`, `ns2.bluehost.com`).

## Common gotchas

- **Page loads but looks unstyled** → `styles.css` is missing or in a subfolder. It needs to be in the same folder as the HTML files.
- **404 on a page** → check the filename matches exactly (lowercase, with `.html`).
- **Old Bluehost placeholder still shows** → delete `index.html`, `default.html`, or any `index.php` left in the folder, then upload yours.
- **Browser cache** → if you see an old version after uploading, hard-refresh with Ctrl+Shift+R (Cmd+Shift+R on Mac).

## Editing later

Anyone can open these `.html` files in a text editor (VS Code, TextEdit, Notepad++, etc.) to change copy. The body text lives between the `<section>` tags — you'll spot it without needing to know HTML. After editing, re-upload the changed file via File Manager and overwrite.

## Email link

The Contact, footer, and CTAs all link to `laurijwray@gmail.com`. To change it, do a find-and-replace for that string across all five HTML files.

---

**Site stack:** plain HTML + CSS, no build step, no JavaScript framework, no database. Loads Google Fonts (Fraunces + Inter) from Google's CDN — no setup needed.

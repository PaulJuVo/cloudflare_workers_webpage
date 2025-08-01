## 🔧 1. **Performance & Bildoptimierung** (vor dem Export)

### ✅ **Performance Lab** (offiziell von [WordPress.org](http://wordpress.org/))

- **Aktivieren:** WebP-Unterstützung, Lazy Load, Optimierung von Assets.
- **Optional:** AVIF-Unterstützung, falls vom Theme/Browser unterstützt.

### ✅ **EWWW Image Optimizer**

- Automatische Bildkomprimierung beim Upload
- Aktivieren: "WebP"-Erzeugung (nur lokal)
- Optional: "Replace original images"

> Wichtig: Alle Optimierungen müssen vor dem Export mit Simply Static erfolgen, da es statische Kopien erzeugt.
> 

---

## 🌐 2. **SEO-Plugins** (Meta-Daten, OpenGraph etc.)

### ✅ **Rank Math SEO** *(oder alternativ: Yoast SEO)*

- Generiert Meta Title, Description, Canonical Tags, OpenGraph & Twitter Cards
- Sitemap funktioniert nur, wenn von Simply Static mit-exportiert oder manuell kopiert

---

## 🔀 3. **Zusätzlich empfehlenswert**

### ✅ **Autoptimize** *(nur aktiv vor Export!)*

- Minifiziert CSS/JS/HTML
- Optimiert Google Fonts, Lazy Load für Iframes

---

## 🧪 4. **Simply Static Setup-Tipps**

### 🔽 "Exclude URLs" – was gehört hinein?

Diese URLs solltest du ausschließen, weil sie dynamisch oder unnötig sind:

```
/wp-admin
/wp-login.php
/wp-json
/xmlrpc.php
?rest_route=
?preview=true
?customize_changeset_uuid=
/wp-includes/js/wp-emoji-release.min.js

```

---

## Short

1. Bildoptimierung durch EWWW / Performance Lab
2. SEO-Daten mit Rank Math eintragen
3. Seite gestalten (Gutenberg, Navigation, Anker etc.)
4. Autoptimize und Performance Lab optimieren Code
5. Simply Static ausführen
6. ZIP exportieren und auf statischem Hoster (Cloudflare Workers) bereitstellen

---

## vs code

robots.txt erstellen 

```java
User-agent: *
Disallow:

Sitemap: https://offenstallamwald.pages.dev/sitemap.xml
```
```html
<link rel="canonical" href="/" /> 
```

→ href setzen

https://developers.cloudflare.com/workers/static-assets/get-started/#deploy-a-static-site

neues Projekt erstellen und Cloudflare CLI Tool verwenden

### Local Testen

 npx wrangler dev --assets=public 

### Deployen

npx wrangler deploy

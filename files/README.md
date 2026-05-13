# Josia Meyer — Website

## Projektstruktur

```
josia-meyer-site/
├── index.html          ← Haupt-Website (hier alles bearbeiten)
├── netlify.toml        ← Netlify Konfiguration (nicht anfassen)
├── images/
│   ├── logo.png
│   ├── photo_spotlight.jpg      → Hero Hintergrund
│   ├── photo_red_portrait.jpg   → About Hauptbild
│   ├── photo_laughing.jpg       → About Gitterbilder
│   ├── photo_stage_wide.jpg     → About Gitterbilder
│   └── ...
└── README.md
```

---

## GitHub + Netlify einrichten (einmalig)

### 1. GitHub Repository erstellen
1. Gehe auf [github.com](https://github.com) → **"New repository"**
2. Name: `josia-meyer-website`
3. **Public** oder Private (beides funktioniert mit Netlify)
4. Klick **"Create repository"**

### 2. Dateien hochladen
1. Im neuen Repository auf **"uploading an existing file"** klicken
2. Den ganzen `josia-meyer-site` Ordner per Drag & Drop reinziehen
3. **"Commit changes"** klicken

### 3. Netlify mit GitHub verbinden
1. [app.netlify.com](https://app.netlify.com) → **"Add new site"** → **"Import an existing project"**
2. **"Deploy with GitHub"** → GitHub authorisieren
3. Dein Repository `josia-meyer-website` auswählen
4. Build-Einstellungen: alles leer lassen (kein Build nötig)
5. **"Deploy site"** klicken → Site ist live ✅

### 4. Eigene Domain verknüpfen
1. Netlify → deine Site → **"Domain management"** → **"Add custom domain"**
2. `josiameyer.de` eingeben
3. Netlify zeigt dir 2 DNS-Einträge → diese bei **United Domains** eintragen
4. Nach 10–30 Minuten ist die Domain live

---

## Website aktualisieren (nach dem Setup)

**Ab jetzt läuft alles über GitHub:**

1. Gehe auf [github.com](https://github.com) → dein Repository
2. Klick auf `index.html`
3. Klick auf das **Stift-Symbol** (Edit) oben rechts
4. Ändere den Text direkt im Browser
5. Klick **"Commit changes"**
6. → Netlify deployed automatisch in ~30 Sekunden ✅

**Neue Fotos hinzufügen:**
1. Im Repository → `images/` Ordner öffnen
2. **"Add file"** → **"Upload files"**
3. Foto hochladen → Commit
4. In `index.html` den Bildpfad anpassen: `src="images/dein-foto.jpg"`

---

## Audio & Video einbetten

### SoundCloud (für Audio-Player)
1. Track auf [soundcloud.com](https://soundcloud.com) hochladen
2. Track-URL kopieren (z.B. `https://soundcloud.com/josia-meyer/lucky-strike`)
3. In `index.html` beim jeweiligen Audio-Card das `data-sc=""` Attribut befüllen:
   ```html
   <div class="mp ..." id="mp1" data-sc="https://soundcloud.com/josia-meyer/lucky-strike">
   ```
4. Beim Klick auf Play öffnet sich SoundCloud direkt → kein Datei-Upload nötig!

### YouTube (für Video-Cards)
1. Video auf [youtube.com](https://youtube.com) hochladen (kann auch Unlisted sein)
2. Video-ID aus der URL kopieren — das ist der Teil nach `v=`
   Beispiel: `https://www.youtube.com/watch?v=`**`dQw4w9WgXcQ`**
3. In `index.html` die Funktion `toggleVid` beim jeweiligen Video-Card anpassen:
   ```html
   onclick="toggleVid('vid1','DEINE_VIDEO_ID')"
   ```
4. Auch das Vorschaubild (Thumbnail) anpassen:
   ```html
   src="https://img.youtube.com/vi/DEINE_VIDEO_ID/mqdefault.jpg"
   ```

### Demo Reel (YouTube)
Gleich wie oben — in `index.html` den iframe src anpassen:
```html
src="https://www.youtube.com/embed/DEINE_VIDEO_ID?controls=1&rel=0&modestbranding=1"
```

---

## Texte ändern — was steht wo?

| Was                  | Suche nach                          |
|----------------------|-------------------------------------|
| Hero-Titel           | `I produce`                         |
| About Bio            | `I'm Josia Meyer`                   |
| Projekt-Titel        | z.B. `Lucky Strike`                 |
| Projekt-Beschreibung | Text unter dem Projekt-Titel        |
| Zitate               | `In their own words`                |
| Kontakt Email        | `Kontakt@Josiameyer.de`             |

---

## Fragen?

Öffne einfach einen neuen Chat mit Claude und schick den Link zu deinem GitHub Repository — dann kann direkt geholfen werden.

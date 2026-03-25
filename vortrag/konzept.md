# Konzept – „Eduard Amthor. Wege werden Wissen.“

## 1. Leitidee & Ziel
-domain: amthor-gera.de
- **Ziel:** Eine immersiv erzählte Scrollytelling-Website, die den gehaltenen Vortrag digital verlängert und Besucher für die geplante Amthor-Tour 2027 begeistert. Der Fokus liegt auf der Transformation von Wissen zu Bewegung: „Amthor hat Wege beschrieben. Wir können sie gehen.“
- **Ton & Haltung:** Ernsthaft, poetisch, respektvoll gegenüber Geschichte – kombiniert mit klarer, moderner Interface-Sprache.
- **Story-Modus:** Kapitelhafte Dramaturgie mit „Stille → Erkenntnis → Bewegung → Einladung“. Jedes Kapitel verdichtet Originalzitate und übersetzt sie in audiovisuelle Erlebnisse.

## 2. Zielgruppen & Nutzungsszenarien
1. **DAV-Mitglieder & Bergbegeisterte** – Inspiration für eine besondere Mehrtagestour.
2. **Historisch Interessierte / regionale Öffentlichkeit** – Zugang zu Amthors Biografie und Gera-Bezug.
3. **Presse / Multiplikatoren** – klarer Überblick über Projektidee, Download-Material, Kontakt.

## 3. Inhalts- und Page-Flow
| Kapitel | Inhaltlicher Fokus | Interaktives Element |
| --- | --- | --- |
| **Stille / Auftakt** | Poetik der Introfolie (Video-only, emotionaler Einstieg) | Vollbild-Video, typografisches Einblenden einzelner Worte, Voice-over |
| **Der Gelehrte** | Biografie + Gera als geistiges Zentrum | Split-Screen mit Porträt, animierte Stichworte, Audio-Snippets aus Briefen |
| **Netzwerk & Publikationen** | „Der Alpenfreund“, Karten, Korrespondenzen | Lightbox-Galerie, SVG-Schreibanimationen, Quellenhover |
| **Die Route** | Daten & Emotion der 4-tägigen Tour | Scrollgeste steuert Karte/Höhenprofil, atmosphärische Field-Recordings |
| **Fortsetzung 2027** | From Story to Call-to-Action | CTA-Karten (Anmeldung, Audio-Edition), Kontaktformular, Download |
| **Schlussakkord** | Erinnerung als Bewegung | Großes Zitat, Audio-Fade-out, Social-Sharing-Block |

Zwischenkapitel-Trenner greifen die „⸻“ aus dem Vortrag typografisch auf, um Ruheinseln zu schaffen.

## 4. Textkuratierung
- **Poetische Passagen** (Intro, Schluss, Programmsatz) bleiben nahezu unverändert und werden als Voice-over produziert.
- **Erklärende Abschnitte** (Biografie, Gera, Publikationen) werden verdichtet auf 3–5 Leitsätze pro Modul.
- **Route** erhält datenjournalistischen Ton (Tagesetappen, Höhenmeter, Schwierigkeit), aber mit je einem Zitat-Anker („Amthor hat Wege beschrieben...“).
- **Microcopy** für UI-Elemente bleibt aktiv („Jetzt Weg entdecken“, „Audioreise starten“), um moderne Klarheit zum historischen Text zu setzen. Ergänzend gezielte Buttons pro Modul:

| Sektion | Microcopy |
| --- | --- |
| Intro / Hero | „Dem Pfad folgen“ |
| Biografie | „Vom Wort zum Weg“ |
| Tirolerführer / Archiv | „Im Archiv blättern“ |
| Tour 2027 | „Die Route begehen“ |
| Schlussakkord | „Erinnerung in Bewegung setzen“ |

## 5. Farb- & Typ-Konzept
| Name | Hex | Einsatz |
| --- | --- | --- |
| **Alpine Night** | `#0B0C10` | Hintergrundfläche, immersive Dunkelheit |
| **Gera Ink** | `#111318` | Sekundäre Panels, Footer |
| **DAV Green** | `#50AE2F` | Primäre Akzente, Linienführung, Buttons |
| **Alpine Mist** | `#A9B5C7` | Fließtexte auf dunklem Grund, Icons |
| **Summit Glow** | `#F1D8A5` | Warmes Highlight für Zitate, Kapitelübergänge |
| **Snow White** | `#F6F8F9` | Text auf hellen Panels, Formularfelder |
| **Rock Gray** | `#707680` | Sekundäre Typografie, Trennelemente |

- **Verläufe:** `linear-gradient(135deg, #0B0C10 0%, #111318 60%, #1E1A27 100%)` in Hero; `linear-gradient(90deg, rgba(80,174,47,0.3), rgba(241,216,165,0.35))` als zarter Overlay über Karten.
- **Typografie:**  
  - `Playfair Display` (Titel/Zitate, Größe 48–80px, Tracking -2%).  
  - `Fira Sans` (Body, Navigations-UI).  
  - `Great Vibes` sparsam für Handschrift-Akzente (z.B. „Eine Erinnerung in Bewegung“).  
- **Iconographie:** Font Awesome Linien-Icons, reduziert auf Themen Tour, Karte, Audio.

## 6. Layout & Komponenten
- **Hauptlinien-Navigation:** Ein vertikaler SVG-Pfad („Hauptlinie“) zieht sich als Sticky-Navigation durch die Seite. Ein wandernder Punkt zeigt die aktuelle Scrollposition; Abzweigungen führen zu Nebenlinien (Biografie, Publikationen, Route).
- **Hero / Kapitel-Intro:** full viewport, Smooth-Scroll-Hinweis, Progress-Dot rechts.
- **Chapter Cards:** horizontale Scroll-Snaps für Publikationen (z.B. `assets/Covers/...`).
- **Quellen-Hover:** On hover Blende mit Quelle, Signatur, Link in `quellen/`.
- **Quote Blocks:** Großflächige Typografie, Zitatlinie plus Stimmungsbild im Hintergrund (Blend Mode `screen`).
- **CTA-Zone:** Zwei gleich große Karten („Tour 2027“, „Audio-Edition“), beide mit Microinteraction (Scale bei Hover).

## 7. Interaktive Ankerpunkte & Module
- **Kapitel „Stille“:** Cinematic Entry mit `intro.mp4`. Scrollstart blendet Voice-over weich ein; Wörter schweben als Nebelfetzen (Opacity + Blur) über das Video.
- **„Gelehrter vs. Reiseteufel“:** Interactive Portrait Flip – Hover/Scroll legt gezeichnete Wanderutensilien über das Porträt, Handschrift-Zitat in `Great Vibes` („Das ist eben der Reiseteufel…“).
- **„Tirolerführer“-Archiv:** Digitales Exponat (hochauflösender Scan) mit Hotspots, Tooltips zu `(t)/(tt)/(ttt)`, Kontext zur Frauenrolle. Lightbox erweitert Informationen.
- **„Amthorspitze“:** 3D-Gipfel (Mapbox GL oder Three.js Heightmap). Scrollzoom, Urkunden-Overlay, Field-Recording Wind.
- **Tour 2027:** Progressive Map mit GPX-Track, Echtzeitzeichnung, fixiertes Höhenprofil + Stats (47,5 km, 3.4k ↑). Scrollposition steuert Marker.
- **Amthor-Prinzip als UX:** Nebenlinien branchen Biografie/Pub/Route aus Hauptlinie aus, sorgen für mentale Karte der Webseite und greifen das „Hauptlinien“-Narrativ auf.
- **Archiv-Hotspots:** Tooltip-Karten erklären Begriffe wie „Hauptlinien“, „merkantil“, „alpin“, um Texttiefe zu erhalten.

## 8. Motion & Scrolling
- **Scroll-Control:** Lenis oder Smooth Scroll + GSAP ScrollTrigger (Fallback ohne JS = lineare Darstellung).  
- **Key Interaktionen:**  
  - Intro-Wörter erscheinen sequenziell (Opacity + Blur).  
  - SVG-Linienzeichnung für Kartenpfad (`assets/alpen-silhuette.svg`).  
  - Audio-Wellenform (Canvas) reagiert auf Scrollposition.  
  - Timeline-Pins (Gera 1854, Amthorspitze 1880, Route 2027) poppen bei Intersection.
- **Performance:** Lottie nur für kleine Effekte, Videos als MP4 + WebM, Lazy Loading für Assets.

## 9. Audio-Konzept
- **Voice-over:** Professionelle Sprecherstimme für Intro, Schlüsselzitate, Schluss.  
- **Atmos Layer:** Wind, Schritte, Hüttengespräch – pro Kapitel wechselnd, nahtlos überblendbar (Web Audio API, Ducking bei Voice).  
- **Audio Controls:** Sticky Player am rechten Rand (Play/Pause, Kapitelwahl). Autoplay nur nach User-Interaction (EU-Richtlinie). Optional Download als Podcast-Kapitel.  
- **Audioproduktion:** 3 Tracks (Intro, Hauptteil, Schluss) + 4 Atmos-Loops.

## 10. Medien- & Asset-Plan
- **Bestehende Assets** (`assets/`): Porträt, Karten, Urkunden, historische Briefe, Videos (`intro.mp4`, `amthor_portrait_animated.mp4`).  
- **Zusätzliche Needs:** Drohnenfootage Hochalpen (lizenzieren), Sounddesign, ggf. aktuelle Fotos Geraer Hütte/Amthorhütte.  
- **Bildbehandlung:** Farbraum leicht entsättigen, Tonwerte an die Grundpalette anpassen (Curves, Grain).  
- **Lightbox:** Klick vergrößert Asset, Infoleiste mit Herkunft/Jahr/Quelle.

## 11. Funktionale Module
1. **Sticky Navigation:** Kapitel-Scroller + Fortschrittsindikator.
2. **Map Experience:** Leaflet/Mapbox, GPX-Track der Tour (4 Etappen, Tooltips, Höhenprofil).
3. **Timeline-Komponente:** 3 Knoten (Gera, Netzwerk, Ehrung 1880) plus horizontales Scrollen.
4. **Kontakt & CTA:** Formular (Name, E-Mail, Interesse), DSGVO-Hinweis, Newsletter-Opt-in.
5. **Downloadbereich:** PDF (Vortrag, Tourdaten, Pressekit), Social Share Cards (Open Graph).

## 12. Technischer Stack & Umsetzung
- **Frontend:** Tailwind CSS + individuelle Utility-Erweiterungen (Farben, Letterspacing), GSAP ScrollTrigger, Intersection Observer, Lenis (Smooth Scroll).  
- **Medienverwaltung:** Assets lokal + optional Cloudfront/CDN für Videos.  
- **Build:** Vite oder reine static page mit esbuild-Bundling für JS.  
- **Accessibility:** Reduced-motion-Fallback (bereits im bestehenden CSS angedeutet), Transkripte für Audio, ausreichende Kontraste (`#50AE2F` auf `#0B0C10` AA-konform).  
- **SEO:** Structured Data (Event 2027), Open Graph mit Hero-Still, Meta-Beschreibungen.

## 13. Content Backlog & ToDos
- [ ] Feinbriefing für Voice-over & Sounddesign.  
- [ ] Textkompression + Übersetzung in modulare Blöcke.  
- [ ] Erstellung GPX + Datenvisualisierung (Höhenprofil, Stats).  
- [ ] Wireframes/Figma-Prototyp (Mobile & Desktop).  
- [ ] Implementierung Scrollytelling + Testing (Desktop, Tablet, Mobile, mit/ohne Audio).  
- [ ] Finale QA (Performance, Accessibility), Deployment, Analytics-Einrichtung.

Mit diesem Konzept kann die bestehende Wirkung des Vortrags in eine moderne, multisensorische Web-Erfahrung übertragen werden, die Geschichte, Landschaft und Zukunftsprojekt nahtlos miteinander verbindet.

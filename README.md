# Maktspelet — landningssida (utkast)

Fristående, statisk scrollande landningssida för museispelet **Maktspelet** (kodnamn Eco Loco).
Ett första utkast tänkt att skickas till museer/arrangörer som ska ta emot och köra spelet.

## Innehåll

- `index.html` — hela sidan (inline CSS + JS, inga byggsteg).
- `media/` — filmer, bilder och typsnitt (alla sökvägar relativa).

Fonter (`Oxanium`, `Chakra Petch`), palett (`#121009` / guld `#C9A94F` / `#F2ECDD`)
och logotyp är hämtade från spelet så att sidan matchar upplevelsens ton.

## Funktioner

- Hero med bakgrundsfilm (autoplay, muted, loop) + logotyp-overlay.
- Scrollytelling: premiss (trailer som bakgrund) → rummet/situationsfoton → levande spel-UI → trailer → versioner → krav på lokalen → CTA (bakgrundsfilm).
- Levande spel-UI: en markör stegar Bygg → Byt → Rösta → Bokslut i ~10 s loop, synkat mot en highlight i det riktiga spelgränssnittet (skärmbild från nuvarande spel.html).
- Trailer spelar som ljudlös teaser och startar om med ljud vid klick.
- **SV/EN-växlare** (svenska som standard, val sparas i `localStorage`).
- Boknings-CTA = `mailto` till Josef + Madde.
- Respekterar `prefers-reduced-motion`, fungerar på mobil + desktop.

## Förhandsgranska lokalt

Öppna `index.html` direkt i en webbläsare, eller kör en enkel server:

```
cd maktspelet-landing
python3 -m http.server 8080
# → http://localhost:8080
```

## Publicering (GitHub Pages)

Samma mönster som `xy-presentation`: statisk sida, push → auto-redeploy.

1. Skapa ett eget repo och lägg innehållet i detta mapp i repo-roten.
2. Aktivera GitHub Pages (branch `main`, mapp `/root`).
3. `.nojekyll` finns med så att allt serveras som statiska filer.

*Deploy-steget tas av Josef — repot är inte skapat eller pushat härifrån.*

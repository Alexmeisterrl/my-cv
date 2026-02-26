# Entscheidungen

- **Stack:** Astro + Tailwind CSS 4.
- **Layout:** Bento-Grid (4 Spalten) mit einseitigem (linksbündigem) Zeitstrahl für bessere Lesbarkeit.
- **Reihenfolge:** 
  1. Hero (Name, Bild, About)
  2. Schulische Laufbahn (2 Spalten)
  3. Berufliche Laufbahn (2 Spalten)
  4. Projekte (4 Spalten)
  5. Skills & Sprachen/Interessen (4 Spalten gesamt)
- **Daten:** Inhalte werden zentral in `CONTENT.json` gepflegt.
- **Features:** Dark/Light Mode (mit LocalStorage-Speicherung), Scroll-Reveal Animationen.
- **Naming:** Die interaktive KI-Seite wurde von "Playground" in "AI Demo" umbenannt, um eine klarere und professionellere Wirkung im Portfolio-Kontext zu erzielen.
- **Profilbild:** Verwendung von `public/profile.jpg` (Original: `pb.jpg`).
- **Gesten-Erkennung:** Umstellung auf eine orientierungsunabhängige, abstandsbasierte Heuristik (unter Einbeziehung der Z-Achse für 3D-Landmarks) zur besseren Imitation der ML-Modell-Ergebnisse aus dem Jupyter Notebook, inklusive Resultat-Glättung (Consensus-Buffer).

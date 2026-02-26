# Projekt-Logbuch: Alexander Leonardo Kolb CV

## 23. Februar 2026 - Meilensteine: Content, GitHub & AI Playground

Heute war ein extrem produktiver Tag. Wir haben die Website von einem Platzhalter zu einem echten, persönlichen Portfolio transformiert und erste Schritte in Richtung interaktiver KI-Features gemacht.

### 👤 Persönliches Profil & Design
- **Daten-Migration:** Alle Informationen aus Alexanders CV (H-BRS, 1&1, Bitsea, Kagawa University) und der `Kenntnisse.md` wurden in die `CONTENT.json` übertragen.
- **Profilbild:** Hochwertiges Foto (`pb.jpg`) integriert.
- **Timeline-Refactoring:** Das Zeitstrahl-Design wurde auf ein sauberes, linksbündiges Layout umgestellt für bessere Lesbarkeit.
- **Grid-Optimierung:** Die Reihenfolge wurde angepasst (Schule -> Beruf -> Projekte -> Skills). Lücken im Grid wurden durch neue Kacheln für Sprachen und Interessen gefüllt.

### 🐙 GitHub & Management
- **Repository-Start:** Lokales Projekt mit `https://github.com/Alexmeisterrl/my-cv.git` verknüpft und gepusht.
- **Sicherheit:** `.gitignore` konfiguriert, um den `personal/`-Ordner mit privaten Daten strikt von GitHub fernzuhalten.
- **Struktur:** Alle Management-Dateien (`PROJECT.md`, `TODO.md`, etc.) in den neuen Ordner `docs/` verschoben für ein sauberes Root-Verzeichnis.
- **README:** Professionelle, ansprechende README mit Badges und Kurzanleitung erstellt.

### 🧪 AI Playground
- **Setup:** Geheime Seite `/playground` erstellt (unverlinkt, `noindex`).
- **Live-Demo:** Grundstein für die "FingerCounting AI" Demo gelegt.
  - Kamera-Zugriff implementiert.
  - Mediapipe Hand-Tracking integriert (Echtzeit-Skelett-Anzeige).
  - Robuste Logik für Finger-Zählen (0-5) und die **Spock-Geste (🖖)** in JavaScript entwickelt.

---
**Nächste Session:**
- Weitere Projekte in die `CONTENT.json` aufnehmen.
- Deployment-Vorbereitung für die Live-Ansicht.

## 26. Februar 2026 - AI Playground Verfeinerung

Die Gestenerkennung im AI Playground wurde heute signifikant verbessert, um die Präzision und Robustheit zu erhöhen.

### 🧠 Intelligente Heuristik
- **3D-Abstände:** Die Logik wurde von einfachen 2D-Vergleichen auf 3D-Abstandsmessungen (Euklidische Distanz unter Einbeziehung der Z-Achse) umgestellt. Dies macht die Erkennung weitgehend unabhängig von der Handorientierung zur Kamera.
- **Robustheit:** Ein Finger wird nun basierend auf dem Abstand zwischen Wurzelgelenk (MCP) und Spitze im Vergleich zum Handgelenk erkannt, was Fehlinterpretationen bei geneigter Hand reduziert.
- **Spock-Präzision:** Die Spock-Geste wird nun durch Gruppen-Cluster-Logik (Index+Mittel nah, Ring+Kleiner nah, Lücke dazwischen) deutlich stabiler erkannt.
- **Glättung (Smoothing):** Implementierung eines Konsens-Puffers (HISTORY_SIZE = 5). Ergebnisse werden über mehrere Frames gemittelt, um "Zittern" und kurzzeitige Fehlklassifizierungen zu eliminieren.
- **Fallzahl-Korrektur:** Wenn keine Hand im Bild ist, wird nun automatisch das Fragezeichen ("?") bzw. "Suchen..." angezeigt, statt das letzte Ergebnis einzufrieren.

### 🧪 AI Demo & Portfolio Integration
- **Umbenennung:** Seite von `/playground` auf `/demo` umgestellt. Titel geändert zu "AI Demo" (🤖).
- **Projekt-Verknüpfung:** Die Projekt-Kachel "FingerCounting AI" ist nun direkt mit der `/demo`-Seite verlinkt.
- **Content-Polishing:** 
  - Der "Über mich" Text wurde in die Ich-Form umgeschrieben für eine persönlichere Ansprache.
  - Die Hero-Sektion wurde auf das Wesentliche (Rolle) reduziert für einen cleaneren Look.
- **UI-Upgrade:** Die Projekt-Sektion wurde von einfachen Links auf ein interaktives Karten-Design mit separaten Links für GitHub und Live-Demos umgestellt.
- **CONTENT.json:** Erweiterung des Datenmodells um `demoLink` für zukünftige interaktive Projekte.
- **GitHub Integration:** Eine neue, prominente GitHub-Bento-Kachel wurde hinzugefügt, um die Code-Basis und Beiträge direkt zugänglich zu machen. Die untere Grid-Reihe wurde für ein besseres Layout neu strukturiert (4 gleichmäßige Kacheln).

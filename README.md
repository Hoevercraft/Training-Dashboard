# TrainingOS Dashboard

Persönliches Trainings-Analyse-Dashboard mit Tredict-Integration und Claude AI.

## Features

- **Letztes Training** — Auswertung mit Pace/Watt, HF-Zonen, prägnante Einschätzung
- **Entwicklung** — 8-Wochen-Trend mit Chart, Volumen & Herzfrequenz
- **Chat** — Direkter Trainingscoach mit Zugriff auf deine Tredict-Daten

## Deployment (Netlify + GitHub)

### 1. Repository auf GitHub anlegen

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/DEIN-USERNAME/training-dashboard.git
git push -u origin main
```

### 2. Netlify mit GitHub verbinden

1. [netlify.com](https://netlify.com) → „Add new site" → „Import an existing project"
2. GitHub auswählen → dein Repository wählen
3. Build-Einstellungen werden automatisch aus `netlify.toml` gelesen
4. „Deploy site" klicken

### 3. API Key hinterlegen (sicher!)

In Netlify: **Site settings → Environment variables → Add variable**

```
Key:   ANTHROPIC_API_KEY
Value: sk-ant-...
```

Speichern → Site neu deployen (Deploys → „Trigger deploy").

### 4. Fertig

Deine URL: `https://DEIN-SITE-NAME.netlify.app`

---

## Lokales Testen

Netlify CLI installieren und lokal starten:

```bash
npm install -g netlify-cli
netlify dev
```

Dann unter `http://localhost:8888` erreichbar.

> ⚠️ Den API-Key **niemals** direkt in den Code oder ins Repository schreiben.

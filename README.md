# VERYLON — Competitor Intelligence

AI-powered competitor review analysis dashboard für VERYLON's Positionierungsstrategie.

## Deploy auf Netlify

### 1. Repo auf GitHub pushen
```bash
git init
git add .
git commit -m "VERYLON Intelligence Dashboard"
git remote add origin https://github.com/DEIN-USERNAME/verylon-intelligence.git
git push -u origin main
```

### 2. Netlify verbinden
1. [netlify.com](https://netlify.com) → "Add new site" → "Import an existing project"
2. GitHub-Repo auswählen
3. Build-Einstellungen: alles leer lassen (kein Build-Step nötig)
4. Deploy

### 3. API Key setzen
In Netlify: **Site configuration → Environment variables → Add variable**
```
Key:   ANTHROPIC_API_KEY
Value: sk-ant-...
```

### 4. Redeploy
Nach dem Setzen des API Keys: **Deploys → Trigger deploy → Deploy site**

## Lokales Testen
```bash
npm install -g netlify-cli
netlify dev
```
Dann: http://localhost:8888

## Struktur
```
verylon-intelligence/
├── index.html                    # Frontend
├── netlify.toml                  # Netlify-Konfiguration
├── netlify/
│   └── functions/
│       └── analyze.js            # Serverless API-Proxy
└── README.md
```

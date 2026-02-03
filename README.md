# accelerate-traffic

Real-time road closure dashboard for Granada (Spain), monitoring A-4026, A-4025, A-4030, and A-395.

## Data source

Live XML from the official DGT National Access Point (DATEX II):
https://nap.dgt.es/datex2/v3/dgt/SituationPublication/datex2_v36.xml

## Deploy on GitHub Pages

1. Go to your repo **Settings > Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose the branch (e.g. `main`) and folder **/ (root)**
4. Click **Save** — the site will be live at `https://<user>.github.io/accelerate-traffic/`

## Local development

Open `index.html` in any browser. No build step or dependencies required.

## How it works

- Fetches the DGT DATEX II XML feed client-side (via CORS proxy fallback)
- Searches for target road identifiers in situation records
- Classifies severity from DATEX II fields and Spanish DGT terminology
- Auto-refreshes every 5 minutes

## Status indicators

| Emoji | Meaning |
|-------|---------|
| ⚫ | Negro / Corte total / Cerrada |
| 🔴 | Rojo / Embolsamiento / Dificultad |
| 🟡 | Amarillo / Precaución / Obras |
| 🟢 | Sin incidencias registradas |

## License

GPL-3.0

# Amber Light — Solar Sizing (PWA)

Solar sizing app ကို ဖုန်းမှာ **app အနေနဲ့** ထည့်သွင်းနိုင်အောင် PWA ဖြစ်အောင် ပြင်ထားသည်။
Offline လည်း အလုပ်လုပ်သည်။

## ဖိုင်များ
| ဖိုင် | အကြောင်း |
|---|---|
| `index.html` | app တစ်ခုလုံး (CSS/JS + logo inline) + PWA meta + SW register |
| `manifest.webmanifest` | App name, icon, standalone display |
| `sw.js` | offline cache (service worker) |
| `icons/` | 192 / 512 / maskable / apple-touch / logo |
| `.nojekyll` | GitHub Pages အတွက် |

## Hosting (HTTPS လိုအပ်သည် — PWA အတွက်)
**GitHub Pages**
1. Repo အသစ် ဖန်တီးပါ။
2. ဤ folder ထဲက ဖိုင်အားလုံး (`icons/` folder ပါမကျန်) upload လုပ်ပါ။
3. Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save။
4. `https://<username>.github.io/<repo>/` ကို ဖုန်းဖြင့် ဖွင့်ပါ။

## ဖုန်းမှာ App အနေနဲ့ ထည့်နည်း
**Android (Chrome):** menu ⋮ → **Add to Home screen / Install app** → Install
**iPhone (Safari):** Share → **Add to Home Screen** → Add
> iPhone တွင် Safari ဖြင့်သာ ထည့်နိုင်သည်။

## Features
- **System Sizing (kW)** — နေ့စဉ် kWh, peak kW, backup နာရီ → PV kWp, Battery kWh, Inverter kW, Main breaker, Transformer
- **Load List** — kW × qty × hours → connected load, peak demand, daily kWh
- **Calculations** — Breaker, Cable, P·S·Q, PF correction, Transformer
- **SLD** — auto-drawn diagram + drag/drop editor + SVG export

## Update လုပ်လိုပါက
`sw.js` ထဲက `var CACHE = 'amber-light-v1'` ကို `v2` ဟု တိုးပြီး upload လုပ်ပါ။

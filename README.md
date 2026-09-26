# Calculateurs de vidéoprojection

Petits outils d'implantation pour vidéoprojecteurs, en HTML autonome (aucune dépendance, aucun serveur : tout se calcule dans le navigateur).

**Site en ligne :** https://alecgib77.github.io/calculateurs-videoprojection/

## Calculateurs

| Calculateur | Fichier | Description |
|---|---|---|
| **Hisense L9Q** | [`l9q-vertical-offset.html`](l9q-vertical-offset.html) | Offset vertical d'un projecteur à ultra courte focale : décalage lentille → bas d'image, placement du meuble et dimensions du meuble à fabriquer. |
| **Optoma ZU820T** | [`zu820t-calculateur.html`](zu820t-calculateur.html) | Implantation plafonnière : distances et tailles d'image, zoom (1,25–2,0:1), lens shift (±55 % / ±25 %), relevé au mur du fond, passage du faisceau sous l'imposte, course du pantographe. Thème clair/sombre et export du schéma (SVG / PNG). |

`index.html` est la page d'accueil qui renvoie vers les deux calculateurs.

## GitHub Pages

Le site est publié depuis la branche `main`, à la racine du dépôt.

1. **Settings → Pages**
2. *Build and deployment* → Source : **Deploy from a branch**
3. Branch : **main** / dossier **/** (root) → **Save**

L'adresse devient `https://<utilisateur>.github.io/calculateurs-videoprojection/`, et `index.html` s'ouvre par défaut (sinon `<adresse>/l9q-vertical-offset.html` et `<adresse>/zu820t-calculateur.html`).

## Utilisation locale

Ouvrir `index.html` dans un navigateur, ou servir le dossier :

```bash
python3 -m http.server 8000
# puis http://localhost:8000/
```

## Sources

- Optoma ZU820T : fiche produit et manuel utilisateur (« Lens Shift Range », offset natif).
- Écran ORION TENS et support MINI PANTOGRAPHE 30 (Dataor).
- Hisense L9Q : « Throw Distance Chart » officiel.

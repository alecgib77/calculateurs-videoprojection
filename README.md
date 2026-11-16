# Calculateurs de vidéoprojection

Petits outils d'implantation pour vidéoprojecteurs, en HTML autonome (aucune dépendance, aucun serveur : tout se calcule dans le navigateur).

**Site en ligne :** https://alecgib77.github.io/calculateurs-videoprojection/

## Calculateurs

| Calculateur | Fichier | Description |
|---|---|---|
| **Hisense L9Q** | [`l9q-vertical-offset.html`](l9q-vertical-offset.html) | Offset vertical d'un projecteur à ultra courte focale : décalage lentille → bas d'image, placement du meuble et dimensions du meuble à fabriquer. |
| **Optoma ZU820T** | [`zu820t-calculateur.html`](zu820t-calculateur.html) | Implantation plafonnière : distances et tailles d'image, zoom (1,25–2,0:1), lens shift (±55 % / ±25 %), relevé au mur du fond, passage du faisceau sous l'imposte, course du pantographe. Thème clair/sombre et export du schéma (SVG / PNG). |
| **Epson EB-L890U** | [`epson-l890u-calculateur.html`](epson-l890u-calculateur.html) | Même implantation avec l'EB-L890U : ratio 1,35–2,20:1, zoom 1,6×, lens shift ±50 % / ±20 %, écran 50–500″, boîtier 440 × 340 × 138 mm, 8,5 kg. |
| **Sharp V801U · XP-41ZL** | [`sharp-v801u-calculateur.html`](sharp-v801u-calculateur.html) | V801U équipé de l'objectif XP-41ZL : ratio 1,30–3,02:1, zoom 2,3×, lens shift +50 % / −10 % vertical, écran 50–500″, 11,2 kg + 1,8 kg d'objectif. Sens de montage réglable (à l'endroit / retourné). |
| **Panasonic PT-VMZ82** | [`panasonic-vmz82-calculateur.html`](panasonic-vmz82-calculateur.html) | Objectif fixe 1,09–1,77:1, zoom 1,6×, lens shift +44 % vers le haut / ±20 % horizontal, écran 30–300″, boîtier 399 × 115 × 348 mm, 7,4 kg. |

Les trois derniers partagent le même moteur que le ZU820T, avec en plus un champ **sens de montage** : les plages de lens shift constructeur sont données en projection bureau/face ; quand le projecteur est suspendu retourné sous la platine, la plage verticale s'inverse en repère salle (par exemple +50 % / −10 % devient 50 % vers le bas / 10 % vers le haut).

`index.html` est la page d'accueil qui renvoie vers les calculateurs.

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
- Epson EB-L890U : fiche produit, *Specifications* officielles (tableau « Screen Size and Projection Distance ») et manuel utilisateur (lens shift ±50 % / ±20 %, réduit à ±12 % vertical si le décalage horizontal est à fond).
- Sharp V801U : fiche produit, manuel utilisateur et guide d'installation (figure « lens shift adjustment range » de l'objectif XP-41ZL : +50 % / −10 % vertical, ±20 % horizontal).
- Panasonic PT-VMZ82 : spécifications officielles et manuel d'utilisation (tableau des distances, « lens shift adjustment range » 0 → +44 % vertical, ±20 % horizontal).
- Écran ORION TENS et support MINI PANTOGRAPHE 30 (Dataor).
- Hisense L9Q : « Throw Distance Chart » officiel.

Les distances sont calculées à partir du ratio constructeur × largeur d'image : l'écart avec les tableaux officiels reste inférieur à 2 % (Epson, 100″ → 2,91 m contre 2,92 m annoncés ; Sharp, 100″ → 2,80 m contre 2,80 m ; Panasonic, 100″ → 2,35 m contre 2,35 m).

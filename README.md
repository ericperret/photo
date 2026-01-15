

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

Outils légers de traitement photo, 100% client-side (HTML/JS pur, aucune dépendance).

## Outils

### Niveaux YUV (`histogram-levels-yuv2.html`)

Ajustement des niveaux de luminance dans l'espace colorimétrique YUV.

**Fonctionnalités :**
- Conversion RGB ↔ YUV (BT.601)
- Histogrammes temps réel : Luminance (Y), Chrominance U et V
- Sélection interactive début/fin sur Y (drag des poignées ou double-clic pour reset)
- Étirement automatique de la plage de luminance
- Export PNG

**Cas d'usage :** Récupérer du contraste sur des photos sous-exposées ou délavées, visualiser la distribution colorimétrique.

---

### Correction de Perspective (`perspective-correction-filtres.html`)

Redressement géométrique et filtres basiques.

**Contrôles géométriques :**
- Rotation X/Y/Z (-180° à +180°)
- Perspective (distance focale simulée)
- Échelle (0.5x à 2x)
- Inclinaison X/Y (skew)

**Filtres :**
- Inversion (négatif progressif 0-100%)
- Contraste (50-200%)

**Cas d'usage :** Redresser une photo prise en contre-plongée, corriger des lignes de fuite, numériser des documents photographiés de biais.

---

## Utilisation

1. Ouvrir le fichier HTML dans un navigateur (Chrome, Firefox, Edge)
2. Charger une image via le bouton ou drag & drop
3. Ajuster les paramètres
4. Sauvegarder le résultat

Aucune installation requise. Fonctionne hors-ligne.

## Licence

CC BY-NC 4.0 — Usage non-commercial, attribution requise.

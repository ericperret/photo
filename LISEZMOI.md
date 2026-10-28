<!--
  Nom      : LISEZMOI.md
  Objet    : Présentation du dépôt photo (outils image et géodonnées dans le navigateur)
  Auteur   : Eric Perret
  Date     : 2026-10-27
  Licence  : CC BY-NC 4.0
-->

# 📸 Photo

🇬🇧 [English version: README.md](README.md)

Six outils autonomes pour l'image et les géodonnées : un fichier HTML chacun, aucune librairie, aucune installation, fichiers lus sur le poste (rien n'est envoyé). Interfaces en français, sauf DEM Tile Downloader et GeoTIFF Inspector (titres en anglais, textes en français).

| Outil | Lancer | Rôle |
|---|---|---|
| Correction de perspective | ▶️ **[perspective-correction-filtres.html](https://ericperret.github.io/photo/perspective-correction-filtres.html)** | Redresser une photo et l'enregistrer |
| Niveaux YUV | ▶️ **[histogram-levels-yuv2.html](https://ericperret.github.io/photo/histogram-levels-yuv2.html)** | Régler les niveaux sur la luminance |
| JPEG Forensic v3 | ▶️ **[jpeg-forensic-v3.html](https://ericperret.github.io/photo/jpeg-forensic-v3.html)** | Analyser la structure et les métadonnées d'un JPEG |
| GeoTIFF / HGT Inspector | ▶️ **[geotiff_inspector.html](https://ericperret.github.io/photo/geotiff_inspector.html)** | Lire la structure d'un GeoTIFF ou d'un HGT |
| DEM Tile Downloader | ▶️ **[dem_downloader.html](https://ericperret.github.io/photo/dem_downloader.html)** | Télécharger des tuiles de modèle numérique de terrain |
| Assistant de captures | ▶️ **[captures.html](https://ericperret.github.io/photo/captures.html)** | Préparer les captures d'écran d'un organigramme |

---

## Correction de perspective

![Correction de perspective](screenshot_perspective-correction-filtres.png)

| Fonction | Description |
|---|---|
| Géométrie | Rotations X, Y, Z, perspective, échelle, inclinaisons X et Y, en direct |
| Filtres | Inversion (négatif), contraste |
| Enregistrement | PNG de l'image telle qu'affichée : projection 3D (homographie) et filtres recalculés sur les pixels, interpolation bilinéaire, fond transparent hors image |
| Réinitialiser | Retour aux réglages neutres |

## Niveaux YUV

![Niveaux YUV](screenshot_histogram-levels-yuv2.png)

| Fonction | Description |
|---|---|
| Niveaux | Bornes début / fin choisies à la main sur l'histogramme de luminance Y |
| Histogrammes | Luminance Y, chrominances U et V |
| Enregistrement | PNG de l'image traitée |

## JPEG Forensic v3

![JPEG Forensic v3](screenshot_jpeg-forensic-v3.png)

| Fonction | Description |
|---|---|
| Structure | Marqueurs JPEG (SOF, DHT, DQT…), dimensions, tables de quantification |
| Métadonnées | EXIF (IFD0, Exif, IFD1 et vignette), GPS avec localisation, IPTC, XMP, MakerNote |
| Plateforme d'origine | Détection par indices (EXIF retiré, ICC, tables de quantification, dimensions, XMP) : Facebook, Instagram, Twitter / X, WhatsApp, Telegram, Discord, Snapchat, image originale ou partiellement nettoyée, avec niveau de confiance |

## GeoTIFF / HGT Inspector

![GeoTIFF / HGT Inspector](screenshot_geotiff_inspector.png)

| Fonction | Description |
|---|---|
| Lecture | IFD TIFF, GeoKeys et tags GDAL, sans charger l'image |
| Formats | TIFF classique, BigTIFF, COG, HGT |
| Sortie | Dump texte copiable (pour une analyse ou une IA) |

## DEM Tile Downloader

![DEM Tile Downloader](screenshot_dem_downloader.png)

| Fonction | Description |
|---|---|
| Tuile | Saisie latitude / longitude, nommage par le coin sud-ouest (convention SRTM / Copernicus) |
| Fournisseurs | SRTM GL1 v3 (NASA Earthdata, compte requis), Copernicus DEM GLO-30 (AWS S3, libre), OpenTopography (clé API) |
| Liens | Liens de téléchargement directs construits pour la tuile |

## Assistant de captures

![Assistant de captures](screenshot_captures.png)

Outil d'appui à la documentation de la plateforme SEG973 (csvgen) : parcourt la liste des modules d'`organigramme.html`, attend un Ctrl+V, propose un recadrage à la souris, un format et une compression avec aperçu du poids, produit le bloc `SHOTS` à coller (`shots.js`), permet de reprendre un travail commencé et d'enregistrer chaque image.

---

## Historique

| Outil | Version | Évolution |
|---|---|---|
| Correction de perspective | 1.1 | Enregistrement corrigé : l'image sauvegardée était l'original non modifié (réglages appliqués en CSS seulement) ; téléchargement fiabilisé |
| Niveaux YUV | 2.1 | Téléchargement fiabilisé |
| Niveaux YUV | 2.3 | Bornes neutres (0 / 255) au chargement d'une image et à la réinitialisation : l'image n'est plus assombrie d'office et les poignées correspondent aux valeurs affichées |
| Niveaux YUV | 2.4 | Poignées de l'histogramme Y : position de la souris ramenée à l'échelle du canevas (affiché plus étroit que ses 512 px) ; la poignée de droite se saisit de nouveau et va jusqu'à 255 |
| Les six outils | 2026-10-18 | Charte graphique AZS : palette ardoise / ambre / cyan, bandeau AZS avec lien de retour vers www.azs.fr, thème sombre pour les niveaux YUV et la correction de perspective ; captures refaites |

## Licence

**Usage libre non commercial** — [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.fr), avec mention obligatoire de la source et de l'auteur :

> photo — Eric PERRET — https://github.com/ericperret/photo

Toute utilisation commerciale est interdite sans autorisation écrite de l'auteur, à demander par courriel : **eperret@azs.fr**.
Conditions complètes (français / anglais) : [LICENSE](LICENSE).

## Auteur

**Eric Perret** — [GitHub](https://github.com/ericperret)

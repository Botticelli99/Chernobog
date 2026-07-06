BLACK SUN ARCHIVE — CHERNOBOG
=============================

COMMENT PUBLIER SUR GITHUB PAGES
---------------------------------
1. Renomme ce dossier comme tu veux, par exemple : chernobog-site
2. Envoie tout le contenu du dossier sur GitHub :
   - index.html
   - css/
   - js/
   - images/
   - audio/
3. Dans GitHub :
   Settings > Pages
   Source : Deploy from a branch
   Branch : main
   Folder : /root
4. Ton site sera disponible à :
   https://TON-PSEUDO.github.io/NOM-DU-DEPOT/


STRUCTURE DU PROJET
-------------------
index.html
  La structure principale du site.

css/style.css
  Toute l'apparence :
  - les panneaux
  - les boutons [+]
  - la fiche d'archive
  - le lecteur audio
  - le responsive

js/app.js
  Toute la logique :
  - navigation sans rechargement
  - remplacement de l'image de droite
  - ouverture de la fiche d'archive
  - maintien de la musique

audio/theme.mp3
  Mets ta musique ici.
  Si ton fichier a un autre nom, modifie dans index.html :
  audio/theme.mp3

images/pages/
  Dossier prévu pour tes futures pages en .webp ou .png.
  Pour l'instant, plusieurs images sont encore intégrées en Base64 dans js/app.js.


MODIFIER LES BOUTONS [+]
------------------------
Dans index.html, cherche :
data-archive-title
data-archive-text

Exemple :
data-archive-title="Personnalité"
data-archive-text="Ton long texte ici..."


AJOUTER UNE PAGE
----------------
1. Ajoute un bouton dans le menu gauche :
   <a href="#pouvoirs" data-page="pouvoirs">Pouvoirs</a>

2. Ajoute l'image dans images/pages/
   images/pages/pouvoirs.webp

3. Dans js/app.js, remplace ou ajoute :
   pouvoirs: "images/pages/pouvoirs.webp"


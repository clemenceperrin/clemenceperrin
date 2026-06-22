# Ma page académique — Guide de déploiement

## Architecture des fichiers

```
mon-site/
├── index.html              ← Page principale (tout le contenu est ici)
├── assets/
│   ├── css/
│   │   └── style.css       ← Tout le design est ici
│   └── images/
│       └── photo.jpg       ← Ta photo de profil (à remplacer)
└── README.md
```

---

## 1. Créer le repo GitHub

1. Va sur [github.com](https://github.com) et connecte-toi
2. Clique sur **"New repository"** (bouton vert en haut à droite)
3. Nomme-le exactement : `TONPSEUDO.github.io`  
   *(remplace TONPSEUDO par ton nom d'utilisateur GitHub)*
4. Coche **"Public"**
5. Clique **"Create repository"**

---

## 2. Uploader les fichiers

### Option A — Via l'interface web (le plus simple)

1. Dans ton nouveau repo, clique **"Add file" > "Upload files"**
2. Glisse-dépose le fichier `index.html`
3. Commit : clique **"Commit changes"**
4. Crée le dossier `assets/css/` :
   - Clique **"Add file" > "Create new file"**
   - Dans le nom, tape : `assets/css/style.css`
   - Colle le contenu du fichier `style.css`
   - Commit
5. Upload ta photo :
   - **"Add file" > "Upload files"**
   - Navigue dans `assets/images/`
   - Upload ta photo et renomme-la `photo.jpg`

### Option B — Via Git (en ligne de commande)

```bash
git clone https://github.com/TONPSEUDO/TONPSEUDO.github.io
cd TONPSEUDO.github.io
# Copie tes fichiers ici, puis :
git add .
git commit -m "Initial academic website"
git push
```

---

## 3. Activer GitHub Pages

1. Dans ton repo, va dans **Settings** (onglet en haut)
2. Dans le menu gauche, clique **"Pages"**
3. Sous **"Source"**, sélectionne **"Deploy from a branch"**
4. Branche : **"main"** (ou "master"), dossier : **"/ (root)"**
5. Clique **"Save"**

→ Ton site sera en ligne sur `https://TONPSEUDO.github.io` en 1–2 minutes.

---

## 4. Personnaliser le contenu

Ouvre `index.html` et remplace :

| Placeholder | Par quoi le remplacer |
|---|---|
| `Prénom Nom` | Ton vrai nom |
| `prenom.nom@institution.fr` | Ton email |
| `votre-profil` (LinkedIn) | Ton URL LinkedIn |
| `Titre de votre article...` | Tes vraies publications |
| Texte "About" | Ta vraie bio |
| `assets/cv.pdf` | Ton CV en PDF (à uploader) |

---

## 5. Ajouter ton CV PDF

1. Dans ton repo GitHub, crée le dossier `assets/` s'il n'existe pas
2. Upload ton fichier CV et nomme-le `cv.pdf`
3. Le bouton "Télécharger le CV" dans la page fonctionnera automatiquement

---

## Questions fréquentes

**Ma photo ne s'affiche pas ?**  
→ Vérifie que le fichier s'appelle bien `photo.jpg` (en minuscules) et qu'il est dans `assets/images/`.

**Mon site n'apparaît pas après 5 minutes ?**  
→ Va dans Settings > Pages et vérifie que GitHub Pages est bien activé sur la branche `main`.

**Je veux changer les couleurs ?**  
→ Ouvre `assets/css/style.css` et modifie les valeurs dans la section `:root { }` tout en haut.

# 📖 Comment modifier le site — Guide simple

Pas besoin d'être informaticienne ! Voici comment mettre à jour votre site en quelques clics.

---

## 🔑 Le fichier magique : `data/articles.json`

C'est le **seul fichier à modifier** pour gérer votre boutique.

---

## ✏️ Modifier les infos de l'atelier

Ouvrez `data/articles.json` et changez la section du haut :

```json
"atelier": {
    "nom": "L'Atelier du Fil",              ← Nom affiché partout
    "slogan": "Votre slogan ici",           ← Phrase sous le logo
    "description": "Votre texte ici...",   ← Paragraphe de présentation
    "instagram": "@votrepseudo"            ← Votre pseudo Instagram (avec le @)
}
```

---

## 🛍️ Ajouter un nouvel article

Copiez-collez ce bloc dans la liste `articles`, en changeant les valeurs :

```json
{
    "id": 5,                          ← Numéro unique (différent des autres)
    "nom": "Nom de votre article",
    "description": "Description de l'article...",
    "photo": "/images/ma-photo.jpg",  ← Nom de votre photo (voir ci-dessous)
    "prix": "35€",
    "badge": "Nouveau",               ← Ou mettre null si pas de badge
    "couleurs": [
        { "nom": "Beige", "hex": "#F5F0E8" },
        { "nom": "Bleu", "hex": "#4A90D9" }
    ]
}
```

> ⚠️ N'oubliez pas d'ajouter une virgule après l'accolade `}` du bloc précédent !

---

## 📸 Ajouter une photo

1. Nommez votre photo simplement : `mon-sac.jpg`
2. Déposez-la dans le dossier **`images/`** de votre projet GitHub
3. Dans le JSON, mettez : `"photo": "/images/mon-sac.jpg"`

**Conseils photo :**
- Format JPG ou PNG
- Ratio portrait (4:5) conseillé
- Fond neutre (blanc ou gris clair) pour un rendu élégant
- Taille max 2 Mo

---

## 🎨 Couleurs : comment trouver le code hexadécimal ?

1. Allez sur 👉 [htmlcolorcodes.com/fr](https://htmlcolorcodes.com/fr)
2. Choisissez votre couleur dans le sélecteur
3. Copiez le code qui commence par `#` (ex: `#FF5733`)
4. Collez-le dans le JSON : `"hex": "#FF5733"`

---

## 🏷️ Les badges disponibles

| Ce que vous écrivez | Ce qui s'affiche |
|---------------------|-----------------|
| `"badge": "Nouveau"` | Étiquette "Nouveau" |
| `"badge": "Bestseller"` | Étiquette "Bestseller" |
| `"badge": "Soldes"` | Étiquette "Soldes" |
| `"badge": null` | Pas d'étiquette |

---

## ❌ Supprimer un article

Effacez tout le bloc `{ ... }` correspondant à cet article dans la liste.

---

## 💾 Sauvegarder et mettre en ligne

Après avoir modifié le fichier sur GitHub :
1. Faites défiler vers le bas
2. Cliquez sur le bouton vert **"Commit changes"**
3. ✅ Votre site se met à jour automatiquement en **1 à 2 minutes** !

---

## 🆘 En cas de problème

Si le site affiche une erreur après vos modifications, c'est probablement une faute de syntaxe JSON. Vérifiez :
- ✅ Chaque `"valeur"` est entre guillemets doubles
- ✅ Il y a une virgule entre chaque article (mais PAS après le dernier)
- ✅ Les accolades `{` et `}` sont bien fermées

Vous pouvez vérifier votre JSON sur 👉 [jsonlint.com](https://jsonlint.com)

---

*Site créé avec ❤️ — Thème Blanc / Noir / Doré*

# Advanced HTML – Techium

Projet Holberton School : construire la structure HTML complète d'un site fictif, **Techium**, une agence digitale.
Il n'y a **aucun CSS** : la page est volontairement « moche ». Le but est d'apprendre à **structurer** une page avec les bonnes balises, pas à la décorer.

> **HTML décrit le sens du contenu. CSS s'occupe de son apparence.**

---

## Vocabulaire de base

| Mot | Signification | Exemple |
|---|---|---|
| **Balise** | Un mot entre chevrons qui ouvre ou ferme un élément | `<p>` … `</p>` |
| **Élément** | Une balise ouvrante, son contenu et sa balise fermante | `<p>Bonjour</p>` |
| **Attribut** | Une information supplémentaire écrite dans la balise ouvrante | `lang="en"` |
| **Parent / enfant** | Un élément placé à l'intérieur d'un autre est son enfant | `<ul>` est le parent de `<li>` |
| **Frères (siblings)** | Des éléments au même niveau, dans le même parent | `header`, `main` et `footer` |
| **Sémantique** | Une balise qui dit **à quoi sert** son contenu | `<nav>` = menu de navigation |
| **Balise auto-fermante** | Une balise sans contenu, donc sans fermeture | `<img>`, `<meta>`, `<hr>`, `<br>` |

---

## Les fichiers du projet

- `0-index.html` à `36-index.html` : les étapes successives de la page d'accueil.
- `index.html` : la **page d'accueil finale**.
- `11-styleguide.html` à `39-styleguide.html` : les étapes successives de la styleguide.
- `styleguide.html` : la **styleguide finale**, une page de référence qui montre chaque élément HTML du site.
- `article.html`, `about.html`, `latest_news.html`, `contact.html` : les autres pages du site.
- `favicon.ico`, `favicon.png` : l'icône affichée dans l'onglet du navigateur.
- `logo-black.png` : le logo de Techium.
- `images/` : les photos des sections.

---

## Les tâches, une par une

### 0. Create your first webpage — `0-index.html`
- `<!DOCTYPE html>` : dit au navigateur « ceci est du HTML5 moderne ». Sans lui, il passe en *mode quirks* et imite les bugs des vieux navigateurs. Il se place **tout en haut, sans commentaire avant**.
- `<html>` : la **racine**, la boîte qui contient toute la page. Seul le doctype est en dehors.
- `lang="en"` : la langue, en code ISO à deux lettres. Elle sert aux lecteurs d'écran (prononciation), aux traducteurs et à Google.
- `dir="ltr"` : le sens de lecture (*left to right*). `rtl` sert pour l'arabe ou l'hébreu.

### 1. Structure your webpage — `1-index.html`
- `<head>` : les informations **sur** la page, invisibles à l'écran (l'enveloppe d'une lettre).
- `<body>` : tout ce que l'utilisateur **voit** (la lettre elle-même).
- Le `head` vient toujours **avant** le `body`, car le navigateur lit de haut en bas et doit connaître les réglages avant le contenu.

### 2. The head — `2-index.html`
- `<meta charset="utf-8">` : l'encodage des caractères. Il évite que « Café » s'affiche « CafÃ© ». Il se place **en premier** dans le `head`.
- `<meta name="viewport" ...>` : adapte la page aux mobiles (vraie largeur de l'écran, pas de zoom au départ).
- `<title>` : le texte de l'onglet et du titre dans Google.
- `<meta name="description" ...>` : le résumé affiché sous le titre dans Google. `name` dit **de quoi** on parle, `content` donne **la valeur**.
- `<link rel="icon" ...>` : le favicon. On en met deux, `.ico` (compris partout) et `.png` (moderne).

### 3. Simple header, main, footer — `3-index.html`
- `<header>` : le haut de la page (logo, menu), souvent identique sur toutes les pages.
- `<main>` : le contenu **unique** de cette page. Un seul par page.
- `<footer>` : le bas de la page (copyright, contact, réseaux).
- Ce sont des balises **sémantiques** : elles s'affichent comme une simple boîte, mais disent à quoi sert leur contenu. Ce sont trois frères dans le `body`.

### 4. Aside — `article.html`
- Une **nouvelle page** du site, donc un nouveau nom de fichier et un nouveau `title`.
- `<aside>` : un contenu **lié mais secondaire**, qu'on peut retirer sans perdre le sens (comme l'encadré « Le saviez-vous ? » d'un manuel). Il est placé dans le `main`.

### 5. Section — `5-index.html`
- `<section>` : regroupe un contenu **par thème**, comme un chapitre.
- Règle simple : *si on peut donner un titre au bloc, c'est une `section`*.
- Sept sections : Hero (la grande bannière d'accueil), Services, Works, About, Latest news, Testimonials et Contact.

### 6. Work, News, Testimonial articles — `6-index.html`
- `<article>` : un contenu **autonome**, qui garde son sens même publié seul ailleurs (un post de blog, un avis client).
- Une `section` est l'étagère, les `article` sont les livres posés dessus.

### 7. Navigation — `7-index.html`
- `<nav>` : le bloc des **liens principaux** du site (le menu). Il est placé dans le `header`.
- On le réserve aux grands blocs de navigation, pas à un lien isolé.

### 8. Level 1 headings — `8-index.html`
- `<h1>` : le **titre principal** de la page. **Un seul par page**, comme le titre sur la couverture d'un livre.
- Il décrit le contenu de la page, pas le nom du site.

### 9. Level 2 headings — `9-index.html`
- `<h2>` : les titres des sections, juste sous le `h1` dans la hiérarchie.

### 10. Level 3 headings — `10-index.html`
- `<h3>` : les sous-titres à l'intérieur des sections.
- On respecte toujours l'ordre `h1` > `h2` > `h3`, **sans sauter de niveau**. Les lecteurs d'écran s'en servent comme d'une table des matières.

### 11. Styleguide — `11-styleguide.html`
- Une **styleguide** est une page de démonstration qui montre chaque élément du site pour vérifier son apparence.
- On y affiche les six niveaux de titres, de `h1` à `h6`.
- Un `header` peut servir d'en-tête à une `section`, pas seulement à la page entière.

### 12. Paragraphs — `12-index.html`
- `<p>` : un **paragraphe** de texte.
- Il ne sert pas à grouper des éléments : pour cela, on utilise une `div`.

### 13. Styleguide paragraphs — `13-styleguide.html`
- Un exemple de titre suivi d'un sous-titre et d'un paragraphe dans la styleguide.

### 14. Span — `14-index.html`
- `<span>` : un conteneur **en ligne** (*inline*) et **sans signification**, pour entourer un bout de texte.
- Ici, il porte le nom « Techium » qui sert de logo texte.

### 15. Div — `15-index.html`
- `<div>` : un conteneur **bloc** sans signification, utilisé pour la mise en page (CSS) plus tard.
- **`div` ou `span` ?** La `div` crée un bloc qui prend toute la largeur, le `span` reste dans la ligne du texte.
- La `div` se place **à l'intérieur** des balises sémantiques et ne les remplace jamais.

### 16. Structure your sections — `16-index.html`
- Chaque section est découpée en un `header` (titre et sous-titre) et une `div` (le contenu).
- Une structure identique partout rend le code prévisible et facile à styliser.

### 17. Comments — `17-index.html`
- `<!-- Texte -->` : un **commentaire**, invisible sur la page, qui sert au développeur à repérer les blocs.
- Une ligne vide avant chaque commentaire aère le code.

### 18. Link your logo — `18-index.html`
- `<a href="/">` : un **lien**. Ici, le logo ramène à la racine du site, c'est-à-dire l'accueil.
- `href` donne la destination du lien.

### 19. Create new pages — `about.html`, `latest_news.html`, `contact.html`
- Trois nouvelles pages, copies de la page d'accueil avec un `title` adapté.

### 20. Add links — `20-index.html`
- Les liens du menu. `href="#services"` est une **ancre** : elle mène à un endroit précis de la même page.

### 21. Add social media links — `21-index.html`
- Des liens vers des sites externes avec une **URL absolue** (adresse complète commençant par `https://`).

### 22. "Button" links — `22-index.html`
- Des liens d'appel à l'action (« Get started », « Get in touch »), qui ressembleront à des boutons une fois stylisés.
- `href="about.html"` est une **URL relative** : un fichier du même site.

### 23. Services, Works, Latest news links — `23-index.html`
- Un lien `<a>` placé **à l'intérieur** de chaque `h3` rend le titre cliquable sans lui faire perdre son rôle de titre.

### 24. List the links — `24-index.html`
- `<ul>` (liste non ordonnée) et `<li>` (élément de liste) : une suite de liens **est** une liste, donc on l'écrit comme une liste.
- Les lecteurs d'écran annoncent alors « liste de 7 éléments ».

### 25. Secondary navigation menu — `25-index.html`
- Un second menu dans le `footer` (mentions légales, confidentialité, cookies).

### 26. Examples of lists — `26-styleguide.html`
- `<ul>` : liste à puces, quand l'ordre n'a pas d'importance.
- `<ol>` : liste numérotée, quand l'ordre compte (comme les étapes d'une recette).
- `<dl>`, `<dt>`, `<dd>` : liste de définitions (un terme, puis sa définition), comme un dictionnaire.

### 27. Separate content — `27-index.html`
- `<hr>` : une **séparation thématique** entre deux blocs de contenu, pas un simple trait décoratif.
- Le paragraphe de copyright se place juste après.

### 28. Horizontal rule example — `28-styleguide.html`
- Un exemple de `hr` dans la styleguide.

### 29. Client quotes — `29-index.html`
- `<blockquote>` : une **citation longue**, en bloc.
- `<cite>` : la source de la citation (ici, l'auteur de l'avis).

### 30. Examples of quotes — `30-styleguide.html`
- `<q>` : une **citation courte**, dans la ligne du texte. Le navigateur ajoute les guillemets tout seul.
- `<blockquote>` : la version longue, en bloc.

### 31. Address and latest news authors — `31-index.html`
- `<address>` : des **coordonnées de contact** (adresse, e-mail).
- `<br>` : un retour à la ligne **dans** un texte. On ne l'utilise jamais pour créer de l'espace : c'est le rôle du CSS.
- `<small>` : un texte annexe ou secondaire (auteur, mentions légales).

### 32. Typography — `32-styleguide.html`
- `<address>` : une adresse avec un retour à la ligne.
- `<pre>` : conserve exactement les espaces et retours à la ligne du texte. `<code>` indique du code informatique.
- `<mark>` : un texte **surligné**, mis en évidence pour le lecteur.

### 33. Table — `33-styleguide.html`
- `<table>` : un tableau de **données**, à ne pas utiliser pour la mise en page.
- `<caption>` : le titre du tableau, important pour l'accessibilité.
- `<thead>` / `<tbody>` : l'en-tête et le corps du tableau.
- `<tr>` : une ligne. `<td>` : une cellule. `<th>` : une cellule d'en-tête.
- `scope="col"` / `scope="row"` : indique si l'en-tête concerne une **colonne** ou une **ligne**, pour les lecteurs d'écran.

### 34. Details — `34-styleguide.html`
- `<details>` : un bloc **repliable** (un accordéon), sans JavaScript.
- `<summary>` : le texte cliquable toujours visible.
- L'attribut `open` affiche le bloc déplié par défaut.

### 35. Replace text logo with image logo — `35-index.html`
- `<img>` : une image. Balise auto-fermante.
- `src` : le chemin du fichier.
- `alt` : le texte alternatif, lu par les lecteurs d'écran et affiché si l'image ne charge pas.
- `width` / `height` : les dimensions, pour que la page ne « saute » pas pendant le chargement de l'image.

### 36. Add images to your sections — `36-index.html`
- Des images dans les sections, rangées dans le dossier `images/`.
- `alt=""` (vide) pour les images **décoratives** : le lecteur d'écran les ignore. Les avatars ont un `alt` descriptif, car ils identifient une personne.
- **Formats d'image :**
  - **JPG** : les photos (léger, mais avec une petite perte de qualité).
  - **PNG** : les logos et images avec transparence (sans perte).
  - **GIF** : les petites animations (limité à 256 couleurs).
  - **SVG** : les icônes et logos **vectoriels**, nets à toutes les tailles.

### 37. Social icons — `index.html` (page finale)
- `<svg>` : une image **vectorielle** écrite directement en code, qui reste nette à toutes les tailles.
- `<title>` dans le SVG : son nom, pour l'accessibilité.
- Le tracé (`path d="..."`) doit être recopié **exactement**.

### 38. Video player — `38-styleguide.html`
- `<video>` : un lecteur vidéo intégré au navigateur.
- `controls` : affiche les boutons (lecture, volume…).
- `loop` : relance la vidéo à la fin.
- `poster` : l'image affichée avant la lecture.
- Le texte placé entre les balises s'affiche si le navigateur ne gère pas la vidéo.

### 39. Audio player — `39-styleguide.html`
- `<audio>` : un lecteur audio, avec `controls` et un texte de secours, sur le même principe que la vidéo.

### 40. Iframe — `styleguide.html` (styleguide finale)
- `<iframe>` : affiche une **autre page web à l'intérieur** de la page (ici, une vidéo YouTube).
- `title` : obligatoire pour l'accessibilité.
- À utiliser avec modération, car chaque iframe alourdit la page.

---

## À retenir

1. **Chaque balise a un sens** : choisir la bonne aide les lecteurs d'écran, Google et les autres développeurs.
2. **`div` et `span` n'ont aucun sens** : on les utilise seulement quand aucune balise sémantique ne convient.
3. **La hiérarchie des titres** (`h1` > `h2` > `h3`) ne saute jamais de niveau.
4. **Toujours un `alt`** sur les images, vide si l'image est décorative.
5. **HTML structure, CSS décore.**

---

## Auteur

**Mathieu Bailliez** – Holberton School

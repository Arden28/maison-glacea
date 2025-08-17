# Glacéa — Site vitrine (HTML + Tailwind + Alpine)

> **FR · English below**

Un site vitrine léger, élégant et ambitieux pour **Glacéa** — une maison de glace créative en France. L’objectif : **poser une identité forte**, raconter **l’histoire et la fondatrice**, et donner envie de **suivre le projet** (lancement pilote prévu **été 2026**), sans activer la vente en ligne.

---

## 🚀 Aperçu

* **Mono‑fichier `index.html`** prêt à déployer
* **Tailwind (CDN)** + **Alpine.js** pour l’interactivité minimale
* **Design** : rue & raffinement, réalité & rêve, sobriété & impact
* **Sections** : Univers · Manifeste · Histoire · Fondatrice · Feuille de route · Contact
* **Logo** : symbole SVG inline + exports PNG/SVG
* **Accessibilité & performance** : images lazy‑load (+ fallback), dark mode, SEO de base, JSON‑LD

---

## 🧱 Stack & dépendances

* **HTML5** (mono‑page)
* **TailwindCSS** via CDN (`<script src="https://cdn.tailwindcss.com">`)
* **Alpine.js** via CDN (state et petits comportements)
* **Google Fonts** : Sora

> Aucun build ni Node requis. Optionnellement, vous pouvez migrer vers une config Tailwind “JIT build” si vous souhaitez purger/optimiser encore plus.

---

## 📂 Structure

```
project/
├─ index.html                # Le site (canvas)
├─ assets/
│  └─ logo/
│     ├─ glacea_logo.svg     # Logo vectoriel
│     ├─ glacea_logo_1024.png
│     ├─ glacea_logo_512.png
│     └─ glacea_logo_256.png
└─ README.md                 # Ce fichier
```

> Les PNG/SVG ont été fournis dans la conversation. Placez‑les dans `assets/logo/` et mettez à jour les chemins si vous les utilisez dans le HTML.

---

## ▶️ Démarrer en local

1. Téléchargez `index.html` et ouvrez‑le dans votre navigateur.
2. (Optionnel) Servez‑le via un petit serveur statique pour de meilleures prévisions cache :

   ```bash
   python3 -m http.server 8080
   ```
3. Ouvrez `http://localhost:8080`.

---

## 🎨 Identité & logo

* Le **logomark** est défini en **SVG inline** dans `index.html` via `<symbol id="glacea-mark">` et un **dégradé** `#glaceaGrad`.
* Pour l’utiliser :

  ```html
  <svg width="40" height="40" viewBox="0 0 64 64" aria-hidden="true">
    <use href="#glacea-mark" />
  </svg>
  ```
* Exports : `assets/logo/glacea_logo.svg` + PNG (1024/512/256). Déconseillé de recolorer le dégradé sans cohérence UI.

**Couleurs brand** : éditables dans le bloc Tailwind config (script en `<head>`), clé `theme.extend.colors.glacea` (+ `strawberry`, `mango`, `pistachio`).

---

## ✏️ Contenu & sections

* **Univers** : moodboard des parfums (prototypes, pas de vente).
* **Manifeste** : piliers (goût vrai, créatif, inclusif, local).
* **Histoire** : vision et chemin vers 2026.
* **Fondatrice** : jeune femme noire, ambitieuse, origines modestes; citation; CTA presse/collab.
* **Feuille de route** : étapes 2025 → 2027.
* **Contact** : newsletter + canaux pros (à personnaliser).

Mettez à jour : emails (`bonjour@glacea.fr`, `invest@glacea.fr`), villes des pop‑ups, textes et photos.

---

## 🖼️ Images

* Placeholders **Unsplash** (libres d’usage, mais l’idéal est d’utiliser vos propres visuels ou images sous licence).
* **Fallback visuel** automatique (dégradé Glacéa) si une image échoue (`<script>` en bas de page).
* **Performance** : lazy‑load par défaut (`loading="lazy"`) ; le **hero** est priorisé (`loading="eager"`, `fetchpriority="high"`).
* **Accessibilité** : alt précis (ex. fondatrice : “jeune femme noire”).

---

## ♿ Accessibilité (A11y)

* Contrastes vérifiés sur les principaux éléments
* Focus visible ; boutons cliquables au clavier
* Libellés/`aria-label` pour les icônes d’UI
* Dark mode conservé via `localStorage`

---

## 🔎 SEO & partage

* Titres/description `<meta>` adaptés
* **Open Graph** image (à remplacer par une image de marque dédiée)
* **JSON‑LD** (`Brand`) avec date, zone et description
* Conseillé : ajouter `sitemap.xml` et `robots.txt`

---

## 🚢 Déploiement

* **GitHub Pages** : push puis activez Pages sur la branche par défaut.
* **Netlify / Vercel** : déposez le repo ; build = none, output = racine.
* **Headers** recommandés : cache statique 1 an pour images et logo, HTML no‑cache pendant la phase de construction.

---

## 🔧 Personnalisation

* **Couleurs** : `tailwind.config` embarqué (script en head)
* **Typo** : Google Font Sora (pouvant être auto‑hébergée)
* **Navigation** : liens ancrés ; renommez les sections au besoin
* **Formulaire** : la newsletter utilise `alert()` par défaut — branchement conseillé : **Brevo/Mailjet/Plausible forms** ou un simple **Formspree** sans cookies.
* **Analytique sans cookies** (RGPD) : **Plausible**, **Matomo**, **Umami**.

---

## ✅ To‑do / prochaines étapes

* [ ] Remplacer tous les placeholders images par vos visuels
* [ ] Créer une **Open Graph card** dédiée (1024×536) signée Glacéa
* [ ] Ajouter **favicon** (16/32) + **Apple Touch Icon** (180) depuis `glacea_logo_1024.png`
* [ ] Brancher la newsletter (Brevo/Mailjet) et page **merci**
* [ ] Créer une page **Kit presse** (logo, photos, bio fondatrice)
* [ ] Internationalisation EN (facile en dupliquant les blocs)
* [ ] (Optionnel) Migration **Next.js + CMS** (Sanity/Contentful) pour éditer contenus

---

## ⚖️ Licence & droits

* **Code** : MIT
* **Logo & marque Glacéa** : © Tous droits réservés (usage restreint)
* **Photos** : remplacez par des visuels avec droits clairs (vos photos, banque d’images, etc.)

---

## 🙌 Crédits

* TailwindCSS · Alpine.js · Google Fonts
* Placeholders image : Unsplash

---

## English (brief)

**Glacéa** is a stylish one‑page **showcase site** (no e‑commerce) built with **HTML + Tailwind (CDN) + Alpine.js**. It introduces the brand, story, and founder, building momentum ahead of a **Summer 2026** pilot.

### Features

* Single file `index.html`, inline SVG logo, lazy‑loaded images with a graceful fallback
* Sections: Universe, Manifesto, Story, **Founder**, Roadmap, Contact
* Basic SEO (Open Graph + JSON‑LD), dark mode, a11y touch‑ups

### Getting started

Just open `index.html` in your browser or serve statically:

```bash
python3 -m http.server 8080
```

### Customize

Edit Tailwind colors in the inline config; replace emails, texts, and Unsplash placeholders with your assets. Newsletter uses `alert()` — wire to your provider.

### Assets & License

SVG + PNG logo exports included (`assets/logo/`). Code under MIT (or your choice). Brand & logo © All rights reserved.

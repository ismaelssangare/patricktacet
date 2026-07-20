# Site — Maître Patrick Tacet

Site vitrine pour Maître Patrick Tacet, avocat au Barreau de Laon, médiateur et enseignant.

Site 100% statique (HTML/CSS, sans framework, sans backend). Déployé sur Vercel et versionné sur GitHub : [github.com/ismaelssangare/patricktacet](https://github.com/ismaelssangare/patricktacet).

## Installation

Aucune dépendance n'est requise pour ce projet. Un seul prérequis si tu veux utiliser les commandes ci-dessous :

- [Node.js](https://nodejs.org/) (version 18 ou plus récente) — uniquement pour lancer un petit serveur local, pas pour builder le site.

Clone le dépôt puis installe (il n'y a rien à installer, cette étape ne fait rien de plus que vérifier que tout est en place) :

```bash
git clone https://github.com/ismaelssangare/patricktacet.git
cd patricktacet
npm install
```

## Lancer le site en local

```bash
npm run dev
```

Le site sera accessible sur [http://localhost:3000](http://localhost:3000).

Alternative sans Node : ouvre simplement le fichier `index.html` dans ton navigateur.

## Variables d'environnement

Ce site n'utilise actuellement **aucune** variable d'environnement — c'est du HTML/CSS statique, sans clé API ni service externe connecté.

Le fichier `.env.example` liste les emplacements prévus pour le jour où une fonctionnalité (formulaire de contact connecté à un service externe, carte Google Maps, etc.) en aurait besoin. Si tu ajoutes une telle clé un jour :

1. Copie `.env.example` vers `.env` : `cp .env.example .env`
2. Remplis `.env` avec les vraies valeurs (ce fichier est ignoré par Git, il ne sera jamais poussé sur GitHub)
3. Ajoute les mêmes variables dans Vercel : Project Settings → Environment Variables

## Déploiement sur Vercel

Le projet est déjà connecté : chaque `git push` sur la branche `main` déclenche automatiquement un nouveau déploiement de production sur Vercel (projet `patricktacet`, domaine [patricktacet.vercel.app](https://patricktacet.vercel.app)).

Pour vérifier ou reconfigurer cette connexion :

1. Va sur [vercel.com](https://vercel.com) → projet **patricktacet** → **Settings** → **Git**
2. Vérifie que le dépôt connecté est bien `ismaelssangare/patricktacet`, branche `main`
3. Si ce n'est pas le cas, clique sur **Connect Git Repository** et sélectionne ce dépôt

Aucune configuration de build n'est nécessaire (pas de framework détecté, le site est servi tel quel).

## Structure du projet

```
patricktacet/
├── index.html                     # Page principale du site
├── mentions-legales.html          # Page mentions légales
├── politique-confidentialite.html # Page politique de confidentialité
├── package.json                   # Script de lancement local uniquement
├── .env.example                   # Modèle des variables d'environnement (aucune requise actuellement)
├── .gitignore
└── README.md
```

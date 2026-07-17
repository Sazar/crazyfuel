# 🚗⛽ CrazyFuel

> Carte interactive temps réel des prix des carburants en France — avec espace communautaire et dashboard administrateur.

[![Live Demo](https://img.shields.io/badge/demo-frontend-teal?style=flat-square)](https://github.com/Sazar/crazyfuel)
[![Stack](https://img.shields.io/badge/stack-HTML%2FCSS%2FJS-orange?style=flat-square)]()
[![Map](https://img.shields.io/badge/map-Leaflet-green?style=flat-square)]()

---

## ✨ Fonctionnalités

### 🗺️ Carte interactive
- Affichage de toutes les stations-service de France sur une carte OpenStreetMap via Leaflet
- Filtrage par **carburant** (Gazole, SP95, SP95-E10, SP98, GPLc, E85)
- Filtrage par **ville ou enseigne**, **prix maximum**, **tri** (prix, distance, nom)
- Clic sur un marqueur → détail complet de la station avec tous ses prix et ses commentaires validés

### 🏆 Top 3 national & proximité
- **Top 3 national** : les 3 stations les moins chères en France pour le carburant préféré du profil
- **Top 3 proximité** : les 3 stations les moins chères parmi les plus proches de la position GPS de l’utilisateur
- Mis à jour automatiquement dès qu’une correction de prix est approuvée par l’admin

### 👤 Compte utilisateur
- Création de compte avec **carburant préféré**
- Le carburant du profil pilote les classements Top 3 en temps réel
- Historique de session (sans backend persistant en version demo)

### 💬 Communauté
- **Commentaires** sur les stations (soumis en modération avant publication)
- **Propositions de correction de prix** avec justification (soumises en modération)
- Affichage des commentaires validés par station et dans le fil communautaire

### 🛡️ Dashboard administrateur
- **File de modération** : tous les commentaires et corrections en attente
- **Approuver** → publie immédiatement le commentaire ou met à jour le prix sur la carte
- **Refuser** → supprime la contribution de la file
- **Journal d’activité** : historique complet des actions admin

---

## 🖼️ Stack technique

| Couche | Technologie |
|---|---|
| Front-end | HTML5 / CSS3 (custom properties) / Vanilla JS |
| Carte | [Leaflet.js](https://leafletjs.com/) + OpenStreetMap tiles |
| Fonts | Fontshare (Cabinet Grotesk + Satoshi) |
| Rendu | Single-page app, navigation par vue |
| Backend (prod) | À connecter : API prix carburants + BDD + Auth |

---

## 🚀 Lancer le projet

```bash
# Cloner le repo
git clone https://github.com/Sazar/crazyfuel.git
cd crazyfuel

# Ouvrir directement dans le navigateur
open crazyfuel.html
# ou avec un serveur local :
npx serve .
```

Aucune dépendance npm requise. Toutes les librairies sont chargées via CDN.

---

## 📁 Structure

```
crazyfuel/
├── crazyfuel.html   # Application complète (SPA)
└── README.md        # Ce fichier
```

---

## 🔌 Intégration production recommandée

Pour passer en production, brancher les éléments suivants :

- **API prix carburants** : [data.gouv.fr — Prix des carburants](https://www.data.gouv.fr/fr/datasets/prix-des-carburants-en-france-flux-instantane-v2/) (flux instantané officiel)
- **Backend** : Node.js / Express ou Supabase pour l’auth, les commentaires et les propositions
- **Base de données** : PostgreSQL ou Supabase avec RLS pour la gestion des rôles (member / admin)
- **Auth** : Supabase Auth, Auth0, ou JWT maison
- **Déploiement** : Vercel, Netlify, ou VPS OVH

---

## 🗺️ Roadmap

- [ ] Connexion à l’API officielle data.gouv.fr (flux temps réel)
- [ ] Authentification persistante (Supabase Auth)
- [ ] Notifications push quand un prix baisse pour une station favorite
- [ ] Historique des prix par station (graphique)
- [ ] Application mobile (PWA)
- [ ] Favoris par utilisateur
- [ ] Export CSV des prix

---

## 📜 Licence

MIT — libre d’utilisation et de modification.

---

*Projet développé avec ❤️ par [@Sazar](https://github.com/Sazar) — juillet 2026.*

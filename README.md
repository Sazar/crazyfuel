# CrazyFuel

CrazyFuel est une web app orientée produit qui permet de visualiser les prix des stations-service en France sur une carte interactive, avec une logique communautaire de commentaires, de corrections de prix et une validation centralisée par un administrateur.

## Fonctionnalités incluses

- Carte interactive Leaflet avec stations réparties en France.
- Affichage multi-carburants : Gazole, SP95, SP95-E10, SP98, GPLc et E85.
- Profil utilisateur avec carburant préféré.
- Classement des 3 stations les moins chères de France selon le carburant choisi dans le profil.
- Classement des 3 stations les moins chères les plus proches de la position utilisateur.
- Création de compte côté front (démonstration produit complète).
- Publication de commentaires soumis à validation admin.
- Propositions de correction de prix soumises à modération.
- Dashboard administrateur avec file d'attente et journal d'activité.
- Design épuré, responsive, mode sombre inclus.

## Stack

- HTML / CSS / JavaScript vanilla
- [Leaflet](https://leafletjs.com/) + OpenStreetMap
- Fonts via [Fontshare](https://www.fontshare.com/) (Satoshi + Cabinet Grotesk)

## Structure

```
crazyfuel/
├── crazyfuel.html   → application principale mono-page
└── README.md
```

## Démarrage rapide

Ouvrir `crazyfuel.html` directement dans un navigateur — aucune dépendance locale ni serveur requis.

## Suite recommandée (production)

1. Brancher une API temps réel de prix carburants (ex : data.gouv.fr prix-des-carburants).
2. Ajouter un backend avec base de données pour comptes, commentaires et modération.
3. Mettre en place une authentification sécurisée (JWT, OAuth).
4. Déployer un backend admin avec rôles, audit trail et notifications.
5. Système anti-abus pour les propositions communautaires (rate-limit, signalement).

## Roadmap

- [ ] Connexion API prix carburants temps réel
- [ ] Authentification persistante
- [ ] Backend modération
- [ ] Notifications push (nouvelles corrections validées)
- [ ] Mode hors-ligne (PWA)
- [ ] Export CSV des prix par région

---

*Projet démarré en juillet 2026.*

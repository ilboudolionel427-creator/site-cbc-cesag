# CBS-CESAG

Site vitrine de la Communauté Burkinabè du Sénégal au CESAG, construit avec React, Vite et Tailwind CSS.

## Préparer une publication

Prérequis : Node.js et npm.

```powershell
npm ci
npm run build
```

Le site prêt à publier est généré dans `dist/`. Pour un hébergement statique tel que Netlify, publiez le contenu de ce dossier. Le fichier `public/_redirects` configure le retour vers l’application pour les routes gérées côté client.

Pour tester la version de production localement :

```powershell
npm run preview
```

Après chaque modification, relancez `npm run build` puis publiez à nouveau `dist/`.

## Limites à connaître avant publication

- L’espace Admin n’est disponible qu’en développement. Le contrôle actuellement dans le navigateur n’est pas une authentification sécurisée.
- Les données enregistrées dans `localStorage` restent dans le navigateur qui les a saisies. Elles ne sont ni partagées entre visiteurs, ni transférées par le déploiement.
- Pour gérer le site en ligne avec des changements visibles par tous, il faudra connecter une API ou une base de données avec une authentification côté serveur.
- Les statistiques, profils de démonstration, partenaires, adresse, horaires et liens sociaux sont accompagnés d’avertissements car ces informations restent à confirmer.

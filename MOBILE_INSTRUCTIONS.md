# Préparation pour Android Studio

Votre application est maintenant configurée comme une **PWA (Progressive Web App)** haute performance. Pour la transformer en application native Android via **Android Studio**, suivez ces étapes :

## 1. Prérequis
- Avoir **Node.js** installé sur votre machine locale.
- Avoir **Android Studio** installé.

## 2. Installation de Capacitor
Dans votre projet local (après avoir téléchargé le code), exécutez :
```bash
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init "Match Compteur" "com.votre.app" --web-dir dist
```

## 3. Configuration de la Build
1. Générez les fichiers de production :
   ```bash
   npm run build
   ```
2. Ajoutez la plateforme Android :
   ```bash
   npx cap add android
   ```
3. Copiez vos fichiers web vers le projet Android :
   ```bash
   npx cap copy
   ```

## 4. Ouverture dans Android Studio
Lancez la commande suivante pour ouvrir le projet natif :
```bash
npx cap open android
```

## Optimisations incluses dans ce projet :
- **PWA Ready :** Un Service Worker a été configuré via `vite-plugin-pwa` pour permettre le fonctionnement hors-ligne.
- **Icones & Manifeste :** Les icônes haute résolution et le manifeste mobile sont déjà configurés dans `vite.config.ts`.
- **Thème :** Les balises meta pour le "plein écran" et la couleur de la barre de statut sont incluses dans `index.html`.

Vouz pouvez maintenant exporter votre projet (Settings > Export to ZIP) et suivre ces étapes sur votre ordinateur.

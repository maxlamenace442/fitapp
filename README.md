# FitPlan — application mobile Android

Cette version conserve l'application web FitPlan et ajoute une configuration Capacitor pour la transformer en application Android.

## Option recommandée — Chromebook + GitHub

1. Envoie tout le contenu de ce dossier dans ton dépôt GitHub.
2. Fais un commit sur `main` (ou `master`).
3. Ouvre l'onglet **Actions** du dépôt.
4. Le workflow **Build FitPlan Android APK** se lance automatiquement après le push.
5. Quand le workflow est terminé, ouvre son exécution puis télécharge l'artefact **FitPlan-debug-apk**.
6. Décompresse l'artefact et installe `app-debug.apk` sur ton téléphone Android.

Tu peux aussi lancer manuellement le workflow depuis **Actions → Build FitPlan Android APK → Run workflow**.

## Option locale

Si Node.js, Java et Android SDK sont disponibles :

```bash
npm install
npx cap add android
npx cap sync android
```

Puis, avec Android Studio :

```bash
npx cap open android
```

## Identité de l'app

- Nom : FitPlan
- App ID : `com.fitplan.app`
- Dossier web : `www`

## Important

Le dossier `android/` n'est volontairement pas inclus : GitHub Actions le génère proprement avec la version actuelle de Capacitor. L'APK généré par le workflow est une version de test (debug). Pour Google Play, il faudra ensuite créer une version signée (release) avec une clé de signature.

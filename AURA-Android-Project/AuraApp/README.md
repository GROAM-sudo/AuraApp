# 🌟 AURA — Application Widgets

<div align="center">
  <img src="app/src/main/res/mipmap-xxxhdpi/ic_launcher.png" width="120"/>
  <h3>Design Glassmorphism · Apple Vision Pro Aesthetic</h3>
</div>

## 📱 Pages de l'application

| Page | Description |
|------|-------------|
| ☁️ **Météo** | Fond animé dynamique selon la météo (pluie, neige, soleil…) + prévisions horaires |
| 🕐 **Horloge** | Horloge plein écran avec fonds d'écran animés (vidéo ou image) |
| 📅 **Agenda** | Calendrier interactif avec gestion d'événements |
| 📝 **Notes** | Notes colorées glassmorphism avec éditeur plein écran |
| 🧘 **Zen** | Exercice de respiration guidée 4-7-8 avec compteur de cycles |

## 🚀 Installer l'APK

### Option 1 — Télécharger directement (recommandé)
1. Allez dans **Releases** → [Dernière version](../../releases/latest)
2. Téléchargez `AURA-v1.0.apk`
3. Sur votre téléphone : **Paramètres → Sécurité → Sources inconnues** → Activez
4. Ouvrez le fichier APK téléchargé et installez

### Option 2 — Compiler vous-même
```bash
git clone https://github.com/VOTRE_USERNAME/AuraApp.git
cd AuraApp
chmod +x gradlew
./gradlew assembleRelease
# APK : app/build/outputs/apk/release/app-release.apk
```

## 🔑 Configuration météo en temps réel

1. Créez un compte gratuit sur [openweathermap.org](https://openweathermap.org/api)
2. Copiez votre clé API
3. Dans l'app, page Météo → champ "Clé API" → collez et validez
4. La géolocalisation se lance automatiquement

## 🏗️ Build automatique sur GitHub

Ce projet utilise **GitHub Actions** pour compiler l'APK automatiquement à chaque push.

1. Forkez / créez un nouveau repo GitHub
2. Poussez ce code :
```bash
git init
git add .
git commit -m "Initial commit — AURA app"
git branch -M main
git remote add origin https://github.com/VOTRE_USERNAME/AuraApp.git
git push -u origin main
```
3. GitHub Actions compile automatiquement l'APK
4. L'APK est disponible dans **Actions → Build AURA APK → Artifacts**
5. Et aussi dans **Releases** avec chaque nouveau push !

## 🎨 Design

- **Glassmorphism** : panneaux transparents avec backdrop-blur
- **Apple Vision Pro aesthetic** : fond sombre profond, accents bleu glacier
- **Animations** : particules météo (pluie, neige, soleil), orbes ambiantes flottantes
- **Police** : Bebas Neue (titres) + Outfit (interface) + Space Mono (secondes)

## 📂 Structure

```
AuraApp/
├── app/src/main/
│   ├── assets/index.html          ← Toute l'UI (HTML + CSS + JS)
│   ├── java/com/aura/app/
│   │   └── MainActivity.kt        ← Wrapper WebView Android
│   ├── res/
│   │   ├── mipmap-*/ic_launcher.png
│   │   └── values/themes.xml
│   └── AndroidManifest.xml
├── .github/workflows/build-apk.yml ← CI/CD automatique
├── build.gradle
└── settings.gradle
```

## 🔧 Requirements
- Android 7.0+ (API 24+)
- Pour compiler : JDK 17, Android SDK 34

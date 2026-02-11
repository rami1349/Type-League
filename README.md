
# Typing Championship

Typing Championship is a competitive, skill-based typing game that transforms traditional typing practice into an esports-style experience. It combines educational tutorials, real-time ranked battles, customizable typing tests, and arcade-style gameplay into a modern, scalable cross-platform application.

---

## 🎯 Vision

Typing Championship makes typing:

- Competitive
- Addictive
- Skill-driven
- Social
- Rewarding

Instead of boring drills, players experience:

- Real-time 1v1 battles
- Combo streak systems
- XP progression
- Seasonal rankings
- Performance analytics
- Cosmetic unlocks

It’s **TypingClub meets Fortnite UI meets competitive esports**.

---

## 🕹 Game Modes

### 1. Tutorial Mode
- Color-coded key-to-finger mapping
- 10-finger overlay
- Auto-scrolling 2-line text
- Progressive lessons
- Accuracy tracking
- Inspired by TypingClub

### 2. Normal Mode
- Customizable typing tests (Paragraph, Words, Quotes, Custom)
- Options to include numbers/punctuation
- Timer selection: 15s / 30s / 45s / Custom
- Tracks WPM, Accuracy, Streaks, Personal bests

### 3. Ranked Mode
- Real-time 1v1 competition
- 45-second fixed matches
- 70% player view / 30% opponent stats
- Live WPM and Accuracy
- Global leaderboard and seasonal ranking

### 4. Fun Mode
- Arcade-style 2D side-scrolling typing game
- Defeat enemies by typing words
- Combo multipliers and power-ups
- Boss stages and increasing difficulty
- Inspired by TypingLand

---

## 👤 User Profile & Progression

- Edit nickname and profile picture
- View last 10 matches
- Track rank and diagnostics graphs
- Monitor WPM, Accuracy, XP
- Progress through seasonal events

---

## 🎨 Design Philosophy

- Modern, clean, and competitive
- Dark / Light mode
- Custom theme color options
- Fortnite-style mode selection UI
- Smooth animations
- Minimalist and engaging interface

---

## 💰 Monetization Strategy

- **Subscriptions:** Removes ads, unlocks premium skins, ranked leagues, XP boost
- **Battle Pass:** Seasonal rewards with Free + Premium tracks
- **Ads:** Rewarded and interstitial ads (non-intrusive)
- **Cosmetic Store:** Skins, themes, visual effects
- Architecture designed for scalability to 1M+ users

---

## ⚙️ Technology Stack

### Frontend
- **Flutter:** Cross-platform support (iOS, Android, Desktop)
- **Flame Engine:** Fun Mode game engine
- **Riverpod:** State management

### Backend
- **Firebase Auth & Firestore**
- **Cloud Functions**
- **Firebase Analytics**
- **RevenueCat:** Subscription handling
- **Google AdMob:** Ads
- Multiplayer architecture: real-time ranked sync

---

## 📊 Firebase Data Structure (Monetization-ready)

```

users/{uid}
email
nickname
createdAt
isPremium
subscriptionExpiration
adsRemoved
ownedSkins[]
totalMatches
lifetimeXP

purchases/{purchaseId}
uid
productId
purchaseDate
platform
verified

ranked_global/{seasonId}/players/{uid}
wpmAvg
accuracyAvg
winRate
matchesPlayed

seasons/{seasonId}
startDate
endDate
premiumPrice
rewards[]

season_progress/{seasonId}_{uid}
xp
tierUnlocked
claimedRewards[]

````

- Entitlement-driven architecture
- Server-side verification of purchases
- Scalable for 10k → 1M+ users

---

## 📈 Scalability & Growth

- Target: 10k → 1M users
- Monetization prioritization: Subscriptions → Battle Pass → Rewarded Ads → Interstitial Ads
- Cloud architecture ready for seasonal resets, leaderboards, and multiplayer scaling
- Analytics for retention, monetization, and engagement tracking

---

## 🛠 Installation / Development

1. **Clone repository**

2. **Install dependencies**

```bash
flutter pub get
```

3. **Run app**

```bash
flutter run
```

4. **Setup Firebase**

* Add Firebase project for Auth, Firestore, Analytics
* Configure AdMob and RevenueCat

5. **Environment Variables**

* Add API keys and environment configs for Firebase, AdMob, RevenueCat

---

## 📂 Folder Structure

```
lib/
  main.dart
  screens/
    home_screen.dart
    tutorial_mode.dart
    normal_mode.dart
    ranked_mode.dart
    fun_mode.dart
  widgets/
    keyboard_overlay.dart
    finger_overlay.dart
    carousel.dart
  services/
    firebase_service.dart
    monetization_service.dart
    ad_service.dart
    subscription_service.dart
    purchase_service.dart
  models/
    user.dart
    match.dart
    entitlements.dart
  utils/
    theme.dart
    constants.dart
    analytics.dart
```

---

## ⚡ Future Roadmap

* **V1:** Core modes, ranked multiplayer, subscription, leaderboard
* **V2:** Battle pass, advanced analytics, seasonal events
* **V3:** Esports tournaments, clan system, creator skins
* **V4:** Global competitions, PC/Desktop release



> Typing League — where typing becomes a sport, and every keystroke counts.

```

---

If you want, I can also generate a **developer-ready “Onboarding & Setup.md”** file with all the Flutter + Firebase + Flame + AdMob + RevenueCat configurations step by step.  

Do you want me to generate that next?
```

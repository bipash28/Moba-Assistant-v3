# MLBB AI Assistant

An advanced AI-powered assistant for Mobile Legends: Bang Bang players that helps dominate matches through real-time analysis, predictions, and strategic guidance.

## Features

### Core Features
- Hero database with detailed stats, skills, and counters
- Real-time game analysis and recommendations
- Build optimization and counter-building suggestions
- Multi-language in-game chat translation
- Performance optimization

### Advanced Features
- **Real-time Map Analysis**
  - Enemy position prediction
  - Jungle monster respawn timers
  - Optimal rotation suggestions
  - Vision control recommendations

- **Combat Analysis**
  - Damage calculation and trade potential
  - Team fight win probability
  - Skill combo suggestions
  - Positioning recommendations

- **Strategic Planning**
  - Lane assignment optimization
  - Split-push timing suggestions
  - Objective priority guidance
  - Team composition strength analysis

- **Resource Management**
  - Gold efficiency tracking
  - Experience optimization paths
  - Item build timing suggestions
  - Power spike alerts

- **Team Coordination**
  - Quick communication shortcuts
  - Role-specific callouts
  - Team fight coordination pings
  - Objective setup reminders

### AI-Powered Features
- Machine learning-based enemy behavior prediction
- Pattern recognition for player playstyles
- Win condition analysis
- Meta adaptation recommendations


## 🚀 Getting Started

### Prerequisites
- Node.js 14+
- NativeScript CLI
- Android Studio (for Android development)
- Xcode (for iOS development)
- VS Code (recommended)

### Installation

1. Install NativeScript CLI:
```bash
npm install -g @nativescript/cli
```

2. Clone the repository:
```bash
git clone <repository-url>
```

3. Install dependencies:
```bash
npm install
```

### Development
```bash
# For Android
ns run android

# For iOS
ns run ios
```

### Building APK

#### Debug APK
To generate a debug APK (for testing):
```bash
ns build android
```
The debug APK will be generated at: `platforms/android/app/build/outputs/apk/debug/app-debug.apk`

#### Release APK
To generate a release APK (for production):

1. Generate a keystore (only needed once):
```bash
keytool -genkey -v -keystore mlbb-assistant.keystore -alias mlbb-assistant -keyalg RSA -keysize 2048 -validity 10000
```

2. Create a `keystore.json` file in the root directory:
```json
{
    "android": {
        "keystore": "mlbb-assistant.keystore",
        "storePassword": "your-store-password",
        "alias": "mlbb-assistant",
        "password": "your-key-password"
    }
}
```

3. Build the release APK:
```bash
ns build android --release --key-store-path mlbb-assistant.keystore --key-store-password your-store-password --key-store-alias mlbb-assistant --key-store-alias-password your-key-password
```
The release APK will be generated at: `platforms/android/app/build/outputs/apk/release/app-release.apk`

### Installing on Your Device

#### Method 1: Using ADB
1. Enable USB debugging on your Android device
2. Connect your device via USB
3. Run:
```bash
adb install platforms/android/app/build/outputs/apk/release/app-release.apk
```

#### Method 2: Direct Installation
1. Transfer the APK to your Android device
2. Enable "Install from Unknown Sources" in your device settings
3. Tap the APK file to install

[Rest of the README content remains the same]
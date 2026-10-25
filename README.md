# Turf Manager – APK සෑදීම

## අවශ්‍ය දේ (එක් වරක් පමණක්)
1. **Node.js** (LTS අනුවාදය, 20 හෝ ඊට වැඩි): https://nodejs.org
2. **Android Studio**: https://developer.android.com/studio (JDK එය සමඟම එයි)

## පියවර
මෙම ෆෝල්ඩරය තුළ Terminal / Command Prompt විවෘත කර:

```
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Android Studio විවෘත වූ පසු (පළමු වතාවට Gradle බාගැනීමට මිනිත්තු කිහිපයක් යයි):

**Build → Build Bundle(s) / APK(s) → Build APK(s)**

සූදානම් වූ විට "locate" ක්ලික් කරන්න. ගොනුව:
`android/app/build/outputs/apk/debug/app-debug.apk`

එය ෆෝන් එකට යවා ස්ථාපනය කරන්න ("Unknown sources" ඉඩ දිය යුතුය).

## ඇප් එක වෙනස් කිරීම
`www/index.html` සංස්කරණය කර `npx cap sync android` නැවත ධාවනය කරන්න.

## වැදගත්
- **වෙළඳපොළ ටැබ් එක** මෙම APK එකේ ක්‍රියා නොකරයි (එයට සර්වර් එකක් අවශ්‍යයි). අනෙක් සියල්ල (වියදම්, ලාභය, පොහොර, රෝග, කැල්කියුලේටරය, භාෂා 3) සම්පූර්ණයෙන් ක්‍රියා කරයි.
- දත්ත ෆෝන් එකේම සුරැකේ. ඇප් එක uninstall කළොත් දත්ත මැකේ.
- Play Store එකට දැමීමට release (signed) build එකක් සහ Google Play developer account එකක් අවශ්‍යයි.
- App icon වෙනස් කිරීමට: `npm i -D @capacitor/assets`, `resources/icon.png` (1024×1024) දමා `npx capacitor-assets generate --android`.

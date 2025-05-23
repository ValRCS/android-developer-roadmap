# Android Deployment in 2025

## Primary Deliverable Format

When publishing an Android application in 2025, the primary deliverable for the **Google Play Store** is:

### ✅ Android App Bundle (.aab)

- **Format**: `.aab` (Android App Bundle)
- **Required by Google Play**: Since **August 2021**
- **Why**: Google Play uses it to generate optimized APKs for different device configurations, reducing size and improving performance.

### 📦 APKs Are Still Useful For:

- Local testing
- Manual distribution or sideloading
- Alternative stores (Amazon, F-Droid, etc.)

---

## Step-by-Step Deployment Guide

### 🛠️ 1. Prepare Your App for Release

- Set build variant to `release`
- Remove debug code and logs
- Set correct `versionCode`, `versionName`, and target SDK in `build.gradle`

### 🔐 2. Generate a Signing Key

- Use Android Studio: `Build > Generate Signed Bundle / APK`
- Create `keystore.jks` and keep it safe

### 📦 3. Build a Signed `.aab`

- Use `Build > Generate Signed Bundle / APK`
- Choose `release` and sign with keystore
- Find output in: `/app/build/outputs/bundle/release/app-release.aab`

### 🧪 4. Test Thoroughly

- Use `adb install` for local APKs
- Use Google Play’s **Internal Testing** or **Closed Testing** tracks

### 🏬 5. Google Play Console Setup

- Register at [play.google.com/console](https://play.google.com/console)
- One-time fee: **$25 USD**

### 📋 6. Create App in Console

- Fill in app name, type, free/paid, policies
- Upload assets (screenshots, descriptions, icon, etc.)

### 🧾 7. Policy Declarations

- Data safety
- App access
- Ads declaration
- Privacy policy URL

### 📤 8. Upload the `.aab`

- Go to **Production > Create release**
- Upload `.aab`, optional mapping.txt for ProGuard

### ✅ 9. Review and Rollout

- Review release summary
- Click "Start rollout to production"
- Wait for review (usually 1–3 days)

---

## Google Play Store 12 users - 14 days testing requirement

### 🔍 New Requirement (2025)

- **Applies to**: Personal developer accounts created **after Nov 13, 2023**
- **Requirement**: Minimum **12 testers**, each opted in for **14 continuous days**
- **Testing type**: **Closed Testing** track only
- **Opt-in must be uninterrupted**

### 🧪 Steps to Comply

1. Create a **Closed Testing** track
2. Share **opt-in link**
3. Ensure 12+ testers **stay opted-in** for 14 days
4. After completion, apply for production access

---

## Best Options for Acquiring 12 Testers in 2025

| Option                     | Cost    | Reliable? | Good for Solo Dev? | 14-Day Valid? |
|---------------------------|---------|-----------|---------------------|---------------|
| University classmates     | Free    | ✅ High    | ✅ Yes              | ✅ Yes        |
| Friends/family            | Free    | ✅ High    | ✅ Yes              | ✅ Yes        |
| Reddit & Discord          | Free    | ⚠️ Medium | ✅ Yes              | ⚠️ Maybe      |
| BetaTesting.com           | Paid    | ✅ High    | ⚠️ Optional         | ✅ Yes        |
| Fake accounts/emulators   | Free    | ❌ No     | ❌ No               | ❌ No         |

📝 **Tips**:
- Use class chats, emails, or posters
- Provide instructions and clear timeline
- Encourage testers to remain opted in and give feedback

---

## Android App Deployment Alternatives (2025)

| Platform | Link | Registration | Fees | Open Source Requirement | App Type Allowed | Notes |
|----------|------|---------------|------|--------------------------|------------------|-------|
| **F-Droid** | [f-droid.org](https://f-droid.org/) | Yes | Free | ✅ Yes | OSS only | Fully open-source apps only; slow process |
| **Amazon Appstore** | [developer.amazon.com](https://developer.amazon.com/apps-and-games) | Yes | Free | ❌ No | All apps | Fire/Kindle support |
| **Samsung Galaxy Store** | [seller.samsungapps.com](https://seller.samsungapps.com) | Yes | Free | ❌ No | All apps | Galaxy-specific features supported |
| **Huawei AppGallery** | [developer.huawei.com](https://developer.huawei.com/consumer/en/appgallery) | Yes | Free | ❌ No | All apps | Use HMS if no GMS |
| **Aptoide** | [aptoide.com](https://www.aptoide.com/) | Yes | Free | ❌ No | All apps | Developer-controlled stores |
| **SlideME** | [slideme.org](http://slideme.org/) | Yes | Free | ❌ No | All apps | Curated apps, niche users |
| **Itch.io** | [itch.io](https://itch.io/developers) | Yes | Pay what you want | ❌ No | Games, tools | Ideal for indie games |
| **GitHub Releases** | [github.com](https://github.com/) | No | Free | ✅ Preferred | OSS preferred | Direct download, dev-friendly |
| **Telegram Channels** | [telegram.org](https://telegram.org/) | No | Free | ❌ No | All apps | Good for communities |
| **Self-hosted Website** | Custom | No | Free | ❌ No | All apps | Must support HTTPS & permissions warning |

---
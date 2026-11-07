# KASHISH AI Android — Dark APK Project

यह Android Studio project है। इसमें:
- Dark chat UI
- SQLite में सिखाए गए सवाल-जवाब की स्थायी मेमोरी
- Hindi/English शब्द-मिलान आधारित retrieval
- Wikipedia search और सारांश; सेव करने से पहले user approval
- Android speech recognition और Text-to-Speech

## APK बनाने के लिए

इस environment में Android SDK/Gradle उपलब्ध नहीं था, इसलिए यहां compiled APK नहीं बनाया गया है।
Source project को Android Studio में खोलकर APK बनाया जा सकता है।

1. Android Studio install करें।
2. इस folder को Android Studio में Open करें।
3. Gradle sync पूरा होने दें।
4. Build > Build Bundle(s) / APK(s) > Build APK(s) चुनें।
5. APK आमतौर पर `app/build/outputs/apk/debug/app-debug.apk` में मिलेगा।

## 4GB RAM फोन पर

- App का memory/chat भाग offline चलता है।
- Wikipedia learning के लिए internet चाहिए।
- Voice के लिए Android speech recognition service चाहिए।
- यह build neural network या generative LLM शामिल नहीं करता। यह Android UI starter है; V4 का Python neural classifier अलग Termux project में है। उसे native APK में जोड़ना अगला development step होगा।
- इसे general AI या unlimited AI न समझें।

## GitHub Actions से APK

`.github/workflows/build-apk.yml` भी दिया गया है। Project को GitHub repository में push करने पर Actions से debug APK build किया जा सकता है।

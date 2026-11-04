# Neu Calculator

MIUI அமைப்பு + 3D neumorphic பொத்தான்கள் கொண்ட Calculator. Scientific mode, Day/Night, 15 converter tools.

## GitHub-ல் build செய்யும் முறை

1. GitHub-ல் புதிய repository உருவாக்கவும்.
2. இந்த folder-ன் அனைத்து files-ஐயும் (`.github` folder உட்பட) upload / push செய்யவும்.
3. **Actions** tab → **Build Android APK** தானாக ஓடும் (அல்லது *Run workflow* அழுத்தவும்).
4. முடிந்ததும் அந்த run-ஐத் திறந்து, கீழே **Artifacts** → `NeuCalculator-debug-apk` download செய்யவும்.
5. ZIP-ஐ extract செய்து `app-debug.apk`-ஐ phone-ல் install செய்யவும்.

## Web version (GitHub Pages)

Repository → **Settings → Pages → Source: GitHub Actions** என்று மாற்றவும். `Deploy to GitHub Pages` workflow முடிந்ததும் உங்கள் calculator இணைய முகவரியில் திறக்கும்.

## Structure

```
www/index.html            ← முழு calculator (HTML + CSS + JS)
capacitor.config.json     ← Android app அமைப்பு
package.json
.github/workflows/
  build-apk.yml           ← APK build
  pages.yml               ← Web deploy
```

`android/` folder-ஐ நீங்கள் upload செய்ய வேண்டாம்; workflow தானாக உருவாக்கும்.

## குறிப்பு

- Debug APK (தானாக sign செய்யப்பட்டது) – நேரடியாக install செய்யலாம்.
- Currency live rates-க்கு இணையம் தேவை; இல்லையெனில் தோராய மதிப்புகள் காட்டும்.

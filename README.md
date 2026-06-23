# ⭐ Stellar Finder

一個純前端、零廣告的手機觀星 AR 工具。手機舉起對著天空，即時顯示當前視角內的星座名稱與連線。

## 功能

- 📍 GPS 定位 + 陀螺儀方向追蹤，即時計算視角內天體
- 🌌 12 個主要星座（連線圖 + 中英文名稱 + 簡介）
- 📷 相機 AR 疊加模式（選用）
- 🔍 星點偵測（OpenCV.js）：即時圈出鏡頭畫面中的亮點，靈敏度可調
- 🔴 夜間紅光模式，保護觀星夜視
- 📱 無陀螺儀裝置可手動拖曳旋轉視角
- 🚫 不需要後端、不需要 API key、不需要安裝、零廣告

## 技術

- 純 HTML / CSS / JavaScript，無框架
- [Astronomy Engine](https://github.com/cosinekitty/astronomy)：天文星曆計算
- [OpenCV.js](https://docs.opencv.org/)：相機影格的星點偵測（WASM，首次按偵測時才載入）
- 瀏覽器原生 API：`Geolocation`、`DeviceOrientationEvent`、`Canvas 2D`、`getUserMedia`

## 使用方式

直接開啟部署後的網址即可，手機建議用 Chrome（Android）或 Safari（iOS）。

> iOS 需要手動授權陀螺儀權限（瀏覽器安全限制）。

## 本機開發

```bash
# 任何靜態伺服器皆可，例如：
npx serve .
```

> ⚠️ 注意：GPS / 陀螺儀 / 相機皆須在 HTTPS（或 localhost）環境下才能運作，直接用 `file://` 開啟本機檔案會被瀏覽器擋掉。

## License

MIT

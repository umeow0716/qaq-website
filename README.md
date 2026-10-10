# QAQ Website

Official website and download page for QAQ, an independent campus life assistant for NTUT students.

## Development

```sh
pnpm install
pnpm dev
```

Production build:

```sh
pnpm build
```

The static output is written to `dist/` and is intended to be deployed to Cloudflare Pages at
`qaq.umeow.eu.org`.

## Licensing

Website source code is licensed under the MIT License. The QAQ logo asset copied from `qaq-app` keeps its original
GPL-3.0 licensing; see `NOTICE.md` and `LICENSES/GPL-3.0.txt`.

## Landing page / 首頁設計

這個網站以 Astro 製作，首頁位於 `src/pages/index.astro`，主要樣式位於
`src/styles/global.css`。首頁保留原有的首屏下載入口，下方加入五個段落：

1. 校園日常：用經過圓角裝置框架處理的 QAQ 課表展示功能；
2. 跨平台：使用原創的 CSS / inline SVG 裝置示意圖；
3. i 學園 VPN：呈現僅在選用實驗性功能後，校外使用 i 學園時的嘗試連線流程；
4. 主題：以實際 APP 截圖比較亮色與暗色，按鈕可切換網站主題；
5. 開源社群：GitHub、下載入口與非官方專案聲明。

靜態示意圖不會請求外部圖片或 icon CDN。`public/previews/` 使用使用者提供的
APP 截圖轉製成壓縮 WebP；桌面截圖的個人識別區已模糊處理。
所有新增段落皆支援首頁原本的繁中／英文切換及主題切換。

### 開發

```bash
corepack pnpm install --frozen-lockfile
corepack pnpm dev
corepack pnpm build
```

視覺參考：Cloudflare `one.one.one.one` 的大幅留白、交錯圖文與平面形狀敘事。
所有新增插畫與 icon 為本專案獨立製作的 SVG / CSS 圖形，未直接複製 Cloudflare 圖像。

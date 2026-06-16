<div align="center">

# 都卜勒效應模擬器 / Doppler Effect Simulator

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chart.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)

</div>

---

## 中文說明

### 簡介

這是一個互動式的**都卜勒效應（Doppler Effect）** 模擬器，讓使用者可以直觀地觀察和聆聽移動聲源產生的頻率變化。模擬器包含完整的加速→等速→減速行駛過程，並支援波前傳播動畫、即時頻率圖表與 Web Audio 聲音合成。

### 功能特色

- **波前擴散動畫** — 即時繪製聲波從移動波源向外擴散的圓形波前
- **都卜勒頻率計算** — 使用延遲時間（retarded time）演算法，精確計算觀測者接收到的即時頻率
- **即時圖表** — Chart.js 繪製觀測頻率隨時間變化的曲線圖
- **Web Audio 聲音合成** — 正弦波振盪器即時輸出對應頻率的聲音，可聽見都卜勒效應
- **兩種聲源模式** — 純音（固定頻率）與救護車（高低頻交替）
- **可拖曳觀測者** — 直接用滑鼠拖曳藍色觀測者圓點，改變離馬路的距離
- **多國語言** — 繁體中文 / English 即時切換
- **深色模式** — 亮色／暗色主題切換
- **響應式設計** — 支援電腦、平板、手機三種裝置
- **超音速馬赫錐** — 當車速超過音速時，自動繪製馬赫錐（Mach cone）

### 如何使用

1. 調整左側面板的參數（聲源頻率、最高速度、加減速時間、馬路長度、觀測者距離）
2. 點擊「**模擬**」按鈕開始，汽車會從左側加速至最高速度，經過觀測者後減速停止
3. 觀測畫面上的**圓形波前**如何隨汽車移動而壓縮（前方）與拉伸（後方）
4. 下方的**頻率-時間圖表**會即時記錄觀測到的頻率變化
5. 啟用聲音時，可聽見頻率隨汽車靠近而升高、遠離而降低

### 技術細節

| 項目 | 說明 |
|------|------|
| **語言** | 純 HTML + CSS + JavaScript（無後端依賴） |
| **繪圖** | Canvas 2D API（波前動畫）、Chart.js（頻率圖表） |
| **樣式** | Tailwind CSS（CDN）、CSS 自訂屬性（深色模式） |
| **聲音** | Web Audio API（OscillatorNode + GainNode） |
| **響應式** | CSS Grid + Media Queries + ResizeObserver |
| **圖示** | Font Awesome 6 |

### 都卜勒效應公式

觀測者接收到的頻率：

$$f' = f_0 \cdot \frac{v}{v - v_r}$$

其中：
- $f_0$ = 聲源原始頻率
- $v$ = 音速（343 m/s）
- $v_r$ = 聲源相對於觀測者的徑向速度（靠近為正）

### 專案結構

```
├── index.htm          # 主程式（最新版本）
├── README.md          # 本說明文件
└── .gitignore
```

---

## English

### Overview

An interactive **Doppler Effect Simulator** that lets you visually and audibly experience frequency shifts from a moving sound source. The simulation models a complete acceleration → cruising → deceleration trajectory with circular wavefront propagation, real-time frequency charting, and Web Audio synthesis.

### Features

- **Wavefront Animation** — Circular waves emitted from a moving source, with compression ahead and stretching behind
- **Doppler Frequency Calculation** — Retarded-time algorithm for accurate observed frequency
- **Real-time Chart** — Chart.js line chart showing observed frequency over time
- **Web Audio Synthesis** — Sine wave oscillator plays the corresponding frequency in real time
- **Two Sound Modes** — Pure tone (fixed frequency) and ambulance (alternating high/low)
- **Draggable Observer** — Drag the blue observer dot to change distance from the road
- **Bilingual UI** — Traditional Chinese / English toggle
- **Dark Mode** — Light/dark theme toggle
- **Responsive Layout** — Optimized for desktop, tablet, and mobile
- **Mach Cone** — Automatically drawn when car speed exceeds the speed of sound

### How to Use

1. Adjust parameters in the left panel (source frequency, max speed, accel/decel time, road length, observer distance)
2. Click "**Simulate**" — the car accelerates from the left, passes the observer, then decelerates to a stop
3. Watch the **circular wavefronts** compress ahead of the car and stretch behind it
4. The **frequency-vs-time chart** records the observed frequency in real time
5. Enable sound to hear the pitch rise as the car approaches and fall as it recedes

### Technical Details

| Item | Description |
|------|-------------|
| **Language** | Pure HTML + CSS + JavaScript (no backend) |
| **Rendering** | Canvas 2D API (wavefronts), Chart.js (frequency chart) |
| **Styling** | Tailwind CSS (CDN), CSS custom properties (dark mode) |
| **Audio** | Web Audio API (OscillatorNode + GainNode) |
| **Responsive** | CSS Grid + Media Queries + ResizeObserver |
| **Icons** | Font Awesome 6 |

### Doppler Effect Formula

Observed frequency:

$$f' = f_0 \cdot \frac{v}{v - v_r}$$

Where:
- $f_0$ = source emission frequency
- $v$ = speed of sound (343 m/s)
- $v_r$ = radial velocity of source toward observer (positive when approaching)

### Project Structure

```
├── index.htm          # Main program (latest version)
├── README.md          # This file
└── .gitignore
```

---

## Live Demo

Open `index.htm` in any modern browser — no build step required.

## License

MIT

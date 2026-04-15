<div align="center">

# Ruoxiang Zhao

### *I build systems where software has to meet the physical world.*

Robots, multi-agent AI, custom hardware — things that have to actually work when you turn them on.

[![Building](https://img.shields.io/badge/Building-Embodied%20AI-1B5E20?style=for-the-badge)](https://github.com/Zhaor3?tab=repositories)
[![Stack](https://img.shields.io/badge/Stack-Robotics%20%C3%97%20LLMs%20%C3%97%20Hardware-0A66C2?style=for-the-badge)](https://github.com/Zhaor3?tab=repositories)
[![Approach](https://img.shields.io/badge/Approach-Prototype%20%E2%86%92%20Deploy-6A1B9A?style=for-the-badge)](https://github.com/Zhaor3?tab=repositories)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![ROS](https://img.shields.io/badge/ROS-22314E?style=for-the-badge&logo=ros&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white)
![PlatformIO](https://img.shields.io/badge/PlatformIO-FF7F00?style=for-the-badge&logo=platformio&logoColor=white)

</div>

---

## About

I gravitate toward problems where you can't fake the answer. The robot either moves or it doesn't. The trade either makes money or it doesn't. The LCD either talks to the SPI bus or you go figure out which GPIO pin you crossed.

Most of what's here started as a question I couldn't stop thinking about and ended as something I could turn on and use.

---

## Featured projects

### [DayTradeAgents](https://github.com/Zhaor3/DayTradeAgents) — Multi-agent LLM trading framework

> An 11-agent system where bull and bear analysts argue with each other before a portfolio manager makes the call.

A six-phase pipeline that mirrors how an actual trading desk operates: data ingestion → analyst team → adversarial debate → trade proposal → risk stress-test → final decision. 15+ technical indicators are computed locally before any LLM gets involved, anchoring the agents in objective signals instead of letting them cherry-pick confirmation.

- **62% exact accuracy** on an 8-stock historical backtest — NVDA +20.6%, META +18.3%, TSLA −14.4%
- Telegram delivery with annotated charts: candlesticks, Bollinger bands, ATR forecast cone
- Position-aware — tell it your shares and average cost, and it factors P&L into the call
- Two-tier model routing keeps cost predictable: deep models for analysis and debate, fast models for formatting and news

`Python` · `Anthropic / OpenAI APIs` · `yfinance` · `Telegram Bot API` · `36-test suite`

---

### [tokenjar](https://github.com/Zhaor3/tokenjar) — Real-time API spend on a desk gadget

> A small wired thing that sits on my desk and tells me exactly how much I'm spending on Claude and OpenAI right now.

ESP32-S3 SuperMini driving a 2" ST7789 LCD over SPI, rotary encoder for input, LVGL-based UI. Six rotating screens show Claude / OpenAI / combined spend across windows from 1h to 30d, plus 24-hour sparklines. First boot drops a captive portal so you configure WiFi and API keys from your phone.

- Pulls from the Anthropic and OpenAI Admin APIs, refreshes every 60s
- WiFi captive portal setup, mDNS as `tokenjar.local`, OTA firmware updates
- Adaptive screen dimming, NVS-persisted credentials, cached fallback when the network drops
- Squashed a nasty `TFT_eSPI` null-pointer bug specific to ESP32-S3 — needed `-DUSE_FSPI_PORT` and a clean rebuild to surface the fix

`C++` · `PlatformIO` · `LVGL` · `TFT_eSPI` · `ESP32-S3`

---

### [TA.skill](https://github.com/Zhaor3/TA-skill) — Relationship-aware persona reconstruction

> Reconstructs a person as a persistent AI persona — not generically, but as they exist *in relation to you specifically*.

Four modular engines model different layers: **Identity** (temperament, values, contradictions), **Relationship** (attachment, conflict patterns, how they actually treat *you*), **Memory** (shared timeline, rituals, unresolved threads), **Presence** (message length, punctuation, response timing). Every inference carries a HIGH / MEDIUM / LOW confidence and a source citation — the persona hedges instead of fabricating.

- Ingests chat exports from WhatsApp, Telegram, Discord, iMessage, plus screenshots and photo cues
- Human Mode for full language modeling, Pet Mode with narrated / interpreted / playful / hybrid voices
- Correction workflow with version snapshots — "she'd never start a sentence like that" updates the persona and is rollback-safe
- Designed around safety: transparent / immersive / hybrid disclosure modes, crisis detection, all data stays local

`Python` · `AgentSkills standard` · `MIT`

---

### [Leaf-vac](https://github.com/Zhaor3/Leaf-vac) — AI-enabled outdoor robotics

> An outdoor robot for yard work — navigation, vision, manipulation, natural-language commands. Collaborative project I've put substantial work into.

VSLAM for moving through unstructured outdoor space, image recognition for obstacles and objects, a 3D-printed claw for grabbing things. Responds to commands like *"find my [item]"* or *"drive 10 feet north."* C/CUDA stack with OpenCV (via gocv) and Darknet for inference, dual-motor drive, Bluetooth-enabled Arduino.

- Stereo camera depth sensing with calibration
- Differentiates permanent vs. temporary obstacles
- Inference optimized for resource-constrained on-device compute

`C` · `CUDA` · `OpenCV` · `Darknet` · `Arduino` · `3D-printed mechanics`

---

## What I'm into

- **Embodied AI** — perception → reasoning → motion, on real hardware, end to end
- **Multi-agent orchestration** — debate-based decisions, role separation, adversarial review
- **Custom hardware** — ESP32, sensors, LCDs, the small mechanical pieces that hold it all together
- **Robotics control** — ROS 2, inverse kinematics, teleoperation, servo safety routing
- **Practical ML deployment** — making models actually run on the device that has to use them

---

## Stack

`Python` · `C / C++` · `ROS 2` · `OpenCV` · `CUDA` · `LVGL` · `PlatformIO` · `Arduino` · `ESP32` · `Raspberry Pi` · `Anthropic API` · `OpenAI API` · `Telegram Bot API` · `Darknet` · `CAD` · `3D printing`

---

<div align="center">

![Zhaor3's GitHub stats](https://github-readme-stats.vercel.app/api?username=Zhaor3&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Zhaor3&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)

</div>

---

<div align="center">

*Curious what I'm tinkering with next? Watch the [repo list](https://github.com/Zhaor3?tab=repositories).*

</div>

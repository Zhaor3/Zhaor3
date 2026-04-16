<div align="center">

<a href="https://github.com/Zhaor3">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=4000&pause=1000&color=70A5FD&center=true&vCenter=true&repeat=true&width=650&height=50&lines=Building+autonomous+systems;Multi-agent+AI+%C3%97+Robotics+%C3%97+Hardware;From+silicon+to+swarm+intelligence" alt="Typing SVG" />
</a>

<br/>

I build systems where software has to meet the physical world.<br/>
Robots, multi-agent AI, custom hardware — things that have to actually work when you turn them on.

<br/><br/>

<img src="https://skillicons.dev/icons?i=python,cpp,c,pytorch,arduino,raspberrypi,linux,docker,git,github&perline=10" alt="Tech Stack" />

<br/>

![ROS 2](https://img.shields.io/badge/ROS_2-22314E?style=flat-square&logo=ros&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![PlatformIO](https://img.shields.io/badge/PlatformIO-FF7F00?style=flat-square&logo=platformio&logoColor=white)
![LVGL](https://img.shields.io/badge/LVGL-2C2D3A?style=flat-square&logoColor=white)

</div>

---

I gravitate toward problems where you can't fake the answer — the robot either moves or it doesn't, the trade either makes money or it doesn't, the LCD either talks to the SPI bus or you go figure out which GPIO pin you crossed.

---

## Projects

### [DayTradeAgents](https://github.com/Zhaor3/DayTradeAgents) — Multi-agent LLM trading framework

11 agents argue — bull vs. bear analysts, adversarial debate, risk stress-test — before a portfolio manager makes the call. Six-phase pipeline mirrors a real trading desk. 15+ technical indicators computed locally before any LLM touches the data.

- **62% exact accuracy** on 8-stock backtest — NVDA +20.6%, META +18.3%
- Telegram delivery with candlestick charts, Bollinger bands, ATR forecast cone
- Position-aware P&L — tell it your shares and cost basis, it factors that in
- Two-tier model routing: deep models for analysis, fast models for formatting

`Python` · `Anthropic / OpenAI APIs` · `yfinance` · `Telegram Bot API`

---

### [tokenjar](https://github.com/Zhaor3/tokenjar) — Real-time API spend on a desk gadget

ESP32-S3 + 2" ST7789 LCD showing Claude & OpenAI spend across 1h–30d windows with 24-hour sparklines. Rotary encoder input, LVGL UI, captive portal WiFi setup from your phone.

- Pulls Anthropic and OpenAI Admin APIs every 60s
- mDNS as `tokenjar.local`, OTA firmware updates
- Adaptive dimming, NVS-persisted credentials, cached fallback on network drop

`C++` · `PlatformIO` · `LVGL` · `TFT_eSPI` · `ESP32-S3`

---

### [TA.skill](https://github.com/Zhaor3/TA-skill) — Relationship-aware persona reconstruction

Four engines — **Identity** (values, contradictions), **Relationship** (attachment, how they treat *you*), **Memory** (shared timeline, rituals), **Presence** (message cadence, punctuation) — model a person as they exist in relation to you. Every inference carries confidence levels and source citations.

- Ingests WhatsApp, Telegram, Discord, iMessage exports + screenshots
- Correction workflow with version snapshots and rollback
- Crisis detection, disclosure modes, all data stays local

`Python` · `AgentSkills standard`

---

### [Leaf-vac](https://github.com/Zhaor3/Leaf-vac) — AI-enabled outdoor robotics

VSLAM navigation through unstructured outdoor space, image recognition, 3D-printed claw, natural-language commands like *"find my [item]"* or *"drive 10 feet north."*

- Stereo camera depth sensing with calibration
- Permanent vs. temporary obstacle differentiation
- C/CUDA stack with on-device inference optimized for constrained hardware

`C` · `CUDA` · `OpenCV` · `Darknet` · `Arduino`

---

## What I'm Into

- **Embodied AI** — perception → reasoning → motion, end to end on real hardware
- **Multi-agent orchestration** — debate-based decisions, role separation, adversarial review
- **Custom hardware** — ESP32, sensors, LCDs, the mechanical pieces that hold it all together
- **Practical ML deployment** — making models run on the device that has to use them

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Zhaor3&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" alt="GitHub Stats" height="180"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Zhaor3&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages" height="180"/>

<br/>

<img src="https://streak-stats.demolab.com/?user=Zhaor3&theme=tokyonight&hide_border=true" alt="GitHub Streak"/>

</div>

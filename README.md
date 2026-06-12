```
  ____ _   _ _   _     ____ ___  _   _ _   _
 / ___| \ | | \ | |   / ___/ _ \| \ | | \ | |
| |  _|  \| |  \| |  | |  | | | |  \| |  \| |
| |_| | |\  | |\  |  | |__| |_| | |\  | |\  |
 \____|_| \_|_| \_|   \____\___/|_| \_|_| \_|

  ____ _   _ _   _     ____ ___  _   _ _   _
 / ___| \ | | \ | |   / ___/ _ \| \ | | \ | |
| |  _|  \| |  \| |  | |  | | | |  \| |  \| |
| |_| | |\  | |\  |  | |__| |_| | |\  | |\  |
 \____|_| \_|_| \_|   \____\___/|_| \_|_| \_|
```

## What is this?

A browser game where you shoot floating targets by flicking your index finger upward. No controller. No mouse. Just you, your webcam, and bad aim.

Made with MediaPipe Hands. Runs entirely in the browser. One HTML file.

---

## How it plays

- Point your finger = move the crosshair
- Flick up = shoot
- Hit targets = score points
- Score points = game speeds up
- Miss = nothing happens (yet)

The game gets faster as you score. Every 5 points adds 0.1x speed. At 3.0x targets fly across the screen like they owe you money.

---

## What's inside

- 5 target styles with unique palettes and ring patterns
- Particle explosions on hit (22+ particles with gravity)
- Shockwave rings and screen shake
- Dynamic speed multiplier
- Flick detector (velocity-based with hysteresis)
- Pinch backup trigger (thumb + index)
- Smoothing filter chain (EMA + deadzone + jitter hysteresis)

---

## Files

```
CV_GunGame/
├── test13.html          # The whole game (1318 lines, zero dependencies)
├── .vscode/launch.json  # Debug config
├── README.md
└── .gitignore
```

---

## Run it

```bash
python -m http.server 8000
# then open http://localhost:8000
```

Camera needs localhost or HTTPS. `file://` won't work.

---

<br>

```
   ____ _   _ _   _     ____ ___  _   _ _   _
  / ___| \ | | \ | |   / ___/ _ \| \ | | \ | |
 | |  _|  \| |  \| |  | |  | | | |  \| |  \| |
 | |_| | |\  | |\  |  | |__| |_| | |\  | |\  |
  \____|_| \_|_| \_|   \____\___/|_| \_|_| \_|
```

## Bu nima?

Floating nishonlarni ko'rsatkich barmog'ingizni siltab otadigan brauzer o'yini. Sichqoncha kerak emas, klaviatura kerak emas — faqat barmoq va kamera.

MediaPipe Hands bilan qilingan. Bitta HTML fayl, hech qanday kutubxona kerak emas.

---

## Qanday o'ynaladi

- Barmoqni ko'rsat = nishonni ol
- Tepaga siltab = o'q uz
- Nishonga tekkan = ball
- Ball yig'ilgach = tezlik oshadi
- Tezlik oshgach = nishonlar tezroq ucha boshlaydi
- 3.0x tezlikda nishonlar raketadek uchadi

Har 5 ball uchun tezlik 0.1x ga oshadi. Maksimal 3.0x.

---

## Ichida nima bor

- 5 xil nishon stili (har xil ranglar va naqshlar)
- Urilganda zarrachalar portlashi (22+ zarracha, gravitatsiya bilan)
- Zarba to'lqini va ekran silkinishi
- Tezlikni dinamik oshirish tizimi
- Flick detektori (tezlikka asoslangan)
- Pinch orqali o'q uzish (bosh + ko'rsatkich barmoq)
- Maxsus smoothing filtrlari (EMA + deadzone + hysteresis)

---

## Ishga tushirish

```bash
python -m http.server 8000
# keyin http://localhost:8000 ni oching
```

Kamera localhost yoki HTTPS talab qiladi. `file://` bilan ishlamaydi.

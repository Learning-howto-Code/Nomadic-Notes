*Generated pariatly wiht the use of AI to improve Clarity
![wiring_diagram](https://github.com/user-attachments/assets/7319788e-9885-478d-abe1-2bd01f249366)


Battery → IP5306

Pack + → B+ pad

Pack – → B– pad

IP5306 → System 5 V

SYS/OUT+ → 5 V rail → Pi VCC (5 V pin) & Amp VCC

SYS/OUT– → common GND

Pi → DAC (I²S)

GPIO 10 (MOSI) → DAC DIN

GPIO 9 (MISO) → DAC not used (keep pull‑down)

GPIO 11 (SCLK) → DAC BCLK

GPIO 18 (PCM‑CLK) → DAC LRC/WS

GND → DAC GND

3.3 V → DAC VCC (if needed)

DAC → MAX9744 Amp

DAC L/R line‑out → AMP L+/R+

DAC GND → AMP GND

Amp → Speaker

AMP OUT+ / OUT– → Speaker ± terminals

Rotary Encoder → Pi

Encoder CLK → Pi GPIO 17 (for example)

Encoder DT → Pi GPIO 27

Encoder SW (push‑button) → Pi GPIO 22

+5 V → Encoder VCC

GND → Encoder GND

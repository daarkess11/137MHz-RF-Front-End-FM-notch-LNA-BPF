# 137MHz-VHF-Satellite-LNA-Receiver

137.5 MHz VHF Downlink RF Front-End for satellite ground stations.

## Quick specs

| Parameter | Value |
|---|---|
| Target frequency | 137.5 MHz VHF Downlink (NOAA-15/18/19, Meteor-M) |
| Active device | PGA-103+ E-PHEMT MMIC |
| Cascaded gain (S21) | 19.2 dB @ 137 MHz |
| Noise Figure (NF) | ~1.84 dB *(simulation/analytical estimate only, not experimentally measured!!)* |
| Out-of-band rejection (88–108 MHz) | -34.8 dB to -50 dB (cascaded) |
| Stability | Unconditionally stable 10 MHz – 4 GHz (R+L shunt & Π-resistor network)¹ |
| PCB | CPWG (50 Ω), via-stitching |

¹ *Above the .s2p model limits (~500 MHz–4 GHz range, depending on component), the stability data comes from simulator extrapolation, not real measurements, check the stability section in the full report before relying on it. Real-world verification with a VNA will follow once I've built and tested the board.*

## Repo structure

- [`/docs`](./docs) — full 16-page engineering report + quick summary
- [`/hardware`](./hardware) — KiCad project files and Gerber zip for manufacturing

If you're looking for the project summary, check the [`/docs`](./docs) folder for the full report. You'll find the KiCad project files and the Gerber zip for manufacturing in the [`/hardware`](./hardware) folder.

Below is a quick summary with the PCB render from KiCad and a couple of screenshots from QUCS-S with the simulation results and schematics.

## ⚠️ Please, do not order this PCB just yet!

I am a student, and as much as I trust my simulations, this is still a prototype. I'm currently buried in exams and labs, so I haven't had the chance to physically solder or test the board with a VNA yet.

I'd hate for you to spend your money on manufacturing a "castaña" (a lemon) only to find out it needs a redesign. Let me be the test pilot. Give me a few months to finish my exams, build the first unit, and verify the real-world performance. If the measurements look good, I'll update this repo and give the "green light" — then you can build your own with confidence!

## Screenshots

*(PCB render from KiCad and QUCS-S simulation plots — add images here)*
## Quick Summary (PCB + Simulations)
### PCB
<img width="1902" height="922" alt="137MHz_RF_FrontEnd" src="https://github.com/user-attachments/assets/9ccd34ab-54cb-4d3c-bd93-b4ec9240ddcb" />

### S[2,1] graphic and measures (only up to 600MHz for a better view, check /docs if you want to see higher frequencies)
<img width="1249" height="763" alt="Captura4" src="https://github.com/user-attachments/assets/ddc5bf62-5228-498d-b46c-dc70e5a33df6" />
<img width="429" height="88" alt="image" src="https://github.com/user-attachments/assets/88863b42-5b3f-4456-b7bd-305d6cdac4c4" />

### Stability
<img width="901" height="718" alt="Captura56" src="https://github.com/user-attachments/assets/da217fe8-5c95-4729-af54-3f1256d212df" />

## Schematics
### Cauer Notch 
<img width="5100" height="1448" alt="Captura4_Nero_AI_Image_Upscaler_Photo_Face" src="https://github.com/user-attachments/assets/a9513412-9d13-4c5e-81b0-508daa168b4a" />

### LNA
<img width="4912" height="2696" alt="Captura57_Nero_AI_Image_Upscaler_Photo_Face" src="https://github.com/user-attachments/assets/cb6baafe-f084-4b75-ab65-5b1752a7dac5" />

### Band-Pass Butterworth
<img width="1036" height="513" alt="image" src="https://github.com/user-attachments/assets/7b104efb-104a-4022-8c3c-e5752f51ca61" />


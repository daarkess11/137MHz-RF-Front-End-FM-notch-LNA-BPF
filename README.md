# 137MHz-VHF-Front-End (Work-in-Progress)

137.5 MHz VHF Downlink RF Front-End for satellite ground stations.

## Quick specs

| Parameter | Value |
|---|---|
| Target frequency | 137.5 MHz VHF Downlink (NOAA-15/18/19, Meteor-M) |
| Active device | PGA-103+ E-PHEMT MMIC |
| Cascaded gain (S21) | 22 dB @ 137 MHz |
| Noise Figure (NF) | ~1.84 dB *(simulation/analytical estimate only, not experimentally measured!!)* |
| Out-of-band rejection (88–108 MHz) | -33.3 dB to -48.8 dB (cascaded) |
| Stability | Unconditionally stable 10 MHz – 4 GHz (R+L shunt)¹ |
| PCB | CPWG (50 Ω), W=1.25mm, H=1.6mm, S=0.24mm, εr=4.5, t=1oz (35µm) |

¹*Above the available .s2p model limits, the stability curves rely on simulator extrapolation and should be treated as indicative rather than physically validated results. See the stability section in the full report for the modelling limitations.*


## Design Approach

- **Simulation:** QUCS-S with real component S-parameters
- **Validation:** Experimental VNA testing pending
- **EM simulation:** Not performed (CPWG geometry validated with calculator/published formulas at 137 MHz)
## Repo structure

- [`/docs`](./docs) — full 16-page engineering report
- [`/hardware`](./hardware) — KiCad project files + BOM list
  
Below is a quick summary with the PCB render from KiCad and a couple of screenshots from QUCS-S with the simulation results and schematics.

## ⚠️ Prototype Status

The design has been fully simulated and theoretically verified. Experimental verification will follow once the PCB has been fabricated and tested with a VNA.

# Screenshots
*Note: I used .s2p files from the manufacturer datasheets for the simulations, not ideal component models, ideal symbols only show up when they make the schematic easier to read.*

### PCB
<img width="1675" height="892" alt="137MHz_RF_FrontEnd" src="https://github.com/user-attachments/assets/1ca23064-942b-4b39-9c42-43a7bb09fac7" />

### S[2,1] graphic and measures (only up to 600MHz for a better view, check /docs if you want to see higher frequencies)
<img width="1055" height="595" alt="image" src="https://github.com/user-attachments/assets/af07083d-4285-4487-982a-5e9da14dffb9" />

### Stability
<img width="1020" height="795" alt="image" src="https://github.com/user-attachments/assets/c5721422-311d-4e02-8eda-6807e5bf5c35" />

## Schematics
### Cauer Notch 
<img width="5100" height="1448" alt="Captura4_Nero_AI_Image_Upscaler_Photo_Face" src="https://github.com/user-attachments/assets/a9513412-9d13-4c5e-81b0-508daa168b4a" />

### LNA
<img width="792" height="571" alt="image" src="https://github.com/user-attachments/assets/699259cd-4e96-440b-b4be-1e2ca5812e42" />

### Band-Pass Butterworth
<img width="1036" height="513" alt="image" src="https://github.com/user-attachments/assets/7b104efb-104a-4022-8c3c-e5752f51ca61" />


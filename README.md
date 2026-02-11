# PM2.5 // IKEDA

Real-time global air quality (PM2.5) data visualization inspired by the aesthetic of [Ryoji Ikeda](https://www.ryojiikeda.com/) — number streams, binary patterns, barcodes, and data grids over a pure black canvas.

Single self-contained HTML file. No build tools. Just open in a browser.

## Demo

Open `index.html` in any modern browser (Chrome, Firefox, Safari).

## Features

- **5 simultaneous visual layers** rendered on a fullscreen p5.js canvas
- **Real-time data** from [OpenAQ API v3](https://openaq.org/) with simulated fallback
- **20 cities** tracked: Delhi, Beijing, Lahore, Dhaka, Kolkata, CDMX, Santiago, Lima, Jakarta, Cairo, Mumbai, Karachi, Chengdu, Hanoi, Bogota, Sao Paulo, Bangkok, Seoul, Los Angeles, London
- **Responsive** — adapts layout, density, and font sizes for mobile screens
- **Zero dependencies** beyond p5.js (loaded from CDN)

## Visual Layers

| Layer | Description |
|-------|-------------|
| Number Rain | Vertical columns of PM2.5 values falling at pollution-proportional speeds |
| Binary Streams | Horizontal bands of 12-bit binary-encoded PM2.5 readings |
| Barcode Bands | Scrolling barcode patterns where bar width = normalized PM2.5 level |
| Data Grid | Center-screen matrix of city codes + values with glitch/scramble effects |
| Coordinate Tickers | GPS coordinates, station IDs, and UTC timestamps scrolling at screen edges |

## Color System

- Default: white on black, varying opacity (0.1–0.8)
- PM2.5 > 200 (very unhealthy): subtle red micro-pulse
- PM2.5 > 300 (hazardous): visible red glitch

## Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Pause / Resume | Click | Tap |
| Fullscreen | `F` | — |
| Refresh data | `R` | — |
| Save screenshot | `S` or PNG button | PNG button |

## Tech

- **p5.js 1.9.4** — canvas rendering
- **OpenAQ API v3** — PM2.5 sensor data (refreshed every 2 min)
- **Simulated fallback** — realistic values based on city averages when API is unavailable

## License

MIT

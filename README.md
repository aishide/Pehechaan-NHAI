<!-- Animated High-Tech HUD Scanner Banner in Indian Flag Accents -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 320" width="100%" height="320" style="background:#030712; font-family:'Inter',system-ui,-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif; border-radius:16px; border: 1px solid rgba(255, 255, 255, 0.08);">
  <style>
    @keyframes scan {
      0% { transform: translateY(0px); opacity: 0.3; }
      50% { transform: translateY(200px); opacity: 0.9; }
      100% { transform: translateY(0px); opacity: 0.3; }
    }
    @keyframes pulse {
      0% { opacity: 0.2; transform: scale(0.98); }
      50% { opacity: 0.5; transform: scale(1.02); }
      100% { opacity: 0.2; transform: scale(0.98); }
    }
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    .scanner-line {
      animation: scan 4.5s ease-in-out infinite;
      stroke: url(#laser-grad);
      filter: drop-shadow(0 0 8px rgba(0, 210, 255, 0.8));
    }
    .hud-bg {
      fill: none;
      stroke: rgba(255, 255, 255, 0.03);
      stroke-width: 1;
    }
    .hud-circle-outer {
      transform-origin: 400px 140px;
      animation: spin 30s linear infinite;
    }
    .hud-circle-inner {
      transform-origin: 400px 140px;
      animation: spin 15s linear infinite reverse;
    }
    .pulse-glow {
      transform-origin: 400px 140px;
      animation: pulse 3s ease-in-out infinite;
    }
    .flag-saffron { fill: #FF9933; }
    .flag-white { fill: #FFFFFF; }
    .flag-green { fill: #138808; }
  </style>

  <defs>
    <linearGradient id="laser-grad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#FF9933" />
      <stop offset="30%" stop-color="#00D2FF" />
      <stop offset="50%" stop-color="#FFFFFF" />
      <stop offset="70%" stop-color="#00D2FF" />
      <stop offset="100%" stop-color="#138808" />
    </linearGradient>
    
    <pattern id="dot-grid" width="24" height="24" patternUnits="userSpaceOnUse">
      <circle cx="2" cy="2" r="1" fill="#1e293b" />
    </pattern>
  </defs>

  <!-- Dot grid background -->
  <rect width="800" height="320" fill="url(#dot-grid)" />

  <!-- Corner Targeting Reticles -->
  <path d="M 30,50 L 30,30 L 50,30" fill="none" stroke="rgba(255, 255, 255, 0.2)" stroke-width="2" />
  <path d="M 770,50 L 770,30 L 750,30" fill="none" stroke="rgba(255, 255, 255, 0.2)" stroke-width="2" />
  <path d="M 30,270 L 30,290 L 50,290" fill="none" stroke="rgba(255, 255, 255, 0.2)" stroke-width="2" />
  <path d="M 770,270 L 770,290 L 750,290" fill="none" stroke="rgba(255, 255, 255, 0.2)" stroke-width="2" />

  <!-- Center Biometric Scanning Zone -->
  <circle cx="400" cy="140" r="110" class="hud-bg" stroke="rgba(255, 255, 255, 0.05)" stroke-width="2" />
  <circle cx="400" cy="140" r="95" fill="none" stroke="#00D2FF" stroke-width="1.5" stroke-dasharray="10 40 30 20" opacity="0.3" class="hud-circle-outer" />
  <circle cx="400" cy="140" r="80" fill="none" stroke="#FF9933" stroke-width="1" stroke-dasharray="5 15 2 8" opacity="0.4" class="hud-circle-inner" />

  <!-- Face Bounding Box HUD -->
  <rect x="345" y="85" width="110" height="110" rx="10" fill="none" stroke="rgba(0, 210, 255, 0.15)" stroke-width="1" class="pulse-glow" />
  <path d="M 345,100 L 345,85 L 360,85 M 440,85 L 455,85 L 455,100 M 455,180 L 455,195 L 440,195 M 360,195 L 345,195 L 345,180" fill="none" stroke="#00D2FF" stroke-width="2" />

  <!-- Face Scanning Line -->
  <line x1="100" y1="40" x2="700" y2="40" stroke-width="3.5" class="scanner-line" />

  <!-- Indian National Flag Accent Stripes -->
  <g transform="translate(300, 20)">
    <rect x="0" y="0" width="67" height="3" class="flag-saffron" />
    <rect x="67" y="0" width="66" height="3" class="flag-white" />
    <rect x="133" y="0" width="67" height="3" class="flag-green" />
  </g>

  <!-- Typography -->
  <text x="400" y="265" text-anchor="middle" font-weight="900" font-size="34" fill="#ffffff" letter-spacing="8">PEHCHAAN</text>
  <text x="400" y="288" text-anchor="middle" font-weight="600" font-size="11" fill="#64748b" letter-spacing="4">NHAI SECURE ON-DEVICE VERIFICATION</text>
</svg>

<br/>

<div align="center">
  
  [![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-blue?style=flat-square&logo=react)](https://reactnative.dev)
  [![ML-Engine](https://img.shields.io/badge/ML%20Engine-TFLite%20On--Device-success?style=flat-square&logo=tensorflow)](https://tensorflow.org)
  [![Database](https://img.shields.io/badge/Database-SQLite%20(WAL)-orange?style=flat-square&logo=sqlite)](https://sqlite.org)
  [![Authentication](https://img.shields.io/badge/Auth-Offline%20First-red?style=flat-square)](#)
  [![Compliance](https://img.shields.io/badge/Compliance-NHAI%20DataLake-008080?style=flat-square)](#)

  **Pehchaan (पहचान)** is a high-performance, completely offline-first facial authentication and active liveness verification system specifically engineered to secure contractor labor tracking, toll plaza handovers, and highway patrol attendance within the **National Highways Authority of India (NHAI)** ecosystem.
</div>

---

## 🏛️ Government of India & NHAI Context

NHAI infrastructure projects are highly distributed and frequently executed in remote regions lacking cellular coverage, such as deep mountain passes, border corridors, or underground tunnels. Standard cloud-based biometric systems fail in these conditions.

Pehchaan resolves this by deploying specialized, lightweight deep neural networks directly onto field personnel's mid-range mobile hardware. All face detection, geometric alignment, and embedding comparisons occur strictly in the device's CPU register layer, making biometric checks fast, secure, and 100% network-independent.

---

## ⚙️ System Architecture & Inference Pipeline

The verification pipeline operates in a sequential, memory-safe loop designed to complete under **150 milliseconds**:

```mermaid
flowchart LR
    A[Camera Capture] --> B[Resize 640x640]
    B --> C[RGBA Byte Decode]
    C --> D[Similarity Warp & Align]
    D --> E[Normalize Input]
    E --> F[TFLite Model Pass]
    F --> G[192-dim Embedding]
    G --> H[Cosine Similarity vs SQLite]
```

### 1. Affine Similarity Transformation
To normalize facial rotation, skew, and size differences caused by camera angles or worker heights, the alignment engine maps the face to a canonical $112 \times 112$ bounding box:
* Computes the angle ($\theta = \text{atan2}(dy, dx)$) and the scale factor ($s = \frac{\text{canonicalDistance}}{\text{actualDistance}}$) based on eye landmarks.
* Warps the pixel canvas using inverse coordinate mapping to center eye, nose, and mouth anchors:
  $$srcX = \frac{(x - t_x)\cos(-\theta) + (y - t_y)\sin(-\theta)}{s}$$

### 2. On-Device Model Inference
* **Normalization:** Pixel buffers are processed in memory and scaled to $[-1.0, 1.0]$.
* **TFLite Execution:** The $112 \times 112 \times 3$ tensor is executed on the CPU registers via native `react-native-fast-tflite` bindings, loading a **5.2 MB** `mobilefacenet.tflite` model.
* **Vector Comparison:** Matches the extracted 192-dimensional vector against stored templates using **Cosine Similarity**:
  $$\text{Similarity}(\vec{A}, \vec{B}) = \frac{\vec{A} \cdot \vec{B}}{\|\vec{A}\|_2 \|\vec{B}\|_2}$$
  Matches are confirmed if similarity is $\ge 0.65$.

---

## 👁️ Challenge-Response Liveness Tracking

To block spoofing attacks using printed headshots or high-definition tablets, Pehchaan integrates a randomized challenge-response validator:

| Challenge Type | Target Metric | Success Condition | Target Threat Prevented |
| :--- | :--- | :--- | :--- |
| **👁️ Blink Cycle** | Eye Aspect Ratio (EAR) | Average EAR drops $< 0.3$ then reopens $> 0.7$ | High-Res Printed Photographs |
| **🔄 Head Turn** | Rotation Yaw Angle | Yaw rotation shifts $\ge \pm 20^\circ$ from baseline | 2D Screen Replay Attacks |
| **😊 Smile Check** | Smile Probability Index | Probability index exceeds $0.75$ | Static Silicon Masks |

---

## 📍 Offline Caching & S3 Sync Mechanics

Pehchaan uses a dual-table caching database layout in SQLite to minimize local disk footprint:

* **Non-Blocking GPS:** Background workers prefetch high-accuracy GPS coordinates (`Location.Accuracy.High`) asynchronously when the camera screen mounts. During face snap, coordinates are read instantly from the memory cache in **0ms**, avoiding any camera shutter delay.
* **Dual-Table Scheme:**
  * `attendance_records` stores detailed, geo-stamped logs.
  * `unique_attendance_days` stores small index records of employee IDs and dates.
* **Delta Sync & Purging:** When internet coverage is restored, the sync manager uploads the detailed logs to AWS S3 using direct REST PUT calls signed locally via Web Crypto SigV4. It then purges successfully synced detailed records from the device to prevent disk bloat, while preserving `unique_attendance_days` so local calendars and stats continue to work offline.

---

## 🚀 Installation & Local Run

### System Environment
* **Android:** API Level 26+ (Android 8.0+)
* **iOS:** iOS 12.0+

### Dependencies Setup
Run the following inside your project directory:
```bash
npx expo install react-native-vision-camera expo-sqlite expo-image-manipulator expo-location expo-linear-gradient react-native-reanimated
```

### Environment Config (`.env`)
```env
EXPO_PUBLIC_AWS_REGION=ap-south-1
EXPO_PUBLIC_S3_BUCKET=pehchaan-attendance-data
EXPO_PUBLIC_AWS_ACCESS_KEY_ID=YOUR_AWS_ACCESS_KEY_ID
EXPO_PUBLIC_AWS_SECRET_ACCESS_KEY=YOUR_AWS_SECRET_ACCESS_KEY
```

---

## 👥 Contributors

Our core engineering and design team:

<table align="center" border="0" cellpadding="10" cellspacing="0">
  <tr align="center">
    <td width="33%">
      <img src="https://github.com/identicons/aishide.png" width="80" style="border-radius:50%;" /><br/>
      <strong>Aishi De</strong><br/>
      <sub>Core Engineer & PM</sub>
    </td>
    <td width="33%">
      <img src="https://github.com/identicons/parthivabhani.png" width="80" style="border-radius:50%;" /><br/>
      <strong>Parthiv Abhani</strong><br/>
      <sub>ML & Pipeline Arch</sub>
    </td>
    <td width="33%">
      <img src="https://github.com/identicons/Svizzcodes.png" width="80" style="border-radius:50%;" /><br/>
      <strong>Shlok Vij</strong><br/>
      <sub>Biometric Core Developer</sub>
    </td>
  </tr>
</table>

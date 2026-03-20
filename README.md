# Smart Agriculture Assistant

An IoT-powered precision farming assistant that recommends optimal crops and fertilizers based on real-time sensor data.

## What It Does

- Reads soil and environmental sensor data (N, P, K levels, temperature, humidity, pH, rainfall) from Arduino hardware
- Predicts the best crop to plant and optimal fertilizer amounts using trained ML models
- Displays real-time recommendations and historical trends on a web dashboard

## Architecture

```
Arduino sensors → WebSocket server (Node.js/Express) → MongoDB
                                    ↓
                  Web dashboard (EJS + Chart.js)
                                    ↓
                     Python ML models (scikit-learn)
                       ├─ Crop prediction
                       └─ Fertilizer recommendation
```

## Stack

- **Backend**: Node.js, Express, WebSocket, MongoDB, Mongoose, JWT auth
- **ML**: Python, scikit-learn, pandas
- **Hardware**: Arduino with soil NPK and weather sensors
- **Frontend**: EJS templates, Chart.js

## Setup

```bash
npm install
pip install -r requirements.txt
```

Add to `.env`:
```
MONGODB_URI=your_connection_string
SECRET=your_jwt_secret
```

```bash
node index.js
```

> This is the final version. Earlier iterations: [ACC-v1](https://github.com/minh-stakc/ACC-v1), [ACC-v0](https://github.com/minh-stakc/ACC-v0).

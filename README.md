# Player Re-Identification in Football Broadcasts

This project implements real-time object detection and visual re-identification to ensure consistent player tracking across frames—even after occlusions or re-entry into the camera view.

---

## 🎥 Demo Videos

- ▶️ **Detection Output**:
  [![Detection Video](https://img.youtube.com/vi/aa5JK6-TQoI/maxresdefault.jpg)](https://youtu.be/aa5JK6-TQoI)
  [Watch Detected Video](https://drive.google.com/file/d/1deGHYQ-Ajzrs7ixgt3QeVnO2uEIHkuiw/view?usp=share_link)

- 🎯 **Tracking with Re-ID Output**:
  [![Tracking Video](https://img.youtube.com/vi/Fc4SgEace-Q/maxresdefault.jpg)](https://youtu.be/Fc4SgEace-Q)
  [Watch Tracked Video](https://drive.google.com/file/d/1deGHYQ-Ajzrs7ixgt3QeVnO2uEIHkuiw/view?usp=share_link)

---

## 📁 Folder Structure
```
project/
├── assets/
│   └── 15sec_input_720p.mp4
├── models/
│   └── best.pt
├── output/
│   ├── tracked_frames/
│   └── tracked_video.mp4
├── detect.py
├── pyproject.toml
├── uv.lock
└── README.md
```

## ⚙️ Setup Instructions

### Step 1: Clone the repository
```bash
git clone https://github.com/VIDIT0906/SoccerPlayer_ReID.git
cd SoccerPlayer_ReID
```

### Step 2: Virtual Environment initializtion
### Alternative 1: If uv is available
``` bash
uv run detect.py
```

### Alternative 2: If pip is available 
**### **Create and activate a virtual environment (recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

**Install dependencies**
```bash
pip install -r requirements.txt
```
**Or install manually:**
```bash
pip install opencv-python torch torchvision numpy pillow scikit-learn ultralytics torchreid
```

### Step 3: Download YOLOv8 model weights
Place the `best.pt` file inside the `models/` or project root directory. This should be your fine-tuned YOLOv11 model for player, referee, goalkeeper, and ball detection.

---

## ▶️ Running the Code

```bash
python detect.py
```
- Outputs: `output/tracked_frames/` (annotated images) and `tracked_video.mp4`

---

## 🛠 Dependencies
- Python 3.8+
- OpenCV
- Ultralytics (YOLOv8)
- Torch + TorchVision
- Torchreid
- scikit-learn
- Pillow

---

# 🚗 Automatic Number Plate Recognition (ANPR) using Python & YOLOv

A computer vision project that leverages **YOLOv** (You Only Look Once - version X) and **Python** to detect and recognize vehicle number plates from video footage in real-time or batch mode.

---

## 📽️ How it Works

The system ingests a video stream (MP4 or live feed), extracts frames using OpenCV, and runs a YOLOv-based object detection model to identify and localize number plates. The detected regions are then passed through a recognition pipeline for text extraction (OCR).

---

## 🎯 Features

- 🧠 **YOLOv-based real-time object detection**
- 🖼️ **Frame-by-frame video processing using OpenCV**
- 🔍 **OCR-based plate number recognition**
- 📂 **Saves annotated frames and plate text data**
- ⏱️ **Batch & real-time video input support**

---

## 📸 Example Outputs


### 📝 Extracted Plate Numbers  'csv'
| Frame | Plate Number |
|-------|--------------|
| 12    | KA05MJ2333   |
| 43    | MH12DE1433   |
| 97    | TN09BA2001   |

---

## 🧱 System Architecture

```

[ Video File / Live Feed ]
    ↓
[ Frame Extraction ]
    ↓
[ YOLOv Detection ]
    ↓
[ Plate Crop & Text Extraction ]
   ↓
[ Results & Annotation ]

```

---

## 🧰 Tech Stack

| Component       | Technology      |
|----------------|-----------------|
| Programming    | Python 3.x       |
| Detection      | YOLOv (e.g., YOLOv5/v7) |
| Video Handling | OpenCV           |
| Text Extraction| Tesseract OCR or EasyOCR |
| Display & Save | Matplotlib, cv2.imwrite |

---

## 📁 Folder Structure

```

ANPR-YOLOv/
├── models/                  # YOLOv weights and config
├── videos/                  # Input videos
├── output/                  # Annotated frames and text output
├── screenshots/             # For README
├── anpr.py                  # Main script
├── detector.py              # YOLOv wrapper
├── recognizer.py            # OCR processing
├── utils.py                 # Helper functions
├── requirements.txt
└── README.md

````

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/automatic-number-plate-recognition-python-yolov.git
cd automatic-number-plate-recognition-python-yolov
````

### 2. Install dependencies

Use a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Add YOLOv Weights

Download your YOLOv weights (e.g., `best.pt`) and place it in the `models/` directory.

### 4. Run the system

```bash
python anpr.py --video videos/sample.mp4 --output output/
```

---

## ⚙️ Configuration Options

| Flag        | Description                | Example              |
| ----------- | -------------------------- | -------------------- |
| `--video`   | Path to input video        | `videos/highway.mp4` |
| `--output`  | Output folder for results  | `output/`            |
| `--weights` | YOLOv weights file path    | `models/best.pt`     |


---

## 🚀 Future Improvements

* 🌐 Cloud-based plate verification
* 📦 Export results in CSV/JSON
* 🧪 GUI with Tkinter or Streamlit
* 🔐 Vehicle database integration
* 🧠 dashcam product

---

## 📃 License

MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgments

* YOLOv community for pretrained models
* OpenCV for image & video processing
* Tesseract & EasyOCR for text recognition


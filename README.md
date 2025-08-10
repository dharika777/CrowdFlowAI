
# 🧠 CrowdFlowAI: Intelligent Pedestrian Flow Monitoring for Large Gatherings

This project implements an AI-powered system that monitors and analyzes pedestrian flow in crowded gatherings like the Kumbh Mela. It uses deep learning for detection and multi-object tracking to analyze crowd movement and potential stampede risks.

---

## 🚩 Problem Statement

Mass gatherings pose a high risk of uncontrolled pedestrian flow and stampede-like conditions. This system aims to:

- Detect and count pedestrians in real-time.
- Track individual and collective movements.
- Simulate panic scenarios.
- Detect early signs of stampedes using flow analysis and anomaly detection.

---

## 📂 Folder Structure

```
Group53_CrowdFlowAI/
├── videos/                    # Folder to place input video files (01.mp4 to 20.mp4)
├── output_videos/            # Auto-generated folder for saving output videos with tracking
├── head_medium.pt             # YOLOv8 model weights for head detection
├── head_detection.ipynb      # Jupyter notebook for entire pipeline
├── tracking_log.csv          #  CSV log for detections and  tracking
├── requirements.txt          # Python dependencies
└── README.md                 # This file
```

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/akshay9024/Group53_CrowdFlowAI.git
cd CrowdFlow
```

### 2. Install Dependencies

Create a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate  # or `venv\Scripts\activate` on Windows
```

Install required packages:

```bash
pip install -r requirements.txt
```

### 3. Download Model Weights

Place the following model file in the `models/` directory:

- `head_medium.pt`: [Download here](https://github.com/Abcfsa/YOLOv8_head_detector/raw/main/medium.pt)

Also ensure `yolov8n.pt` is available via `ultralytics`.

---

## ▶️ How to Run

### Using Jupyter Notebook

1. Open `head_detection.ipynb` in Jupyter or Colab.
2. Ensure that:
   - Input videos are in the `videos/` folder.
   - Paths are correctly set in the code:  
     - `input_folder = "videos"`  
     - `output_folder = "output_videos"`

### Output

- Tracked videos will be saved in `output_videos/`
- A `tracking_log.csv` file will be generated for further analysis.

---

## 🧠 Techniques Used

- **YOLOv8** for pedestrian and head detection.
- **DeepSORT** for robust object tracking.
- **OpenCV** for frame extraction and video manipulation.
- **CSV Logging** for tracking analytics.

---


## 📌 To Do / Extensions

- ✅ Panic simulation using agent-based models.
- 🔲 Anomaly detection on trajectory data.
- ✅ Heatmap and risk zone visualizations.
- 🔲 Dashboard integration (e.g., with Streamlit).

---

## 📁 Requirements


```txt
ultralytics
deep_sort_realtime
opencv-python-headless
matplotlib
pandas
torch
torchvision
```

---

## 📷 Sample Results
![alt text](<WhatsApp Image 2025-05-03 at 16.33.25.jpeg>)
Explore more output videos with tracked pedestrians and ID labels  saved in `[Results](https://drive.google.com/file/d/1MxUTAs9juJsxAt73dGspiYHMIcWYPfFk/view?usp=share_link)
.

## Presentation and Output

You can find the complete project presentation, model outputs, and demonstration at the following link:

🔗 [Project Presentation and Output (Canva)](https://www.canva.com/design/DAGmeBgjDFY/OYlEzlf3RberhFJSjqfh5Q/edit?utm_content=DAGmeBgjDFY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

---

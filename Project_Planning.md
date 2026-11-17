# 🏀 Division of Work

### MEMBER 1 – Dataset Preparation & AI Model Development
* **Responsibility:** Roboflow and Computer Vision Dataset
* **Deadline:** Day 2
* **Software and tools:** Roboflow, Google Drive, Google Colab, Python, OpenCV

**Tasks:**
* Create the Roboflow workspace and project.
* Record basketball footage using a mobile phone (coordinate with all members).
* Extract video frames using OpenCV.
* Upload approximately 150–250 selected images to Roboflow.
* Annotate three classes:
  * `Player`
  * `Basketball`
  * `Hoop`
* Generate the dataset version.
* Train an object detection model.
* Evaluate model performance using Precision, Recall, and mAP.
* Share model ID and class mapping with Member 2.

**GitHub Deliverables:**
* `notebooks/01_data_preparation.ipynb`
* Dataset preparation documentation in `README.md`
* Model configuration and evaluation results

---

### MEMBER 2 – Object Detection & Player Tracking
* **Responsibility:** Python Video Processing and Tracking
* **Deadline:** Day 5
* **Software and tools:** Python, Google Colab, Roboflow Inference, OpenCV, Supervision, ByteTrack, Pandas

**Tasks:**
* Connect the trained Roboflow model to Python.
* Upload and process basketball footage.
* Detect players, basketballs, and hoops.
* Implement ByteTrack to assign player IDs.
* Track player movement across video frames.
* Calculate the number of players detected per frame.
* Extract timestamps and player coordinates.
* Develop basic basketball shot detection.
* Export tracking and occupancy data into CSV files.

**GitHub Deliverables:**
* `notebooks/02_object_detection.ipynb`
* `notebooks/03_player_tracking.ipynb`
* `src/detection.py`
* `src/tracking.py`
* `src/shot_detection.py`
* `outputs/player_tracking.csv`
* `outputs/occupancy.csv`

---

### MEMBER 3 – Camera Calibration & Business Analytics
* **Responsibility:** Court Mapping, Occupancy and Heatmaps
* **Deadline:** Day 5
* **Software and tools:** Python, OpenCV, NumPy, Pandas, Matplotlib, Seaborn, Google Colab

**Tasks:**
* Identify court reference points from the video.
* Perform camera calibration using perspective transformation (Homography).
* Convert player image coordinates into court coordinates.
* Divide the court into six analytical zones.
* Calculate court occupancy percentage.
* Calculate average and maximum player counts.
* Analyse occupancy by hour using timestamped recordings.
* Generate player movement heatmaps.
* Calculate time spent in different court zones.
* Prepare analytical charts and visualizations.

**GitHub Deliverables:**
* `notebooks/04_court_analytics.ipynb`
* `src/calibration.py`
* `src/occupancy.py`
* `src/heatmap.py`
* `outputs/heatmap.png`
* Occupancy analysis and visualizations

---

### MEMBER 4 – Dashboard Development & Integration
* **Responsibility:** Final Application and Project Integration
* **Deadline:** Day 6
* **Software and tools:** Python, Streamlit, Pandas, Matplotlib, Seaborn, GitHub, Google Colab

**Tasks:**
* Create the Streamlit dashboard layout.
* Develop a main statistics section.
* Display current and maximum player counts.
* Display made shots, missed shots, and shooting percentage.
* Display court occupancy statistics.
* Integrate hourly occupancy graphs.
* Display player movement heatmaps.
* Integrate outputs from Members 2 and 3.
* Test the complete application.
* Prepare project documentation and presentation.

**Dashboard Sections:**
1. Overview
2. Player Detection & Tracking
3. Shot Analytics
4. Court Occupancy
5. Court-Zone Heatmap
6. Reports

**GitHub Deliverables:**
* `dashboard/app.py`
* `requirements.txt`
* Final `README.md`
* Application screenshots and presentation

---

## 3. Seven-Day Execution Schedule

| Day | Activities | Members |
| :--- | :--- | :--- |
| **Day 1** | GitHub setup, mobile video recording, Roboflow project creation | All |
| **Day 2** | Frame extraction, image annotation, dataset generation and model training | M1 |
| **Day 3** | AI integration, object detection and initial player tracking | M1, M2 |
| **Day 4** | Tracking completion, calibration and court-zone mapping | M2, M3 |
| **Day 5** | Occupancy, heatmaps, shot analytics and CSV exports | M2, M3 |
| **Day 6** | Dashboard integration, testing and debugging | M4, All |
| **Day 7** | Final testing, report preparation and presentation | All |

> **Parallel Work Strategy:** Members 2, 3, and 4 should begin using sample or dummy data while Member 1 develops the model. Do not wait for all modules to be completed before starting integration.

---

# 🏀 Basketball Court Analytics System

> **7-Day Project Execution Plan | Team of 4**

An AI-powered computer vision system built with Python to monitor player activity, track basketball shots, analyze court occupancy, perform camera calibration, and generate player movement heatmaps.

---

## 📋 Table of Contents
- [Project Objective](#-project-objective)
- [Technology Stack](#-technology-stack)
- [Repository Structure](#-repository-structure)
- [Getting Started & GitHub Setup](#-getting-started--github-setup)
- [Team Roles & Division of Work](#-team-roles--division-of-work)
- [7-Day Execution Schedule](#-7-day-execution-schedule)
- [GitHub Collaboration Rules](#-github-collaboration-rules)
- [Final Deliverables & Success Criteria](#-final-deliverables--success-criteria)

---

## 🎯 Project Objective

Develop a computer vision-based basketball court analytics system using AI and Python to:
* Detect players, basketballs, and hoops in video footage.
* Track player movement across frames and log player counts/timestamps.
* Map camera coordinates to a 2D court layout via camera calibration (Homography).
* Analyze court occupancy across 6 distinct court zones and hourly intervals.
* Generate player movement heatmaps and track basic shot statistics.
* Present insights in an interactive **Streamlit** dashboard.

---

## 🛠 Technology Stack

| Software / Tool | Purpose |
| :--- | :--- |
| **GitHub** | Code sharing, task allocation, and version control |
| **Roboflow** | Image annotation, dataset preparation, and AI model training |
| **Google Colab** | Cloud-based Python development and GPU execution |
| **Python** | Core programming and analytics |
| **OpenCV** | Video processing and camera calibration |
| **YOLO / Roboflow Inference** | Object detection (`Player`, `Basketball`, `Hoop`) |
| **ByteTrack & Supervision** | Multi-object player tracking and ID assignment |
| **Pandas & NumPy** | Data processing, transformation, and calculations |
| **Matplotlib & Seaborn** | Analytical graphs and movement heatmaps |
| **Streamlit** | Final interactive web dashboard |
| **Google Drive** | Storage and sharing of large raw video footage and datasets |

---

## 📁 Repository Structure

```text
basketball-court-analytics/
│
├── data/
│   ├── raw_videos/          # Local storage for raw video clips (ignored in Git)
│   ├── extracted_frames/    # Frames extracted for annotation
│   └── processed/           # Cleaned/transformed intermediate datasets
│
├── models/                  # Trained weights / model configuration metadata
│
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_object_detection.ipynb
│   ├── 03_player_tracking.ipynb
│   └── 04_court_analytics.ipynb
│
├── src/
│   ├── detection.py         # Roboflow/YOLO inference logic
│   ├── tracking.py          # ByteTrack player tracking & counting
│   ├── calibration.py       # Homography & perspective transformation
│   ├── occupancy.py         # Court-zone & hourly occupancy calculations
│   ├── shot_detection.py    # Shot attempt & make/miss detection
│   └── heatmap.py           # Spatial movement heatmap generation
│
├── dashboard/
│   └── app.py               # Main Streamlit dashboard application
│
├── outputs/
│   ├── player_tracking.csv  # Frame-by-frame player IDs & coordinates
│   ├── occupancy.csv        # Timestamped player counts & zone occupancy
│   ├── shots.csv            # Logged shot attempts and outcomes
│   └── heatmap.png          # Generated court movement heatmap
│
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
└── .gitignore               # Ignored files (videos, API keys, cache)

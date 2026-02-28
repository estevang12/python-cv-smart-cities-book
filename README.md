# Python and Computer Vision for Smart Cities

Official companion repository for the book:
Companion code and practical workshops for Smart City, Airport, and UAM Computer Vision systems using Python and YOLO

**"Python and Computer Vision for Smart Cities: Applications in Airports, Heliports, and Urban Mobility"**  
By Estevan R. Gómez Torres

---

## 📌 About This Repository

This repository contains the practical workshops, code examples, and mini-projects developed throughout the book.

The goal is to provide reproducible implementations of Computer Vision systems applied to:

- Smart City traffic monitoring
- Airport ground operations
- Runway safety and apron monitoring
- Intelligent parking systems
- Urban Air Mobility (UAM) and vertiport operations
- Edge AI deployments

All examples are implemented using Python, OpenCV, and YOLO (Ultralytics).

---

## 🧠 Topics Covered

- Image Processing Fundamentals
- OpenCV Core Operations
- Object Detection with YOLO
- Zone-based Safety Monitoring
- Traffic Analytics
- Vertiport Monitoring Systems
- Smart Infrastructure Perception Pipelines

---

## 📂 Repository Structure
chapter_1/
chapter_2/
chapter_3/
chapter_4/
workshop_traffic/
workshop_airport_safety/
workshop_uam/
chapter_5/
notebooks/
sample_frames/



Each chapter folder contains scripts and workshop implementations corresponding to the book.

---

## ⚙ Requirements

Install dependencies:

```bash
pip install ultralytics opencv-python numpy matplotlib

🎥 Video and Dataset Notes

⚠️ Videos are NOT included in this repository due to copyright restrictions.

Users are encouraged to work with:

Publicly available airport CCTV footage

Smart City traffic videos

Educational UAM / vertiport simulations

Public domain or self-recorded material

Suggested sources include:

YouTube (educational use)

Pexels

Pixabay

Government open-data portals

Please ensure compliance with usage rights and copyright policies

🚀 Example Workshop Execution
from ultralytics import YOLO
import cv2

model = YOLO("yolov8n.pt")
cap = cv2.VideoCapture("your_video.mp4")

while True:
    ret, frame = cap.read()
    if not ret:
        break

    results = model(frame)
    annotated = results[0].plot()

    cv2.imshow("Detection", annotated)
    if cv2.waitKey(1) & 0xFF == 27:
        break

cap.release()
cv2.destroyAllWindows()
🎯 Educational Purpose

This repository is designed for:

University students

Researchers

Smart City engineers

Airport operations professionals

AI practitioners working on infrastructure analytics

⚖ License

This project is released under the MIT License.

🌎 Author

Estevan R. Gómez Torres
Researcher in Artificial Intelligence and Smart Infrastructure Systems

📖 Citation

If you use this material in academic or professional work, please cite:

Gómez Torres, E. R. (2025). Python and Computer Vision for Smart Cities: Applications in Airports, Heliports, and Urban Mobility.

⭐ Contributing

Contributions are welcome for educational improvements and reproducible research extensions.



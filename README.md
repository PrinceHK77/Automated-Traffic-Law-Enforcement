# 🚦 Traffic Law Enforcement System – Helmet Violation Detection

An AI-powered traffic surveillance system designed to automatically detect **helmet violations** by two-wheeler riders using traffic signal camera feeds. The system captures vehicle images, extracts number plates using OCR, and automatically raises challans through integration with the RTO database.

---

## 🧠 Technologies Used

- **Programming Language**: Python  
- **Libraries & Frameworks**:
  - OpenCV (Computer Vision & Image Processing)
  - Tesseract OCR (Number Plate Recognition)
  - NumPy, Pandas
- **AI/ML Models**:
  - Helmet Detection using deep learning (YOLOv5 / SSD)
  - Number Plate Detection Model
- **Backend**:
  - RTO Database Integration (API or local DB simulation)

---

## 🔧 How It Works

1. **Live Feed Processing**:
   - Captures video frames from a **traffic camera** placed at signals or intersections.

2. **Helmet Detection**:
   - Uses a trained object detection model to identify **riders without helmets** on two-wheelers.

3. **Vehicle Image Capture**:
   - Automatically captures an image of the violating vehicle at the moment of detection.

4. **Number Plate Cropping**:
   - The number plate region is extracted using contour detection or a pre-trained license plate detector.

5. **OCR Processing**:
   - Tesseract OCR is used to extract the number plate text from the cropped image.

6. **RTO Database Lookup**:
   - The extracted number is cross-verified with the **RTO database** to fetch the vehicle owner’s details.

7. **Automatic Challan Generation**:
   - If violation is confirmed, a **digital challan is raised**, and optionally, a notification is sent to the vehicle owner.

---

## 🖼 Sample Workflow

1. **Input**: Video stream from a traffic signal.
2. **Output**: Helmet violation detection, number plate cropped and recognized.
3. **Final Action**: Challan auto-generated and logged with timestamp and evidence.

---

## 📦 Folder Structure (Suggested)

```
traffic-enforcement/
├── models/                # Trained YOLO or SSD models
├── utils/                 # Image processing and OCR utilities
├── data/                  # Sample images, video frames
├── rto_database.json      # Simulated RTO data
├── main.py                # Core pipeline
├── detect_helmet.py       # Helmet violation detection logic
├── plate_reader.py        # Number plate detection + OCR
├── challan_generator.py   # Auto challan logic
└── README.md              # Project documentation
```

---

## ⚖️ Potential Impact

- 💡 Enforces helmet compliance without manual policing
- 🛡️ Enhances road safety through automation
- ⚙️ Reduces traffic personnel workload
- 🔗 Easily integrable into Smart City infrastructure

---

## 🔮 Future Enhancements

- Face recognition for pillion rider compliance
- Multi-class violation detection (triple riding, red light jumping)
- Real-time dashboard for traffic authorities
- Integration with payment gateways for online challan clearance

---

> “AI meets civic responsibility — enforcing road safety, one frame at a time.”


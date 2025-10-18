# Hand Gesture Mouse Control

This project implements a hand gesture-based mouse control system using computer vision and deep learning frameworks. The system allows controlling the mouse pointer through five different hand gestures: `fist`, `one_finger`, `open_hand`, `pinch`, and `two_fingers`.

---

## Dataset Creation

The dataset was created by capturing **videos of hand gestures** using a webcam. Each video is **1 minute long**. To extract the dataset frames:

- Use `extract_frames.py` to extract **5 frames per second** from each video.
- There are a total of **5 videos**, one for each gesture.
- **Tip:** Capturing with an IR camera could improve dataset quality and help achieve better model performance.

---

## System Workflow

1. **Webcam Detection:** The system automatically detects the connected webcam.
2. **Screen Calibration:**  
   - Run `calibration.py` to calibrate the system with the screen.  
   - This generates `calibration.json` which stores calibration data.
3. **Mouse Control:**  
   - Run `mouse_control.py` to control the mouse using hand gestures in real-time.
4. **Dataset Preparation:**  
   - Use `augment_dataset.py` to augment the dataset for better training.
5. **Model Training:**  
   - Train the gesture recognition model using `train_model.py`.

---

## Installation

Install the required dependencies using the provided `requirements.txt`:

```bash
pip install -r requirements.txt

 # 🖼️ Object Detection using Qwen3-VL Vision Model

This project implements an object detection system using the Qwen3-VL Vision-Language model. It detects objects in images, generates bounding boxes with confidence scores, and provides an interactive Gradio web interface for easy experimentation.

The model leverages Qwen3-VL-2B-Instruct to perform vision-based reasoning and returns structured JSON outputs that are parsed, validated, and visualized.

# ✨ Features

🔍 Object detection using Qwen3 Vision-Language Model

📦 Bounding box localization with confidence scores

🧠 Prompt-driven detection with strict JSON output

🎯 Optional class-based filtering

📊 Object counting by class

🖥️ Interactive Gradio UI

🛠️ Automatic bounding box normalization and correction

# 🧠 Model

Model Name: Qwen/Qwen3-VL-2B-Instruct

Type: Vision-Language Model (VLM)

Usage: Image understanding + structured object detection

Inference: Auto device mapping (GPU/CPU)

# 📦 Installation

Install the required dependencies:

pip install torch transformers pillow opencv-python supervision gradio

# 🚀 Usage

Run the application:

python app.py


Once launched:

Upload an image

(Optional) Enter object classes to filter (comma-separated, e.g. person, car)

View:

Annotated image with bounding boxes

Object counts per class

Raw JSON output from the model

# 🧾 Model Output Format

The model is prompted to return only valid JSON in the following format:

[
  {
    "label": "object_name",
    "confidence": 0.95,
    "box_2d": [x1, y1, x2, y2]
  }
]

# Notes:

Bounding boxes may be normalized, scaled, or absolute

The system automatically converts and corrects box coordinates

Invalid or hallucinated outputs are filtered out

# 🖼️ Gradio Interface

The UI includes:

Image Upload

Class Filter Input

Annotated Image Output

Object Count Summary

Raw Model JSON Output

Title shown in UI:

Qwen3-VL Object Detection (Advanced)

# 🗂️ Project Structure
├── app.py              # Main application script

├── README.md           # Project documentation

# ⚙️ How It Works

Image + prompt are sent to the Qwen3-VL model

Model generates structured JSON detections

Output is parsed and validated

Bounding boxes are normalized and auto-corrected

Results are visualized using OpenCV

Gradio displays results interactively

# ⚠️ Limitations

Detection quality depends on model reasoning

Not a traditional CNN-based detector (YOLO, Faster R-CNN)

Performance may vary on small or crowded objects


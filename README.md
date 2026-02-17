# interactive-vc-map-json-util

# 📘 Interactive VC Map JSON Utility Tool

A lightweight Python utility built with OpenCV to create interactive hotspot areas and automatically generate the corresponding JSON configuration for Interactive VC Maps.
This tool enables you to edit the existing hotspots defined and edit it accordingly. 
This tool replaces the previous two-step workflow (using external image map tools + manual JSON formatting) with a single draw-and-export process.

The main application file is:
1. map_picker.py

## 📂 Folder Structure
```
interactive-vc-map-json-util/
├── images/               # Source map images (.jpg)
├── output/               # Generated JSON files
├── map_picker.py         # Main application
├── requirements.txt      # Python dependencies
└── README.md
```

## 🚀 Setup & Usage
Setup & Installation (Ubuntu 24.04 Recommended)


1. If not already, create and activate virtual environment
```python3 -m venv venv
source venv/bin/activate
```

2. Install dependencies
```pip install opencv-python```


3. Running the Tool
```python map_picker.py```
You will be prompted for:
- Image file name (must exist in ./images/)
- Brand name (used in the generated JSON title)
---

## 🎮 Controls

Inside the OpenCV window:

Drag        → draw new rectangle (Draw mode)

d           → delete mode (click inside rectangle to delete)

m           → modify mode (click rectangle to edit title & credential)

n           → return to draw mode

u           → undo last added rectangle

s           → save JSON

q           → quit (prompts to save if changes detected)

## 🔄 Workflow Summary
1. Place your .jpg map inside /images
2. Run map_picker.py
3. Draw hotspot rectangles
4. Enter title + sample credential
    - For title, ensure you start with "DFR, DCC, DPP, DTE". For example: "DFR - Facility Record - Location M"
    - For sample credential, fill in the issued credential
5. Modify/delete if needed
6. Press s to save
7. JSON is ready for use in the Interactive VC Map

## 🎯 Why This Tool Exists

Previously:
- Use external image map generator
- Copy coordinates manually
- Manually format JSON
- Risk formatting mistakes

Now:
- Draw → Enter details → Save
- JSON generated automatically
- Faster, cleaner, and less error-prone

## 🛠 Dependencies
- Python 3.10+
- OpenCV (opencv-python)


## 📄 JSON Output

Output is automatically saved to:
```./output/<image_name>.json```

## 👩‍💻 Credits
Created by Karina Liauw, in collaboration with ChatGPT and Grok.

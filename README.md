# YOLO-LLM Image Description

## Introduction
This repository contains a Python-based pipeline that integrates YOLOv8 for object detection with a Large Language Model (LLM) for generating descriptive text of images. It is designed to first identify objects within an image using YOLOv8 and then use an LLM to create a coherent description of the scene.

## Setup Instructions

### Prerequisites
- Python 3.6 or higher.
- Access to a GPU is recommended for faster processing.

### Installation
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mikemoll84/TextOCR 
   cd YOLO-LLM Image Description
   ```

3. **Install Dependencies:**
   - Run the command: `pip install -r requirements.txt`

4. **Download Model Files:**
   - Ensure that frozen_east_text_detection.pb (EAST model) and yolov8n.pt (YOLOv8 model) are in the root directory of the project. If not included in the repository, download them from their respective sources.

## Usage
To run the image description pipeline, follow these steps:

1. **Prepare Your Image:**
   - Place the image you want to analyze in a known directory.

2. **Run the Pipeline:**
   - Use the following Python code:
    ```python
     from image_description_pipeline import ImageDescriptionPipeline

     pipeline = ImageDescriptionPipeline(east_model_path='path/to/east_model', yolo_model_path='path/to/yolo_model')
     image_path = 'path/to/your/image.jpg'
     description = pipeline.describe_image(image_path)
     print(description)
    ```

## Example Output
The output will be a descriptive text of the detected objects in the image, such as:
"The image contains a person standing near a tree, a dog to the left, and a car in the background."

## Additional Information
- **Hardware Requirements:** For optimal performance, running the models on a GPU is recommended.
- **Customization:** You can customize the pipeline by modifying the script according to your needs.

## Support
For questions or issues, please open an issue on the repository's issue tracker.

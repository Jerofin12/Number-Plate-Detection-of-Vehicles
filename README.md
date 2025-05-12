# 🚗 Indian Vehicle Number Plate Detection with EasyOCR
This repository performs automatic number plate recognition (ANPR) on images of Indian vehicles using EasyOCR. It uses a simple pipeline to detect and read license plate text from images and visually highlight the results using OpenCV.

# 📦 Features
Detects and extracts text from vehicle number plates
Uses EasyOCR for text recognition
Highlights detected license plate regions in the image
Processes multiple images from a folder
Displays annotated images directly in Google Colab

# 📁 Dataset
Ensure your dataset is structured like:

/Indian_Number_Plates/Sample_Images/
    ├── car1.jpg
    ├── car2.jpg
    └── ...
Images should clearly show the number plates of vehicles.

# 🛠️ Installation
Run the following inside a Google Colab notebook:

!pip install easyocr
Then mount your Google Drive:

from google.colab import drive
drive.mount('/content/drive')

# 📌 How It Works
Loads each image from the specified dataset folder in Google Drive.
Uses EasyOCR to detect and recognize text (typically from number plates).
Draws bounding boxes and labels for each detected text region.
Displays the annotated image using cv2_imshow.

# 🧪 Example Output

Processing car1.jpg...
Detected Text for car1.jpg: ['MH12AB1234']
And an image is displayed with bounding boxes and the detected text overlaid.

# 🧠 Code Overview

reader = easyocr.Reader(['en'])  # Initialize OCR reader
#Detects text and draws bounding boxes
def detect_number_plate(image_path):
    ...
    return annotated_image, detected_texts
#Loops through folder and applies detection
def analyze_dataset(dataset_path):
    ...
    return results_dict
# 🖼️ Visualization
Bounding boxes (green) are drawn around detected number plate regions.
Detected text (blue) is overlaid on the image using cv2.putText.

# 🗂️ File Structure

├── number plate detection.ipynb       # Main script
├── README.md                          # Project README

# 🔒 License
This project is open-source and available under the MIT License.

# 📌 Notes
Accuracy may vary based on image clarity and angle.
Best results are achieved when number plates are clearly visible and centered.
# ✅ Conclusion
This project uses EasyOCR to detect and read vehicle number plates from images in a simple and effective way. It can recognize the text on number plates and highlight it using boxes, making it easy to see the results. The system works well with clear images and is useful for basic applications like tracking vehicles or managing entries in parking areas. With some improvements, like better detection of the number plate area or checking the format of the numbers, it can become even more accurate and reliable.


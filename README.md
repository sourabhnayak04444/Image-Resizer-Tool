# Image-Resizer-Tool
# 📸 Batch Image Resizer Tool (Colab & Pillow)

A simple Python script designed to efficiently **resize and convert a batch of images** to a specific width while maintaining their aspect ratio. It's configured to run seamlessly in **Google Colaboratory**, allowing users to upload images from their local machine and download the compressed, resized results directly.

### ✨ Features

* **Batch Processing:** Resizes all `.jpg`, `.jpeg`, and `.png` images in the input directory.
* **Aspect Ratio Preservation:** Automatically calculates the new height based on the `NEW_WIDTH` to prevent distortion.
* **Conditional Resizing:** Skips resizing if an image is already smaller than the target width.
* **Format Conversion:** Converts all output images to **JPEG** format with `quality=90` for optimized file size.
* **Local I/O in Colab:** Uses `google.colab.files` to handle direct upload/download from your local PC.

### 🚀 How to Run in Google Colab

1.  **Open Google Colab:** Create a new notebook.
2.  **Install Library:** Run the following command in a code cell (Pillow is usually pre-installed):
    ```python
    !pip install Pillow
    ```
3.  **Paste and Configure:** Copy the entire `image_resizer.py` script into a new code cell. Adjust the **`NEW_WIDTH`** variable to your desired size (e.g., `NEW_WIDTH = 1200`).
4.  **Execute the Code:** Run the cell.
5.  **Upload:** A file selection window will pop up. Select all the images you wish to resize from your local machine.
6.  **Download:** After processing, a ZIP file named `resized_images_output.zip` will automatically download to your computer, containing all the resized images.

### ⚙️ Configuration (Within the Script)

The main configuration variables are at the bottom of the script:

```python
# --- Configuration using Colab's local /content directory ---
INPUT_DIR = 'input_images'   # Temporary folder for uploaded files
OUTPUT_DIR = 'output_images' # Temporary folder for resized files
NEW_WIDTH = 800              # Set your desired width in pixels (e.g., 800px)
# ---------------------

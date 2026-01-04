# ImgCap-LoRA
_LoRA Dataset Builder_



A lightweight, **Gradio-based web interface** designed to streamline the manual preparation of image datasets for LoRA (Low-Rank Adaptation) and DreamBooth training.

This tool solves the tedious task of resizing images and writing matching `.txt` caption files simultaneously, ensuring your training data is perfectly formatted for Image Diffusion trainers like Kohya_ss or OneTrainer.

## 🚀 Features

* **ZIP Upload Support:** Batch upload your raw images in a single `.zip` file.
* **Dual-Path Saving:** Automatically organizes your data into `data/images` and `data/captions` directories.
* **Intelligent Resizing:** Built-in presets for common training resolutions (512px, 768px, 1024px) using high-quality **Lanczos** or **Bicubic** interpolation.
* **Dynamic Captioning:** Automatically generates captions using a base character name and optional "add-on" tags for specific poses or backgrounds.
* **Manual Control:** Navigate through your dataset with "Next" and "Previous" buttons to ensure every image is curated specifically.

## 📖 How to Use

1. **Enter Character Name:** Input the unique trigger word/name for your LoRA (e.g., `anshu`).
2. **Upload ZIP:** Upload a zip file containing your raw `.jpg`, `.png`, or `.webp` images.
3. **Process Images:**
* Select the **Body Type** (Face, Half, Full) to append to the filename.
* Choose a **Resize Preset** to ensure uniform dimensions.
* Add **Caption Add-ons** (e.g., "sitting in a cafe, looking at camera").


4. **Save:** Click "Save Image + Caption". The tool will save the processed image and a `.txt` file with the same name into the `data/` folder.

## 📂 Project Structure

```
├── data/
│   ├── images/      # Processed & resized training images
│   └── captions/    # Matching .txt files for each image
├── temp/            # Temporary extraction folder
└── app.py           # Main Gradio application code

```

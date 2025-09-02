# CRNN OCR Pipeline in Google Colab

## 📌 Overview

This project implements an **end-to-end Optical Character Recognition (OCR) pipeline** in Google Colab. It automates the process of:

1. Converting scanned PDFs into training images.
2. Auto-generating `labels.csv` using **Tesseract OCR** (no manual labeling required).
3. Training a **Convolutional Recurrent Neural Network (CRNN)** with **CTC Loss** for sequence recognition.
4. Performing inference on new images.
5. Exporting recognized text into structured CSV output.

Everything runs in a **single Colab cell**, making the workflow reproducible and user-friendly.

---

## ⚙️ Features

* ✅ **Automatic Data Preparation** – PDF pages are converted into images, and labels are generated automatically.
* ✅ **Deep Learning Model** – CRNN with CNN + BiLSTM layers for text recognition.
* ✅ **One-Click Training** – Seamless PyTorch DataLoader and training loop.
* ✅ **Inference Ready** – Run OCR on unseen test images.
* ✅ **Result Export** – Saves recognized text into `.csv` for downstream use.

---

## 🛠 Tech Stack

* **Language:** Python
* **Frameworks/Libraries:** PyTorch, Torchvision, Pandas, Pillow
* **OCR Tool:** Tesseract OCR
* **Utilities:** pdf2image, Google Colab, Poppler
* **Environment:** Google Colab + Google Drive

---

## 📂 Project Structure

```
ocr_project/
│── scanned_input.pdf        # Input PDF file  
│── train_images/            # Auto-generated training images from PDF  
│── labels.csv               # Auto-generated text labels from Tesseract  
│── crnn_model.pth           # Saved trained CRNN model  
│── testdata.png             # Sample test image for inference  
│── testdata_table.csv       # OCR output stored in CSV  
```

---

## 🚀 How to Run

1. **Open Google Colab** and copy the notebook cell.
2. **Mount Google Drive** 
3. **Place Input PDF** in the project directory as `scanned_input.pdf`.
4. **Run All Cells** – The pipeline will:

   * Convert PDF → Images
   * Auto-generate `labels.csv`
   * Train CRNN model
   * Save model to Google Drive
5. **Inference**

   * Upload a test image (`testdata.png`).
   * Recognized text will be saved in `testdata_table.csv`.

---

## 🧠 Model Architecture (CRNN)

* **CNN Layers:** Extract visual features from images.
* **BiLSTM Layers:** Capture sequential dependencies in text.
* **CTC Loss:** Align predictions with ground truth labels.

---

## 📊 Example Output

Input:

```
(testdata.png – scanned image of text)
```

Output (saved in CSV):

```csv
recognized_text
"Hello World from OCR"
```

---

## 🔮 Future Improvements

* Add dataset augmentation (rotation, blur, noise).
* Train with multiple fonts and languages.
* Deploy as a web app for interactive OCR.

---

## 👤 Author

**Subhradeep Ghosh**
AI & ML Enthusiast | OCR & NLP Projects

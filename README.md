# Egyptian National ID Card — Data Extraction Pipeline

A pipeline that extracts structured data from Egyptian National ID cards
using two YOLOv8 models (card cropping + field detection) and PaddleOCR.

## Pipeline
1. Crop card from image (`crop_card`)
2. Detect 15 fields (front + back) (`detect_fields`)
3. Preprocess each field for OCR (`preprocess_field`)
4. Extract text with PaddleOCR (`extract_text_ordered`)
5. Build structured DataFrame

## Trained Models
Download and place in a local folder, then update the paths in the notebook:
- [Crop model (best.pt)](https://drive.google.com/file/d/1om0YoPmQwy71_4ASZTkfYyFC2-MAwxG8/view?usp=sharing)
- [Fields model (best.pt)](https://drive.google.com/file/d/1MMIkaRozhUMaIsQde_EZyg_JTzV7yK5D/view?usp=sharing)

## Training Data
- [Dataset used for training]
- [Crop model ] (https://drive.google.com/file/d/1tPS-okXA_JQ0QcTweOZLcwTrnMgxKx90/view?usp=sharing)
- [Fields model ]  ( https://drive.google.com/file/d/1yCwj3HsFZXzcPjTr7TXNJpJUMXsLRVKu/view?usp=sharing)
- Note: this dataset was sourced from the internet for educational/academic purposes and is not originally owned by this project.

## Requirements
pip install -r requirements.txt



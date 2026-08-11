# Egyptian National ID Card — Data Extraction Pipeline

A pipeline that extracts structured data from Egyptian National ID cards
using two YOLOv8 models (card cropping + field detection) and PaddleOCR.

## Pipeline
1. Crop card from image (`crop_card`)
2. Detect 15 fields (front + back) (`detect_fields`)
3. Preprocess each field for OCR (`preprocess_field`)
4. Extract text with PaddleOCR (`extract_text_ordered`)
5. Build structured DataFrame

## Notebooks

The project is split into 5 notebooks under `notebooks/`, meant to be read/run in order:

| # | Notebook | Description |
|---|---|---|
| 01 | `01_data_preparation.ipynb` | Copies datasets, fixes Roboflow `data.yaml` paths |
| 02 | `02_crop_model.ipynb` | Trains the card-cropping YOLOv8 model, `crop_card()` function |
| 03 | `03_fields_model_and_ocr_setup.ipynb` | Trains the field-detection model, sets up PaddleOCR, `detect_fields()` function |
| 04 | `04_full_pipeline_single_card.ipynb` | Full pipeline demo on one card: preprocessing + OCR + results |
| 05 | `0

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

## Note on Privacy

Some sample outputs (cropped card images, extracted personal fields) shown in
the notebooks come from a test card used for demonstration purposes only.


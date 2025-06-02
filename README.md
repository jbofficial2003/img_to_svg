# Image to SVG Converter

This script converts raster images to vector SVG format using the Potrace algorithm.

## Requirements

- Python 3.7 or higher
- Required Python packages (install using `pip install -r requirements.txt`):
  - Pillow
  - numpy
  - pypotrace

## Installation

1. Clone this repository or download the files
2. Install the required packages:
```bash
pip install -r requirements.txt
```

## Usage

Basic usage:
```bash
python image_to_svg.py input_image.png output.svg
```

Advanced usage with parameters:
```bash
python image_to_svg.py input_image.png output.svg --turdsize 2 --alphamax 1.0 --optcurve True --opttolerance 0.2
```

### Parameters

- `input`: Path to the input image file
- `output`: Path where the SVG file will be saved
- `--turdsize`: Remove speckles of up to this size (default: 2)
- `--alphamax`: Corner threshold parameter (default: 1.0)
- `--optcurve`: Optimize curves (default: True)
- `--opttolerance`: Curve optimization tolerance (default: 0.2)

## Notes

- The input image will be converted to grayscale before processing
- The quality of the SVG output depends on the input image quality and the parameters used
- For best results, use images with clear edges and good contrast 
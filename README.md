# AutoMorphoTrack

**AutoMorphoTrack** is an automated Python package for detecting, classifying, tracking, and analyzing lysosomes and mitochondria from multi-channel time-lapse microscopy images. The package produces both numerical metrics and high-quality visualizations for publication or exploratory analysis.

---

# Features

- Organelle detection using adaptive thresholding  
- Morphology classification (elongated vs. punctate) for mitochondria  
- Tracking of lysosomes and mitochondria across frames  
- Colocalization analysis between channels  
- Export of displacement, velocity, and morphology metrics  
- Publication-ready image and figure generation

---

# Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/AutoMorphoTrack.git
cd AutoMorphoTrack
pip install -r requirements.txt
```

Or install directly via:

```bash
pip install .
```

---

## Input Requirements

- Multi-frame `.tif` stack with **two channels**:
  - **Channel 0**: Lysosomes (e.g., LAMP1)
  - **Channel 1**: Mitochondria (e.g., TOM20 or mito-GFP)
- Images should be pre-aligned and background-corrected if needed.

---

# Example Usage

For a fully annotated example, see:  
`AutoMorphoTrack_Example.ipynb`

---

# Key Outputs

- **Detection overlays**: Organelles outlined over raw images  
- **Morphology overlays**: 'E' (elongated) or 'P' (punctate) labels  
- **Tracking plots**: Line or dot traces across time  
- **Colocalization map**: Cyan overlay of lysosome-mitochondria interaction  
- **CSV exports**:  
  - `lysosome_counts.csv`  
  - `morphology_counts.csv`  
  - `displacement_velocity.csv`  
  - `pearson_colocalization.csv`

---

# Customization

You can adjust:
- Detection thresholds (size, eccentricity)
- Morphology classification criteria
- Channel assignments
- Visualization styles and figure sizes

Each module (e.g., `detection.py`, `morphology.py`, `tracking.py`) can also be used independently.

---

# Project Structure

```
AutoMorphoTrack/
│
├── core.py               # Main pipeline controller
├── detection.py          # Organelle detection
├── morphology.py         # Morphology classification
├── tracking.py           # Organelle tracking
├── colocalization.py     # Colocalization metrics
├── visualization.py      # Visualization tools
├── AutoMorphoTrack_Example.ipynb   # End-to-end example
└── ...
```

---

# Applications

- Mitochondrial dynamics in neurons  
- Mitophagy and lysosomal trafficking  
- Neurodegeneration models (e.g., Parkinson's, Alzheimer's)  
- Drug screens targeting organelle function

---

# Support

For questions or contributions, please open an issue or contact the authors. Pull requests welcome!

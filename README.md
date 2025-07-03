# Spider Plot Generation for Cell Trajectory Analysis

This repository contains a Jupyter Notebook for generating customizable **spider plots** to visualize and compare **cell migration trajectories**, particularly suited for scratch-wound invasion assays.  
Statistical testing is performed on **final displacement**, not total distance traveled.

---

## Files

- `SpiderPlot.ipynb`  
  Main Jupyter Notebook for generating spider (radar) plots using `matplotlib`. Includes sample data and statistical testing code.

---

## Getting Started

### 1. Data Collection

This protocol is designed for scratch-wound invasion assays in a 96-well plate format.

- Use a 5-10 % population of fluorescently labeled cells (preferably nucleus-labeled) mixed with 90-95% parental cells.
- Grow cells to approximately 90% confluence.
- Create a scratch using the **IncuCyte WoundMaker** (Essen BioScience) or manually.
- Overlay with 10–20% Matrigel diluted in pre-cooled complete DMEM as ECM and top with treatment layer.
- Begin imaging every 2 hours for up to 72 hours in relevant fluorescence channels.

### 2. Tracking (ImageJ + TrackMate)

- Download time-lapse images as a stack.
- Open the stack in **ImageJ** and use the **TrackMate** plugin.
  - Use the **Laplacian of Gaussian (LoG)** detector.
  - Select the **LAP tracker** for linking spots.
- Focus on cells located at the leading edge of the wound area.
- Export each well’s tracking data to a `.csv` file.

---

## Plotting and Statistical Testing

### 3. Running the Notebook

- Open `SpiderPlot.ipynb` in **Jupyter Notebook** or **Google Colab**.
- Replace sample data with your own `.csv` tracking files and labels.
- Run all cells to:
  - Generate spider plots of cell trajectories.
  - Perform statistical comparison of **final displacement** values.
- Customize:
  - Axis labels
  - Color scheme
  - Title and plot limits
  - Export resolution

---

## Preview

Example output plots:

![image](https://github.com/user-attachments/assets/87105470-e81b-4833-92eb-0c6957a83263)

![image](https://github.com/user-attachments/assets/5c54b47d-9743-4489-b872-09467e1f0743)



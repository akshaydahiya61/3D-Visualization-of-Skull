# 3D-Visualization-of-Skull

# 📦 3D Volume Rendering and Gradient Visualization

Welcome to my academic project for **3D volume data visualization and gradient analysis** using pure Java. This project processes volumetric data (e.g. medical CT or MRI scans) stored in raw binary format, computes gradients, and generates 2D image projections for visual analysis.

---

## 📊 Project Overview

The application loads a volumetric dataset, computes per-voxel gradients via **central difference approximation**, and creates 2D image renderings based on **isosurface thresholds**. Users can choose the projection axis and rendering direction for flexible visual exploration of the dataset.

Key operations include:
- Reading raw 3D volume data from binary files.
- Computing the **3D gradient vector** at each voxel.
- Visualizing:
  - 2D slices of raw data.
  - 2D slices of gradient magnitudes.
  - RGB gradient images.
  - Isosurface renderings with gradient-based shading.
- Saving outputs as **TIFF images**.

---

## 📸 Example Results

- **Isosurface projections along Z-axis**
- **Gradient magnitude slices**
- **RGB gradient visualizations**

(TIFF images are generated when running the program)

---

## 🛠️ How It Works

The program performs the following steps:

1. **ReadData:** Load the raw volumetric data from a binary file (skipping the header bytes if necessary).
2. **Gradient:** Compute central difference gradients in 3D for every voxel.
3. **ExtractSlice / ExtractSliceOfGradient:** Extract 2D slices of raw data or gradients.
4. **Render:** Project isosurfaces along the specified axis based on a user-defined threshold (`isovalue`) and visualize gradient-based shading.
5. **SaveImage / SaveImageRGB:** Export images as TIFF files for visualization.

---

## ⚙️ Usage

### 📦 Compile:
```bash
javac Lab2Solution.java
----
🚀 Run:
java Lab2Solution <dimX> <dimY> <dimZ> <headerSize> <isovalue> <projectionAxis> <positiveDirection>

Example:
java Lab2Solution 256 256 225 62 95 0 true

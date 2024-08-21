# 3D Reconstruction using COLMAP and PyColmap

This project demonstrates how to perform 3D reconstruction using COLMAP and PyColmap libraries. It processes a set of images to create a 3D point cloud and textured mesh.

## Prerequisites

- Python 3.9+
- PyColmap
- NumPy
- Open3D

## Installation

1. Install the required packages:
      pip install pycolmap numpy open3d

2. Ensure COLMAP is installed on your system.

## Usage

1. Place your images in a directory (e.g., "Datasets/fountain").

2. Update the `dataset_path` variable in the script to point to your image directory.

3. Run the script:
     python colmap_3DReconstruction.py


## Features

- SIFT feature extraction
- Exhaustive feature matching
- Incremental mapping for 3D reconstruction
- Point cloud generation and visualization
- Mesh texturing (optional)

## Configuration

The script uses the following configuration:

- SIFT extraction:
  - Max features: 8192
  - First octave: -1
  - Number of octaves: 4

- Camera model: OPENCV

- Incremental mapping:
  - Number of threads: 4
  - Min inliers for initialization: 100
  - Min inliers for absolute pose: 30
  - Min inlier ratio for absolute pose: 0.25

## Output

The script generates the following outputs:

1. Reconstructed point cloud (PLY format)
2. Textured mesh (OBJ format, if texturing is enabled)
3. Visualization of the point cloud using Open3D

## Troubleshooting

If you encounter issues with file reading, ensure that:

1. The image files are in a supported format (e.g., PNG, JPG).
2. The script has read permissions for the dataset directory.
3. There are no non-image files in the dataset directory that could be mistaken for images.

## License

## Acknowledgements

This project uses the following open-source libraries:
- COLMAP
- PyColmap
- Open3D

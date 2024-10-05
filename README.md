# Variational and Bayesian Methods and Discrete Optimization (IMA203) - 2023/2024

## Course Overview

This repository contains materials and resources for the course **IMA203: Variational and Bayesian Methods and Discrete Optimization**, part of the **Image-Data-Signal** curriculum. The course focuses on advanced mathematical methods for filtering and segmenting images using variational, Bayesian, and discrete optimization techniques, with applications in digital photography, aerial imaging, and medical imaging.

### Key Topics:

- Variational Methods: Techniques for image filtering and segmentation.
- Deformable Models: Applications in various image analysis tasks.
- Bayesian Methods: Markov random fields and probabilistic models.
- Discrete Optimization: Graph cut methods for image segmentation.

## Prerequisites

Students are expected to have basic knowledge of:
- Image processing (IMA201 or equivalent)
- Mathematics (calculus, optimization)
- General programming skills

## Course Structure

- Total Hours: 24 hours
- Credits: 2.5 ECTS
- Evaluation: Written exam and practical reports.

## Instructor

- Professor Florence Tupin

## Installation and Setup

Some exercises and projects require Python and relevant image processing libraries. You can follow the instructions below to set up your environment using `conda`:

1. Anaconda/Miniconda: Download and install Python with Anaconda or Miniconda from [Conda Official Site](https://docs.conda.io/en/latest/).
2. Image Processing Libraries: Create a new conda environment with the necessary packages:
   ```bash
   conda create -n ima python matplotlib numpy scipy scikit-image ipykernel pandas scikit-learn jupyter tqdm bokeh opencv munkres
   ```
3. Activate the environment:
   ```bash
   conda activate ima
   ```

4. Launch Jupyter Notebook (if required for exercises):
   ```bash
   jupyter notebook
   ```

This will set up the necessary environment for running image processing tasks and exercises for the course.

## How to Contribute

Feel free to contribute to the repository by:
- Submitting pull requests for corrections or improvements.
- Providing additional examples or extending the projects.

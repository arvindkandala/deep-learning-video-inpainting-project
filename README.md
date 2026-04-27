# Deep Learning Video Inpainting Project

This project explores video inpainting for animated/anime-style video clips using deep learning and diffusion-based inpainting methods. The goal was to remove masked regions from video frames and generate visually coherent reconstructions while preserving the structure and style of the original video.

This was completed as a team project for our Deep Learning coursework at Duke University and received a final score of **95/100**.

## Project Overview

Video inpainting is a challenging computer vision task because the model must fill in missing regions in a way that is both visually realistic and consistent with the surrounding frames. Our project investigated how deep learning-based inpainting methods can be used to reconstruct masked regions in short video clips.

The pipeline includes:

- Loading and preprocessing short video clips
- Extracting frames from each clip
- Creating masks over regions to be inpainted
- Applying diffusion-based inpainting methods
- Reconstructing the final inpainted video
- Comparing outputs across different model settings
- Evaluating results using both qualitative inspection and quantitative metrics

## Motivation

We were interested in this project because video inpainting combines several areas of deep learning that are especially exciting:

- Computer vision
- Generative modeling
- Diffusion models
- Video understanding
- Image reconstruction
- Evaluation of generated outputs

Unlike static image inpainting, video inpainting also requires attention to consistency across time. This made the project especially interesting because strong frame-level results do not always guarantee smooth video-level outputs.

## Project Highlights

- Built an end-to-end video inpainting pipeline using Python, PyTorch, OpenCV, and Hugging Face Diffusers.
- Processed video clips into frames, applied masks, generated inpainted frames, and reconstructed output videos.
- Experimented with diffusion-based inpainting pipelines and guidance-scale settings.
- Compared baseline outputs against multiple model configurations.
- Explored VAE-based reconstruction as an additional generative modeling experiment.
- Evaluated outputs using image/video quality metrics and qualitative visual inspection.
- Improved results through iterative experimentation, debugging, and pipeline refinement.
- Final project score: **95/100**.

## Tech Stack

- Python
- PyTorch
- Hugging Face Diffusers
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## Deep Learning Concepts Used

This project involved several core deep learning and computer vision concepts:

- Diffusion-based generation
- Image and video inpainting
- Masked reconstruction
- Frame extraction and video reconstruction
- Latent-space representations
- Guidance-scale tuning
- Qualitative and quantitative model evaluation
- Tradeoffs between compute cost, runtime, and output quality

## Pipeline

The general workflow for the project was:

1. **Load video clips**

   Short animated/anime-style clips were loaded and prepared for processing.

2. **Extract frames**

   Each video was broken into individual frames so that image-level inpainting could be applied.

3. **Generate masks**

   Masks were created to define which parts of each frame should be reconstructed.

4. **Run inpainting model**

   A diffusion-based inpainting pipeline was used to generate missing content for the masked regions.

5. **Reconstruct video**

   The inpainted frames were stitched back together into a final output video.

6. **Evaluate results**

   Outputs were evaluated using a combination of visual inspection and quantitative metrics.

## Experiments

The project included several experiments to understand how different settings affected output quality.

### Baseline Inpainting

A baseline inpainting output was generated to establish a starting point for comparison.

### Guidance Scale Experiments

Different guidance-scale settings were tested to evaluate how strongly the model should follow the prompt and conditioning information.

### VAE-Based Reconstruction

A VAE-based experiment was also tested as an additional generative modeling approach. This helped compare a simpler reconstruction-based method against the diffusion-based inpainting pipeline.

### Qualitative Evaluation

Since video inpainting quality can be difficult to capture through metrics alone, outputs were also evaluated visually. Important factors included:

- Whether the masked region was filled plausibly
- Whether the output matched the surrounding frame
- Whether the reconstructed frames were visually coherent
- Whether the final video looked smooth enough across time

## Results

The final diffusion-based inpainting pipeline produced stronger and more visually coherent results than the baseline and VAE-based experiments. The best outputs were selected based on both quantitative metrics and visual quality.

The project received a final score of **95/100**.

## Key Challenges

Some of the main challenges in this project included:

- Managing video data and frame-level preprocessing
- Handling compute constraints while experimenting with deep learning models
- Debugging environment and dependency issues
- Preserving output quality while keeping the pipeline efficient
- Understanding the difference between strong image-level outputs and consistent video-level outputs
- Evaluating generative model outputs beyond simple numerical metrics

## What We Learned

Through this project, we gained hands-on experience with the full deep learning experimentation workflow, including:

- Working with diffusion-based inpainting models
- Building a computer vision pipeline from preprocessing to final output
- Debugging model and environment issues under compute constraints
- Comparing different generative modeling approaches
- Evaluating generated outputs both quantitatively and qualitatively
- Iterating on model settings to improve final results

This project strengthened our understanding of deep learning for computer vision, especially in generative AI and video reconstruction.

## Relevance to AI Research

This project is closely connected to broader AI research because it required both practical implementation and experimental thinking. We worked through model limitations, evaluation challenges, and tradeoffs between quality and compute cost.

The project also helped us better understand how generative models can be applied to real-world visual reconstruction tasks, which connects to broader research areas such as computer vision, multimodal AI, and responsible model evaluation.

## Repository Structure

```text
.
├── notebooks/
│   └── video_inpainting_project.ipynb
├── outputs/
│   ├── sample_frames/
│   ├── inpainted_frames/
│   └── final_videos/
├── data/
│   └── sample_clips/
├── README.md
└── requirements.txt
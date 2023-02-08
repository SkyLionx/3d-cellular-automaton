# 🐠 3D Growing Neural Cellular Automaton

This project is based on the work of <a href="https://distill.pub/2020/growing-ca" target="_blank">Mordvintsev, et al. (2020)</a>, which proposes a method to model the **morphogenesis** process using a **Neural Cellular Automaton** in order to reconstruct 2D images.

Morphogenesis is the biological process that allows cells to **develop and persist** their shape. Starting from a simple initial form, cells grow to construct a more complex one defining connections among them.

In the original work, from a simple image with only one pixel, called **seed**, a full target image is regenerated based on the training data. This is modeled using a Cellular Automaton which during its training learns an **update rule** which is used by each cell to update its state and eventually reconstruct the final target shape.

In this project, a deep model is implemented in order to replicate the morphogenesis process on a **3-dimensional Euclidean space** using voxels, as we can see from the examples below.

<br/>

<div align="center">
  <video src="https://user-images.githubusercontent.com/58000595/217600398-4ff8cc6f-8a18-4be3-b065-753a8e8493c1.mp4">
</div>

<br/>

![image info](splash-steps.png)

## Contributors

<a href="https://github.com/SkyLionx" target="_blank">
  <img src="https://img.shields.io/badge/Profile-Fabrizio%20Rossi-green?style=for-the-badge&logo=github&labelColor=blue&color=white">
</a>
<br /><br />
<a href="https://github.com/dotmat3" target="_blank">
  <img src="https://img.shields.io/badge/Profile-Matteo%20Orsini-green?style=for-the-badge&logo=github&labelColor=blue&color=white">
</a>

## Repository content
The `deep_learning_project.ipynb` contains the Colab notebook used to develop the project, so it is better viewed directly on the Colab platform:

<a href="https://colab.research.google.com/github/SkyLionx/DL2021/blob/master/deep_learning_project.ipynb" target="_blank">
<img src="https://img.shields.io/badge/Colab-Open%20Notebook-green?style=for-the-badge&logo=googlecolab&color=blue">
</a>
<br/>
<br/>

Inside the `shapes` folder, we uploaded the 3D voxel models we created which were used as training data. They are saved in the proprietary `.vox` format used by the [Voxelator editor](http://voxelator.com/).

Instead, in the `videos` folder we have all the videos that we produced using the pretrained models contained in the notebook. <br>
For each shape there are three videos with different suffixes:
- `_normal` videos are used to demostrate the persisting capabilities of the model;
- `_damage` videos are produced using a damaged shape as input;
- `_rotate` videos are produced giving as input an angle for the x-axis of 90 degrees.

Finally, the file `damage_visualization.pdf` shows how our damage affects the splash model in 36 different cases, and it is a tool we used in order to assess how good our damage algorithm performed.

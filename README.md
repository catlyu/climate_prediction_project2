# climate_prediction_project2

This repository contains Group 4's Project 2, focused on vertical mixing shape profile prediction using ocean surface boundary layer information. Our group was interested in two tasks:
1) Learn more about the distribution of input features. We are interested in better understand how different quantities of the input features (like latitude and boundary layer depth) correlate with the shape function across the depth of the profile.
2) Try different model architectures based on what we learned. We tried a number of different machine learning algorithms including: macro + refine, parameter shape, and XGBoost. These profiles allow for more customized learning of different shape functions.

This repo contains a number of notebooks with many things we explored while working on this project. The notebook `data_story.ipynb` is self-contained and holds all the material we expect to be reviewed/graded.

Contribution statement:
CL, PB, BH, and AMF collaboratively designed the study. AMF drafted the outline of the data story and all team members added results from their section. AMF examined the correlation between four input features and the output shape profile based on different boundary layer depth intervals. PB examined the correlation between four input features and the output shape profile based on the latitude differences (tropical and non-tropical). CL designed and implemented two level-by-level architectures (macro+refine model & parameter shape model) to improve performance in shape function prediction tasks. BH designed and compared neural network and XGBoost models, evaluating five input combinations.found that removing h0​ improved neural network performance but hurt XGBoost accuracy. BH implemented an XGBoost-to-PyTorch wrapper for unified evaluation, and showed that NN generalizes better while XGBoost depends heavily on h0​.*Make sure to add what you worked on here :)* 

# climate_prediction_project2

This repository contains Group 4's Project 2, focused on vertical mixing shape profile prediction using ocean surface boundary layer information. More specifically, we plan on focusing on the below tasks:

1. **Expanding the inputs**  
Sane et al provide four inputs to the algorithm including two variables based on position (f, h) and two variables at the surface (b0, u*) and the model must then learn a relationship across 16 depth points. We’re interested in providing some information about variables at depth either using statistical quantities (mean, st deviation) or dimensional reduction (PCA).
2. **Expanding the inputs**  
Studying feature importance: we’d like to understand which variables are most influential in producing the output. There are a few ways to accomplish this including SHAP (Shapley Additive Explanations) for the whole output and LRP (Layer-wise Relevance Propagation) for individual layers and individual neurons. This would also provide a way to evaluate the “usefulness” of adding inputs in step 1.
3. **Two-level NN prediction**
The reasoning behind this method is that we are using a small number of inputs to predict a big number of outputs, so taking steps could ease the model tasks and improve performance. 
- One way to do this is to use the network to predict the rough shape - relative positions of node 1 through node 16 - of the outputs, then feed in additional data to fine tune the 16 outputs
- Another idea is to group the desired outputs into macro levels (for example, four groups of four grouped by their depths), so the model can predict the macro level information before predicting the finer precise outputs. 
4. **Model spread**
We’d like to estimate model spread or prediction uncertainty. One way to do this would be to train multiple models that have the same architecture using different parts of the training dataset. Then comparing the spread of outputs between different models could provide some kind of estimate of how “reliable” the results are.

# XML-Final-Project: Exploring XAI methods for Image Classifiers
Our project aims to quantify the inherently subjective concept of ranking two explainable machine learning (XML) methods on image classification predictions. We qualitatively and quantitatively evaluate explanations given by GradCAM and SHAP on results from VGG-16, ResNet-50, and DenseNet-121 image classification models using the ImageNet50 dataset. The quantitative analysis involved measuring % increase and drop in confidence of predictions when the model is given an image perturbed using direct occlusion or ROAD based on the original explanations. We also explored using an object-localization metric- intersection over union (IoU) by comparing explanations with ground-truth masks that we manually annotated. Overall, we found that GradCAM outperforms SHAP for image classifier explanations. Further, GradCAM explanations for DenseNet-121 showed the best results across XML methods and other models.

## To Reproduce our Results
Download the dataset folder and change all ``path`` variables accordingly. As our method is focused on generating image explanations, we used Google Colab for convenience. For queries related to ground truth masks, GradCAM, and quantitative evaluation feel free to tag @ananya314 in the issues.

## References
1. https://lime.readthedocs.io/en/latest/
2. https://shap.readthedocs.io/en/latest/index.html
3. https://medium.com/@stepanulyanin/implementing-grad-cam-in-pytorch-ea0937c31e82
4. https://colab.research.google.com/drive/1FXgkHZy4rVIURSECRIQtRPhtndvBKYYm?usp=sharing
5. ``pytorch-gradcam`` https://github.com/jacobgil/pytorch-grad-cam (a compilation of various CAM-based image explanation techniques, we used only the ROAD metric in this project)
6. GradCAM++ metrics https://arxiv.org/abs/1710.11063
7. Relevant surveys and resources that also describe evaluation metrics: 
    * Akhtar N. A Survey of Explainable AI in Deep Visual Modeling: Methods and Metrics. (2023) https://arxiv.org/pdf/2301.13445.pdf 
    * Li X, Xiong H, Li X, Wu X, Zhang X, Liu J, Bian J, Dou D. Interpretable deep learning: Interpretation, interpretability, trustworthiness, and beyond. Knowledge and Information Systems. Knowl Inf Syst 64, 3197–3234 (2022) https://doi.org/10.1007/s10115-022-01756-8 
    * https://github.com/utkuozbulak/pytorch-cnn-visualizations
    * Bommer P, Kretschmer M, Hedström A, Bareeva D, Höhne MM. Finding the right XAI method--A Guide for the Evaluation and Ranking of Explainable AI Methods in Climate Science. (2023) https://arxiv.org/pdf/2303.00652.pdf

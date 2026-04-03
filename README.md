# MHPE

MHPE: Learning Morphology Relationships for Robust Head Pose Estimation with Facial Rotation Representation

## :book: Abstract
Although accurate head pose estimation is critical for natural human–computer interaction, it remains challenging due to occlusion, extreme poses, illumination conditions, and data ambiguity issues. To address these challenges, a novel morphology aware Transformer framework (MHPE) is proposed, which can learn morphological relationships during facial rotation. The methodology is based on two key findings: cross-region geometric dependencies and angle-specific morphodynamic representations. The proposed framework incorporates two key components: adversarial feature generation, which generates robust rotation representations by adaptive multi-scale feature interaction; and morphology relationship inference, which establishes long-range dependencies between facial features through a cross-modal attention mechanism that incorporates morphological priors. Extensive evaluations on three demanding benchmarks (BIWI, AFLW2000, and 300W-LP) demonstrate state-of-the-art performance, particularly in demanding scenarios.

## :rocket: Overview
Figure 1 shows the overall architecture of the proposed MHPE model, which consists of two key components: 1) the AFG module and 2) the MRI module. The MRI module implements three processing stages: visual token representation, morphology token construction, and cross-region attention modeling. The AFG module first performs an adaptive interaction of the multi-view head images sampled from the input batch, generating augmented training samples. These samples undergo biomechanically constrained feature integration, where view-specific, shared, and composite features are combined using learnable spatial weighting. Subsequently, the MRI module establishes long-range dependencies between facial features through a cross-modal attention mechanism incorporating morphology morphological priors. Our architecture achieves dynamic feature enhancement based on head rotation, morphology-consistent spatial relationship modeling, and robust pose estimation under varying viewing conditions. Our framework significantly improves the accuracy of pose estimation while maintaining computational efficiency, especially in challenging situations involving extreme poses or partial occlusions.

<img src="https://raw.githubusercontent.com/Qshijia/MHPE/main/Figure1.png" width="500">

##### Fig. 1. Overview of our proposed MHPE model that consists of two modules: AFG and MRI. The MRI module implements three processing stages: visual token representation, morphology token construction, and cross-region attention modeling.

## :sparkles: Contributions
1. We developed a novel morphology aware Transformer framework (MHPE), which can accurately infer head posture by learning the morphology relationships of facial regions during head rotation. To the best of our knowledge, this is the first work to incorporate morphological relationships into HPE.
2. The AFG module generates robust rotation representations by adaptive multi-scale feature interaction. By mining the common features of images and filtering redundant information, the generalization ability of the model can be effectively improved. Meanwhile, the MRI module establishes long-range dependencies between facial features through a cross-modal attention mechanism that incorporates morphological priors.
3. Comprehensive evaluations demonstrate the superiority of MHPE over existing methods on three benchmark datasets: BIWI, AFLW2000, and 300W-LP. Our approach introduces a new state-of-the-art performance in extracting morphology correlation features, particularly for large-angle pose estimation.

## :file_cabinet: Datasets

AFLW2000 represents a renamed portion of the AFLW dataset, specifically comprising the first 2000 images. This dataset furnishes precise 3D facial ground truth data alongside their respective 68 landmark points. A number of the head pose images within this particular dataset present significant challenges due to substantial variations in body positioning, facial expressions, and lighting conditions, offering valuable testing opportunities for researchers.

300W-LP is a synthetically generated dataset based on the expanded 300W data. This comprehensive resource incorporates elements from various datasets, such as AFW, HELEN, IBUG, and LFPW. The 300W-LP dataset creates roughly 61,225 distinct samples featuring prominent head poses through facial profiling. Furthermore, image mirroring doubles this collection to 122,450 composite examples, offering a wide
array of diverse poses. This dataset is widely utilized as a foundational training set for tasks involving HPE.

BIWI dataset captured with a Kinect camera, consists of 24 separate video sequences featuring 20 individuals. Four of these recordings were duplicated, bringing the total image count to 15,678 frames. This dataset effectively demonstrates a wide spectrum of pitch, yaw, and roll angle changes. Considering that the head occupies only a small area within many of its images, the multitask CNN (MTCNN) is typically used to detect and crop the head region, generating the relevant face bounding box.

## :bulb: Citation

```python

@ARTICLE{11329052,
  author={Liu, Tingting and Ju, Jianping and Song, Zhixiong and Qian, Shijia and Rao, Ning and Liu, Hai and Li, You-Fu},
  journal={IEEE Transactions on Circuits and Systems for Video Technology}, 
  title={MHPE: Learning Morphology Relationships for Robust Head Pose Estimation with Facial Rotation Representation}, 
  year={2026},
  volume={},
  number={},
  pages={1-1},
  keywords={Head;Morphology;Pose estimation;Facial features;Accuracy;Nose;Magnetic resonance imaging;Feature extraction;Current transformers;Correlation;Morphology-aware;Transformer;Morphology representation learning;Geometric dependencies;Head pose estimation},
  doi={10.1109/TCSVT.2026.3651198}}


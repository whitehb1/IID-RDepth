#  Monocular Depth Estimation From the Perspective of Feature Restoration: A Diffusion Enhanced Depth Restoration Approach


[**Paper**](paper-link) | [**Code**](https://github.com/whitehb1/IID-RDepth)

Official implementation of Monocular Depth Estimation From the Perspective of Feature Restoration: A Diffusion Enhanced Depth Restoration Approach

[Huibin Bai](https://github.com/whitehb1), Shuai Li, Hanxiao Zhai, Yanbo Gao, Chong Lv, Yibo Wang, Haipeng Ping, Wei Hua, Xingyu Gao

<p align="center">All Code will be released soon... 🏗️ 🚧 🔨</p>


Abstract: *Monocular Depth Estimation (MDE) is a fundamental computer vision task with important applications in 3D vision. The current mainstream MDE methods adopt an encoder-decoder architecture with multi-level/scale feature processing. However, the limit of the current architecture and effects of different-level features on the prediction accuracy are not evaluated. In this paper, we first investigate the above problem and show that there is still substantial potential in the current framework if the encoder features can be improved. Therefore, we propose to formulate the depth estimation problem from the feature restoration perspective, by treating pretrained encoder features as degraded features of an assumed ground truth feature that yields the ground truth depth map. Then an Invertible transform enhanced Indirect Diffusion (InvT-IndDiffusion) module is developed for the feature restoration. Because of lacking a direct supervision on the feature, only indirect supervision from the final sparse depth map is used. Under the iterative procedure of diffusion, this results in feature deviations among steps. The proposed InvT-IndDiffusion solves this problem by using an invertible transform based decoder under bi-Lipschitz condition. Finally, a plug-and-play Auxiliary Viewpoint based Low-level Feature Enhancement module (AV-LFE) is developed to enhance local details with auxiliary viewpoint when available. Experiments demonstrate that the proposed method achieves better performance than the state-of-the-art methods on various datasets., Specifically on the KITTI benchmark, compared with the baseline, the performance is improved by 4.09\% and 37.77\% under different training settings,  in terms of RMSE.*

<p align="center">
    <img src="error_map.png">
</p>


## Method

Overview of the proposed IID-RDepth. The input image is first processed through a frozen encoder to extract the multi-level features. Then the
high-level semantic features are combined as mutual conditional maps and fed into the InvT-IndDiffusion for restoration. For low-level detail features, AV-LFE
is used as a plug-and-play module to enhance the identity connection when auxiliary viewpoint is available.
<p align="center">
    <img src="method.png">
</p>


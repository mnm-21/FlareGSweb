# 🌟 FlareGS: 4D Flare Removal using Gaussian Splatting for Urban Scenes

**Authors:** Mayank Chandak, Sai Sri Teja Kuppa, Rahul, Gopi Raju Matta, Vinayak Gupta, Kaushik Mitra

[![Paper](https://img.shields.io/badge/Paper-ICCV%202025-blue)](https://openaccess.thecvf.com/ICCV2025)
[![arXiv](https://img.shields.io/badge/arXiv-coming%20soon-orange)](https://arxiv.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<img src="ICCV2025-Author-Kit-Feb/images/abstract_new.png" width="800px" alt="FlareGS Teaser">
<p><em>Our approach addresses 4D flare removal by utilizing multi-view information through Gaussian splatting. We present a pipeline for recovering flare-free novel views from flare-corrupted multi-view videos, enabling improved performance on downstream tasks.</em></p>
<p><strong>Key Insights:</strong> The teaser demonstrates our novel 4D flare removal pipeline that leverages multi-view consistency through Gaussian splatting. By aggregating information from spatially and temporally adjacent views, our method achieves photometrically and geometrically consistent reconstructions. This enables robust flare removal while preserving scene structure and improving downstream perception tasks.</p>

## 📖 Abstract

Flare artifacts such as halos, ghosting, and internal reflections often degrade visual quality in autonomous driving scenarios, particularly under adverse weather conditions like rain, fog, or rapid pressure shifts across windshields. These flares, arising from water droplets, condensation, or internal glass reflections, are fundamentally distinct from conventional lens flares and remain largely unaddressed in prior literature.

In this work, we present the first systematic effort to model and remove such reflective flares that appear in real-world driving videos. Our method leverages multi-view consistency through Gaussian Splatting-based novel view synthesis, achieving more photometrically and geometrically consistent reconstructions compared to single-view approaches.

## 🎯 Key Contributions

- **🌊 Physics-based Synthetic Pipeline**: We introduce a controlled synthetic dataset that simulates flare formation using physics-informed rendering
- **🔍 Depth-guided Uformer Architecture**: A multi-modal restoration framework that fuses flare-degraded RGB inputs with flare-invariant depth priors
- **🎨 Gaussian Splatting Framework**: Novel view synthesis that enhances multi-view consistency and facilitates accurate reconstruction of flare-free scenes
- **📊 Comprehensive Evaluation**: Significant improvements in both visual fidelity and downstream tasks (segmentation, optical flow) under adverse weather conditions

## 🏗️ Method Overview

<img src="ICCV2025-Author-Kit-Feb/images/splatformer_diagram.png" width="600px" alt="Method Architecture">
<p><em>Our depth-guided Uformer architecture leverages depth information to better disentangle flare artifacts from scene content.</em></p>
<p><strong>Key Insights:</strong> Our multi-modal architecture fuses flare-corrupted RGB inputs with flare-invariant depth priors from LiDAR sensors. The depth information serves as a reliable structural prior since it remains unaffected by optical flare artifacts. This enables precise localization of flare-affected regions and more accurate restoration compared to RGB-only approaches.</p>

## 🎨 Qualitative Results

<img src="ICCV2025-Author-Kit-Feb/images/Qualitative_results.png" width="800px" alt="Qualitative Results">
<p><em>Visual comparison of flare removal results across different methods and scenarios.</em></p>
<p><strong>Key Insights:</strong> Our method demonstrates superior flare removal capabilities across diverse weather conditions including rain, fog, and varying lighting scenarios. The results show effective suppression of reflective flares, ghosting artifacts, and halo patterns while preserving fine scene details. Compared to baseline methods, our approach maintains better color consistency and structural integrity in the restored images.</p>

## 📊 Model Comparison

<img src="ICCV2025-Author-Kit-Feb/images/ModelComparision.png" width="800px" alt="Model Comparison">
<p><em>Quantitative comparison with state-of-the-art methods on flare removal and downstream tasks.</em></p>
<p><strong>Key Insights:</strong> Quantitative evaluation shows our method achieves significant improvements in PSNR, SSIM, and LPIPS metrics compared to existing flare removal approaches. The depth-guided architecture provides consistent performance gains across different flare intensities and weather conditions. Our approach also demonstrates better generalization to unseen scenarios, making it more practical for real-world autonomous driving applications.</p>

## 🔬 Ablation Studies

<img src="ICCV2025-Author-Kit-Feb/images/abalation.png" width="600px" alt="Ablation Study 1">
<p><em>Ablation study demonstrating the effectiveness of different components in our framework.</em></p>
<p><strong>Key Insights:</strong> The first ablation study validates the importance of each component in our pipeline, showing that depth guidance provides the most significant improvement in flare removal accuracy. The Uformer backbone combined with depth priors achieves better artifact suppression than traditional CNN architectures. Multi-view consistency further enhances the quality by leveraging temporal information from adjacent frames.</p>

<img src="ICCV2025-Author-Kit-Feb/images/abalation2.png" width="600px" alt="Ablation Study 2">
<p><em>Additional ablation results showing the impact of depth guidance and multi-view synthesis.</em></p>
<p><strong>Key Insights:</strong> The second ablation study demonstrates the synergistic effect of combining depth guidance with Gaussian splatting-based view synthesis. Depth information alone improves flare localization, while multi-view synthesis enhances photometric consistency across different viewpoints. The combination achieves optimal results by leveraging both spatial structure from depth and temporal consistency from multiple views.</p>

## 🎯 Downstream Task Performance

<img src="ICCV2025-Author-Kit-Feb/images/segmentation.png" width="700px" alt="Segmentation Results">
<p><em>Improved semantic segmentation performance after flare removal using our method.</em></p>
<p><strong>Key Insights:</strong> Flare removal significantly improves the performance of downstream perception tasks, with semantic segmentation accuracy increasing by 15-20% on flare-corrupted images. The improved segmentation results demonstrate that our method preserves important scene semantics while removing artifacts. This validates the practical impact of flare removal for autonomous driving applications where accurate scene understanding is critical.</p>

## 🎭 Synthetic Dataset

<img src="ICCV2025-Author-Kit-Feb/images/synthetic_dataset.png" width="700px" alt="Synthetic Dataset">
<p><em>Our physics-based synthetic dataset generation pipeline for realistic flare simulation.</em></p>
<p><strong>Key Insights:</strong> Our physics-informed synthetic dataset generation pipeline creates realistic flare artifacts by modeling light interaction with water droplets, condensation, and glass surfaces. The synthetic data closely matches real-world flare patterns observed in autonomous driving scenarios, enabling effective model training without extensive manual annotation. This approach provides a scalable solution for generating diverse flare-corrupted training data.</p>

## 🚗 Real-world Driving Scenarios

<img src="ICCV2025-Author-Kit-Feb/images/differentids_output.png" width="700px" alt="Real-world Results">
<p><em>Flare removal results on real-world driving scenarios with various weather conditions.</em></p>
<p><strong>Key Insights:</strong> Real-world evaluation demonstrates robust performance across diverse driving scenarios including urban environments, highways, and adverse weather conditions. Our method effectively handles various flare types including reflective flares from streetlights, scattering flares from rain, and halo patterns from fog. The results show consistent flare suppression while maintaining scene fidelity, making it suitable for deployment in autonomous driving systems.</p>

## 📚 Citation

If you find this work useful for your research, please cite our paper:

```bibtex
@inproceedings{flaregs2025,
  title={FlareGS: 4D Flare Removal using Gaussian Splatting for Urban Scenes},
  author={Mayank Chandak and Sai Sri Teja Kuppa and Rahul and Gopi Raju Matta and Vinayak Gupta and Kaushik Mitra},
  booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
  year={2025}
}
```

## 🤝 Acknowledgments

We thank the ICCV 2025 reviewers for their valuable feedback. This work was supported by [Institution Names].

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p><strong>🌟 Star this repository if you find it helpful!</strong></p>
<p>For questions and discussions, please open an issue or contact the authors.</p> 
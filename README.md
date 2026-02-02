# OpenVLA

---
## OpenVLA: An Open-Source Vision-Language-Action Model
* https://github.com/openvla/openvla
 

A simple and scalable codebase for training and fine-tuning vision-language-action models (VLAs) for generalist robotic manipulation:

* Different Dataset Mixtures: We natively support arbitrary datasets in RLDS format, including arbitrary mixtures of data from the Open X-Embodiment Dataset.
* Easy Scaling: Powered by PyTorch FSDP and Flash-Attention, we can quickly and efficiently train models from 1B - 34B parameters, with easily adaptable model architectures.
* Native Fine-Tuning Support: Built-in support (with examples) for various forms of fine-tuning (full, partial, LoRA).

Built on top of Prismatic VLMs.

---
## Prismatic VLMs
https://github.com/TRI-ML/prismatic-vlms

A flexible and efficient codebase for training visually-conditioned language-models (VLMs):

* Different Visual Representations. We natively support backbones such as CLIP, SigLIP, DINOv2 – and even fusions of different backbones. Adding new backbones is easy via TIMM.
* Base and Instruct-Tuned Language Models. We support arbitrary instances of AutoModelForCausalLM including both base and instruct-tuned models (with built-in prompt handling) via Transformers. If your favorite LM isn't already supported, feel free to submit a PR!
* Easy Scaling. Powered by PyTorch FSDP and Flash-Attention, we can quickly and efficiently train models from 1B - 34B parameters, on different, easily configurable dataset mixtures.
 

---
## Open X-Embodiment Dataset
https://robotics-transformer-x.github.io/

Large, high-capacity models trained on diverse datasets have shown remarkable successes on efficiently tackling downstream applications. In domains from NLP to Computer Vision, this has led to a consolidation of pretrained models, with general pretrained backbones serving as a starting point for many applications. Can such a consolidation happen in robotics? Conventionally, robotic learning methods train a separate model for every application, every robot, and even every environment. Can we instead train “generalist” X-robot policy that can be adapted efficiently to new robots, tasks, and environments? In this paper, we provide datasets in standardized data formats and models to make it possible to explore this possibility in the context of robotic manipulation, alongside experimental results that provide an example of effective X-robot policies. We assemble a dataset from 22 different robots collected through a collaboration between 21 institutions, demonstrating 527 skills (160266 tasks). We show that a high-capacity model trained on this data, which we call RT-X, exhibits positive transfer and improves the capabilities of multiple robots by leveraging experience from other platforms.

---
<img width="1200" height="214" alt="image" src="https://github.com/user-attachments/assets/9569e2b5-4e1f-4cec-9336-f53267226558" />


---
## Optimized Fine-Tuning (OFT) recipe for VLAs

* Fine-Tuning Vision-Language-Action Models: Optimizing Speed and Success
  * https://openvla-oft.github.io/
* Our new Optimized Fine-Tuning (OFT) recipe for VLAs — which combines parallel decoding, action chunking, a continuous action representation, and L1 regression objective — significantly enhances inference speed (25-50x) and task performance (20%+ boost in success rate).
* OpenVLA-OFT, a policy created with our fine-tuning recipe, achieves SOTA results in LIBERO: 97.1% average success rate across 4 task suites, outperforming π0, MDT, Seer, DiT Policy, Octo, and Diffusion Policy.
* Our recipe, when augmented with FiLM for better language grounding ("OFT+"), enables high-frequency language-driven control on the bimanual ALOHA robot with a 7B-parameter VLA policy and outperforms other fine-tuned VLAs (π0 and RDT-1B) and popular imitation learning policies trained from scratch (ACT and Diffusion Policy).

---
## AutoFly: Vision-Language-Action Model for UAV Autonomous Navigation in the Wild

* https://openreview.net/forum?id=88RKxlFUNY
* ICLR 2026

Vision-language navigation (VLN) requires intelligent agents to navigate environments by interpreting linguistic instructions alongside visual observations, serving as a cornerstone task in Embodied AI. Current VLN research for unmanned aerial vehicles (UAVs) relies on detailed, pre-specified instructions to guide the UAV along predetermined routes. However, real-world outdoor exploration typically occurs in unknown environments where detailed navigation instructions are unavailable. Instead, only coarse-grained positional or directional guidance can be provided, requiring UAVs to autonomously navigate through continuous planning and obstacle avoidance. To bridge this gap, we propose AutoFly, an end-to-end Vision-Language-Action (VLA) model for autonomous UAV navigation. AutoFly incorporates a pseudo-depth encoder that derives depth-aware features from RGB inputs to enhance spatial reasoning, coupled with a progressive two-stage training strategy that effectively aligns visual, depth, and linguistic representations with action policies. Moreover, existing VLN datasets have fundamental limitations for real-world autonomous navigation, stemming from their heavy reliance on explicit instruction-following over autonomous decision-making and insufficient real-world data. To address these issues, we construct a novel autonomous navigation dataset that shifts the paradigm from instruction-following to autonomous behavior modeling through: (1) trajectory collection emphasizing continuous obstacle avoidance, autonomous planning, and recognition workflows; (2) comprehensive real-world data integration. Experimental results demonstrate that AutoFly achieves a 3.9% higher success rate compared to state-of-the-art VLA baselines, with consistent performance across simulated and real environments.


---
## News

*「最強具身VLA大模型」，究竟強在哪兒？ (2025-11)
 * https://bangqu.com/oYj2N5.html?fbclid=IwY2xjawOQpXBleHRuA2FlbQIxMQBzcnRjBmFwcF9pZBAyMjIwMzkxNzg4MjAwODkyAAEek9Jt0G-fzZg-5lTNd5ZKsJBVJ5kvmkDXiYebvnCcanV5pG_IvN_hUDFHiDs_aem_9O0kjnNAjcOp-D93gaDlnw

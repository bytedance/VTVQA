<big>ViteVQA</big>
--------------------------------------------------------------------------------

Towards Video Text Visual Question Answering: Benchmark and Baseline [[Paper](https://openreview.net/pdf?id=yPZ7w29qSNK)] Accepted by NeurIPS 2022.
<h3>Describition</h3>

A novel task named  <i> <b>Vi</b>deo <b>Te</b>xt <b>V</b>isual <b>Q</b>uestion <b>A</b>nswering </i>  (<b>ViteVQA</b> in short), which aims at answering questions by jointly reasoning textual and visual information in a given video.

The first ViteVQA benchmark dataset, which is named <i> <b>M</b>ulti-category <b>M</b>ulti-frame <b>M</b>ulti-resolution <b>M</b>ulti-modal </i> benchmark for ViteVQA (<b>M4-ViteVQA</b> in short).

<img src="https://github.com/bytedance/VTVQA/blob/master/Imgs/Fig-Intro.png" width="100%" class="aligncenter">
<small> Some examples from our M4-ViteVQA dataset. ‘A’ indicates the answers returned by TextVQA models and wrong answers are colored in red. Leveraging temporal, textual, and visual information in the video
is the only way to correctly answer the question.</small>

**Major features for ViteVQA:**
-  **Challenging**: It must jointly exploit both textual and visual information as well as temporal logic among video frames or events.
-  **General**: As an extension to the TextVQA task, it is more general and has wider applications since it can answer temporal-related questions as well as handle video streams.


**Major features for M4-ViteVQA:**
-  **Multi-category**: M4-ViteVQA consists of 7,620 video clips of nine categories (i.e., <i>shopping</i>, <i>traveling</i>, <i>driving</i>, <i>vlog</i>, <i>sport</i>, <i>advertisement</i>, <i>movie</i>, <i>game</i> and <i>talking</i>).
-  **Multi-resolution**: M4-ViteVQA has three kinds of resolutions (i.e., 720p, 1080p and 1176X664)
-  **Dataset size**: 7,620 video clips; 25,123 question-answer pairs; 1,317,392 frames; 500GB storage cost
-  **Three settings**: Two generic QA settings and one domain adaption setting to deal with unlearned content and completely different category-specific questions

<h3>Tasks and Metrics</h3>


We define 2 tasks with 3 settings for the ViteVQA problem, namely <i>regular QA task</i> (Task1) and <i>domain adaption task</i> (Task2).

In Task1, the model is trained and tested on all the nine categories of M4-ViteVQA, which is a regular setting. In order to meet the different requirements for the robustness of the model, we consider two data splits for Task1. The first one is called <b>Task1Split1</b> that is divided according to the 7,620 cropped videos, the second one is called <b>Task1Split2</b> that is divided by the 1,150 raw videos.

In <b>Task2</b>, the model is trained with seven categories while tested on the remaining two categories. Task2 requires the model to deal with unlearned content and completely different category-specific questions, which is very challenging. It is worth mentioning that for Task2, we provide an extra set, which can be used in different ways (e.g. semi-supervised learning, weakly supervised learning etc.) to improve the adaption ability of the model.

Two metrics are used in this benchmark to evaluate model performance. The first is <b>accuracy</b> used in existing TextVQA benchmarks. The second is the <b>average normalized Levenshtein similarity</b> (ANLS).

<h3>Download Links and Accessibility</h3>

The download links of annotations are given as follows (v0.0.2):

[Task1Split1Train](Annotations/ViteVQA_0.0.2_t1s1train.json) | [Task1Split1Val](Annotations/ViteVQA_0.0.2_t1s1val.json) | [Task1Split1Test](Annotations/ViteVQA_0.0.2_t1s1test.json)

[Task1Split2Train](Annotations/ViteVQA_0.0.2_t1s2train.json) | [Task1Split2Val](Annotations/ViteVQA_0.0.2_t1s2val.json) | [Task1Split2Test](Annotations/ViteVQA_0.0.2_t1s1test.json)

[Task2Train](Annotations/ViteVQA_0.0.2_t2train.json) | [Task2Val](Annotations/ViteVQA_0.0.2_t2val.json) | [Task2Test](Annotations/ViteVQA_0.0.2_t2test.json) | [Task2Extra](Annotations/ViteVQA_0.0.2_t2extra.json)

Following features are provided:

- Raw videos and frames
- OCR tokens and FRCN features (Extracted by [TransVTSpotter](https://github.com/weijiawu/TransVTSpotter), [ABINet](https://github.com/FangShancheng/ABINet) and [Faster R-CNN](https://github.com/facebookresearch/maskrcnn-benchmark), respectively)
- Object FRCN features and S3D video features (Extracted by [Here](https://github.com/antoyang/just-ask))


Instructions:
-  M4-ViteVQA can only be used for **non-commercial research purposes only**
-  Researchers should read the [responsibility agreement](https://github.com/bytedance/VTVQA/blob/master/M4-ViteVQA_Agreement.pdf) carefully, ask their supervisor/advisor to sign the agreement appropriately, and then send the scanned version  to zhaomy20@fudan.edu.cn or bjli20@fudan.edu.cn.
-  After verifying your request, we will provide the dataset download link.

<h3>Baseline</h3>

We provide [T5-ViteVQA]() as a baseline for ViteVQA.

<h3>Table Ranking</h3>

<h3>TodoList</h3>

<h3>Organization</h3>

Affiliations: 

Fudan University, ByteDance

Authors:

Minyi Zhao, Bingjia Li, Jie Wang, Wanqing Li, Wenjing Zhou, Lan Zhang
Shijie Xuyang, Zhihang Yu, Xinkun Yu, Guangze Li, Aobotao Dai, Shuigeng Zhou

<h3>Contact Us</h3>
Feel free to contact us if you have any problems! zhaomy20@fudan.edu.cn or bjli20@fudan.edu.cn

<h3>Citation</h3>

<h3>License</h3>

- The researcher shall use the M4-ViteVQA dataset only for non-commercial algorithm research and educational purposes. The researcher can not use the M4-ViteVQA dataset for any other purposes, including but not limited to distribution, commercial usage, etc...
- The researcher takes full responsibility for his or her use of the M4-ViteVQA dataset and shall defend and indemnify the dataset, including their affiliates, employees, trustees, officers and agents, against any and all claims arising from the researcher’s use of the M4-ViteVQA dataset.
- The researcher agrees and confirms that authors reserve the right to terminate the researcher’s access to the M4-ViteVQA dataset at any time.
- If the researcher is employed by a for-profit business entity, the researcher’s employer shall also be bound by these terms and conditions, and the researcher hereby shall represent that he or she is fully authorized to enter into this agreement on behalf of such employer.

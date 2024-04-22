# Getting LLM to think and act like a human being: Logical path reasoning and Replanning
<div align="center">

[[Arxiv]](xxx)
[[PDF]](xxx)
[[Videos]](https://github.com/superlin30/Real-World-Web-Agent/assets/48671954/dc1cb04e-d13e-4e98-bc9f-41304b340c12)

[![Python Version](https://img.shields.io/badge/Python-3.9-blue.svg)](https://github.com/MineDojo/Voyager)
[![GitHub license](https://img.shields.io/badge/MIT-blue)]()
______________________________________________________________________
</div>


https://github.com/superlin30/Real-World-Web-Agent/assets/48671954/dc1cb04e-d13e-4e98-bc9f-41304b340c12
______________________________________________________________________
https://github.com/superlin30/Real-World-Web-Agent/assets/48671954/b95ca0e7-5a77-43fe-9cf3-49bd6748c4e1


We introduce a Replanning mechanism for LLM-based agents that dynamically integrates feedback from actions and implicit information which not available in an initial thinking and reasoning framework, forming a bridge between the thinking and acting of LLMs. Compared to other agent methods, experiments conducted on real-life ticket booking websites such as Ctrip and Booking show that our method is more robust in executing clear instructions, capable of successfully completing more steps, and achieving a higher success rate in practical tasks such as ticket booking. especially in challenging tasks that require interactive thinking and action for LLMs.

<p align="center">
  <img src="figs/Comparison%20.png" alt="Comparison" width="95%">
</p>

## Innovations

 We propose three innovative mechanisms: implicit reasoning, Replanning, and Reaction, which make the following contributions:

1. **Implicit reasoning** based on logical path propagation, which integrates explicit and implicit information for reasoning, achieving a cognitive process closer to human-like thinking.

2. **Replanning**, a mechanism based on action feedback, allowing planning to dynamically integrate experiences from successful or failed actions, linking these isolated local optimal decisions for globally optimal Replanning.

3. **Reaction** and inductive deduction based on **Replanning**, which corrects erroneous actions and explores new actions while reassessing and correcting action strategies under a global information set, refining and preserving more general laws and strategies.

<p align="center">
  <img src="figs/Implicit%20reasoning%20and%20Replanning.png" alt="Implicit" width="95%">
</p>


# Our method

The framework is based on three innovative components: **logic path reasoning based** on Knowledge Graphs (KG), **single action process** incorporating environmental feedback and skill management, and **task chain management** for implementing Replanning and Reaction.


<p align="center">
  <img src="figs/Algorithm.png" alt="Algorithm" width="60%">
</p>


1.**The logic path reasoning** component is based on KG, which captures implicit information based on the identity, background, and preferences of the user. The reasoning process involves named entity recognition and KG retrieval, path propagation, and mindmap generation. This approach transforms sparse, document-based knowledge repositories into a more effective knowledge graph-based reasoning and rapid response mechanism.

<p align="center">
  <img src="figs/Logic%20path%20reasoning%20based%20on%20KG.png" alt="Logic" width="95%">
</p>

2.**The single action process** component is based on environmental feedback and skill management. It enables the interaction of Replanning and Reaction in LLM’s actions by treating LLM’s single action as a dynamic skill management system based on environmental feedback. The process involves environmental awareness, skill library management, and error handling mechanism based on environmental feedback.

<p align="center">
  <img src="figs/Roadmap%20of%20single%20action%20process.png" alt="Logic" width="95%">
</p>

3.**The task chain management** component is responsible for implementing Replanning and Reaction. It uses a vector database to store different task chains and merges them based on the vector similarity of the tasks, creating a comprehensive mindmap that encompasses multiple task chains. This mindmap dynamically integrates and manages actions triggered in the past, following the logical relationships of the planned tasks.

<p align="center">
  <img src="figs/Task%20chain.png" alt="Task" width="95%">
</p>






# References

There are several key papers that contribute to the arguments and research field of our work. Let's discuss the significance of these important references:

- **Abend and Rappoport (2017)** - provide an overview of semantic representation, which is crucial for understanding how LLMs process and interpret language. This foundational knowledge is essential for developing the Replanning mechanism. [[PDF]](https://aclanthology.org/P17-1008.pdf)
- **Achiam et al. (2023)** - present the GPT-4 technical report, which is a significant LLM that serves as a basis for the research. Understanding the capabilities and limitations of GPT-4 is vital for developing mechanisms to improve LLM-based agents. [[PDF]](https://arxiv.org/pdf/2303.08774.pdf?fbclid=IwAR2XS6JT2NLIP4MjFn9npot34FhddoqStNbLwIvWETf5ZGlCPsIbuYneo8s&mibextid=Zxz2cZ)
- **Ahn et al. (2022)** - discuss grounding language in robotic affordances, which is relevant to the authors' focus on integrating thinking and action in LLMs. This paper provides insights into how language models can be applied to real-world tasks and the challenges they face. [[PDF]](https://arxiv.org/pdf/2204.01691.pdf)
- **Brown et al. (2020)** - explore the few-shot learning capabilities of language models, which is an important aspect of the authors' research on Replanning. This paper highlights the potential of LLMs to learn from limited examples and adapt to new tasks. [[PDF]](https://proceedings.neurips.cc/paper_files/paper/2020/file/1457c0d6bfcb4967418bfb8ac142f64a-Paper.pdf)
- **Bubeck et al. (2023)** - discuss early experiments with GPT-4, providing further insights into the capabilities of this LLM. This reference helps to contextualize the authors' research within the broader field of LLM development.[[PDF]](https://arxiv.org/pdf/2303.12712.pdf?utm_source=webtekno)
- **Celikyilmaz et al. (2020)** - survey the evaluation of text generation, which is a key aspect of the authors' focus on improving LLM performance in complex tasks. This paper offers a comprehensive overview of the challenges and best practices in text generation. [[PDF]](https://arxiv.org/pdf/2006.14799.pdf)
- **Chang et al. (2023)** - provide a survey on the evaluation of large language models, which is directly relevant to the authors' research on enhancing LLM-based agents. This reference offers a critical analysis of the current state of LLMs and their performance in various tasks. [[PDF]](https://dl.acm.org/doi/abs/10.1145/3641289)
- **Chen et al. (2020)** - review knowledge reasoning over knowledge graphs, which is an important aspect of the authors' focus on integrating explicit and implicit information for reasoning. This paper provides insights into how LLMs can leverage knowledge graphs to improve their reasoning capabilities. [[PDF]](https://www.sciencedirect.com/science/article/pii/S0957417419306669)
- **Chen et al. (2023)** - discuss the robustness of GPT-3.5 to text generation, which is a predecessor to the GPT-4 model used in the authors' research. This reference helps to establish a baseline for understanding the improvements made by the proposed Replanning mechanism. [[PDF]](https://arxiv.org/ftp/arxiv/papers/2303/2303.00293.pdf)




---
permalink: /
title: "Homepage"
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

Yuqiang Sun (孙宇强 in Chinese) is now a research fellow at Nanyang Technological University. 
He got his Ph.D. degree in School of Computer Science and Engineering @ Nanyang Technological University, supervised by [Prof. Yang Liu](https://personal.ntu.edu.sg/yangliu/).
Before Ph.D. study, he got his bachelor degree in Sichuan University.
His research interests include program analysis, vulnerability detection and patch generation.
He hopes to collaborate with more innovative researchers on various exciting topics in software engineering, program analysis, vulnerability detection, and self-evolving LLM agents in software engineering or software security.

<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=KAWDTzsAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=KAWDTzsAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>). -->


<!-- # 🔥 News
- *2025.099: &nbsp;🎉🎉 He is now graduated from NTU!
- *2024.01*: &nbsp;🎉🎉 Happy new year! Our preprint "LLM4Vuln: A Unified Evaluation Framework for Decoupling and Enhancing LLMs' Vulnerability Reasoning" was available on Arxiv! 
- *2023.12*: &nbsp;🎉🎉 Our paper "GPTScan: Detecting Logic Vulnerabilities in Smart Contracts by Combining GPT with Program Analysis" was accepted to appear in ACM SIGSOFT International Conference on Software Engineering (ICSE), Lisbon, Portugal, 2024.
- *2023.08*: &nbsp;🎉🎉 He passed Qualifying Examination (QE) and became a Ph.D. candidate.
- *2023.07*: &nbsp;🎉🎉 Our paper "Who is the Real Hero? Measuring Developer Contribution via Multi-dimensional Data Integration" was accepted by ASE 2023! 
- *2021.08*: &nbsp;🎉🎉 He joined Nanyang Technological University as a Ph.D. student.  -->

# 📖 Educations
- *2021.08 - 2025.09*, Ph.D. student at school of computer science and engineering, Nanyang Technological University, Singapore.
- *2017.09 - 2021.06*, Undergraduate student at college of cyber space and engineering, Sichuan University, Chengdu, Sichuan, P.R.C. 

# 💻 Working Experience
- *2025.04 - now*, Cofounder and Research Lead, Agent LISA.
- *2025.11 - now*, Research Fellow, Nanyang Technological University, Singapore.
- *2025.04 - 2025.10*, Research Engineer, Nanyang Technological University, Singapore.

# 📝 Selected Publications [[Full List](/publication/)]

<!-- <div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2016</div><img src='images/500x300.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> -->

<!-- </div>
</div> -->

- [Using My Functions Should Follow My Checks: Understanding and Detecting Insecure OpenZeppelin Code in Smart Contracts](https://www.usenix.org/conference/usenixsecurity24/presentation/liu-han)
![](https://img.shields.io/badge/CCF-A-red?style=flat-square)[![](https://img.shields.io/badge/UsenixSecurity-2024-blue?style=flat-square)](https://www.usenix.org/conference/usenixsecurity24/presentation/liu-han)
  - Han Liu, Daoyuan Wu, **Yuqiang Sun**, Haijun Wang, Kaixuan Li, Yang Liu, Yixiang Chen
  - Usenix Security 2024 <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:_FxGoFyzp5QC'></span></strong>
  - This paper is about using static analysis to find the unsafe implementations of OpenZeppelin based projects.
  - [Slides for Usenix Security 2024](/assets/pdf/ZepScope.pdf)
  - ZepScope is now open-sourced. Find more at [this website](https://zepscope.github.io/).

- [PropertyGPT: LLM-driven Formal Verification of Smart Contracts through Retrieval-Augmented Property Generation](https://www.ndss-symposium.org/ndss-paper/propertygpt-llm-driven-formal-verification-of-smart-contracts-through-retrieval-augmented-property-generation/) 
![](https://img.shields.io/badge/CCF-A-red?style=flat-square)
[![](https://img.shields.io/badge/NDSS-2025-blue?style=flat-square)](https://www.ndss-symposium.org/ndss-paper/propertygpt-llm-driven-formal-verification-of-smart-contracts-through-retrieval-augmented-property-generation/)
[![](https://img.shields.io/badge/arXiv-2405.02580-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.02580) 
  - Ye Liu, Yue Xue, Daoyuan Wu, **Yuqiang Sun**, Yi Li, Miaolei Shi, Yang Liu
  - Network and Distributed System Security (NDSS) Symposium 2025 <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:eQOLeE2rZwMC'></span></strong>
  - The paper got distinguish paper award from NDSS 2025 🎉🎉!
  - This paper is about generating formal verification rules with LLM for vulnerability detection.

- [Combining Fine-Tuning and LLM-based Agents for Intuitive Smart Contract Auditing with Justifications](https://arxiv.org/abs/2403.16073) 
![](https://img.shields.io/badge/CCF-A-red?style=flat-square) [![](https://img.shields.io/badge/ICSE-2025-blue?style=flat-square)]() [![](https://img.shields.io/badge/arXiv-2403.16073-B31B1B?style=flat-square)](https://arxiv.org/abs/2403.16073)
  - Wei Ma, Daoyuan Wu, **Yuqiang Sun**, Tianwen Wang, Shangqing Liu, Jian Zhang, Yue Xue, Yang Liu
  - Preprint <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:W7OEmFMy1HYC'></span></strong>
  - This paper is about fine-tuning LLMs with knowledge about logic bugs in smart contract to detect vulnerabilities.

- [LLM4Vuln: A Unified Evaluation Framework for Decoupling and Enhancing LLMs' Vulnerability Reasoning](https://arxiv.org/abs/2401.16185) 
[![](https://img.shields.io/badge/arXiv-2401.16185-B31B1B?style=flat-square)](https://arxiv.org/abs/2401.16185)
  - **Yuqiang Sun**, Daoyuan Wu, Yue Xue, Han Liu, Wei Ma, Lyuye Zhang, Miaolei Shi, Yang Liu
  - Preprint <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:zYLM7Y9cAGgC'></span></strong>
  - This paper is about enhancing the ability of LLMs in detecting vulnerabilities by providing extra knowledege and external tools. 

- [GPTScan: Detecting Logic Vulnerabilities in Smart Contracts by Combining GPT with Program Analysis](https://dl.acm.org/doi/abs/10.1145/3597503.3639117)
![](https://img.shields.io/badge/CCF-A-red?style=flat-square) [![](https://img.shields.io/badge/ICSE-2024-blue?style=flat-square)]() [![](https://img.shields.io/badge/arXiv-2308.03314-B31B1B?style=flat-square)](https://arxiv.org/abs/2308.03314)
  - **Yuqiang Sun**, Daoyuan Wu, Yue Xue, Han Liu, Haijun Wang, Zhengzi Xu, Xiaofei Xie, Yang Liu
  - The 46th IEEE/ACM International Conference on Software Engineering (ICSE 2024) <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:YsMSGLbcyi4C'></span></strong>
  - This paper is about combining LLM with static analysis method to detect vulnerabilities in smart contracts. 
  - [Slides for ICSE 2024](/assets/pdf/GPTScanSlides.pdf)
  - GPTScan is now open-sourced. Find more at [this website](https://gptscan.github.io/).

- [Who is the Real Hero? Measuring Developer Contribution via Multi-dimensional Data Integration](https://ieeexplore.ieee.org/document/10298552/) 
![](https://img.shields.io/badge/CCF-A-red?style=flat-square) [![](https://img.shields.io/badge/ASE-2023-blue?style=flat-square)](https://ieeexplore.ieee.org/document/10298552/)
  - **Yuqiang Sun**, Zhengzi Xu, Chengwei Liu, Yiran Zhang, Yang Liu
  - The 38th IEEE/ACM International Conference on Automated Software Engineering (ASE 2023) <strong><span class='show_paper_citations' data='KAWDTzsAAAAJ:qjMakFHDy7sC'></span></strong>
  - This paper is about measuring the contribution of developers in open source projects. We proposed an approach to fuse information from different dimensions for a more comprehensive evaluation of developer contribution. 

<!-- # 🎖 Honors and Awards
- *2021.10* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.09* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->

# 💬 Invited Talks
- *2024.05*, Transforming Language Models into Smart Contract Audit Experts. GeekCon 2024 @ Singapore
  - [Slides](/assets/pdf/geekcon2024.pdf)

<!-- # 💻 Internships
- *2019.05 - 2020.02*, [Lorem](https://github.com/), China. -->

# 📫 Services

- Junior/Shadow PC: MSR 2024/2025, ICSE 2026
- Artifact Evaluation: Usenix Security 2024, ISSTA 2024
- Journals: TDSC, TOSEM
- Sub-reviewer: ICSE, ISSTA, ASE, RAID, AisaCCS, ICICS, Usenix Security, CCS, NDSS


# 📚 Teaching

- Teaching Assistant of SC1003: Introduction to Computer Thinking and Programming, NTU, 2023 Fall
- Teaching Assistant of SC1006: Computer Organization and Architecture, NTU, 2023 Spring

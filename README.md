<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Rithin%20Ragunathan&fontSize=52&fontColor=38bdf8&fontAlignY=38&desc=Engineering%20Student%20%E2%80%A2%20AI%2FML%20%E2%80%A2%20Computer%20Vision&descColor=94a3b8&descAlignY=60&animation=fadeIn"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1000&color=38BDF8&center=true&vCenter=true&width=600&lines=Learning+every+single+day+%E2%9C%A6;Java+Developer+%7C+Backend+Engineer;Building+systems+from+first+principles.;AI+%2F+ML+%7C+Computer+Vision+%7C+DeepStream;RAG+from+scratch+%7C+YOLO+Pipelines)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rithinragunathan-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rithinragunathan)
[![GitHub](https://img.shields.io/badge/GitHub-rithinragunathan-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rithinragunathan)
[![Portfolio](https://img.shields.io/badge/Portfolio-rithinragunathan-38bdf8?style=for-the-badge&logo=githubpages&logoColor=white)](https://rithinragunathan.github.io/Portfolio/)

</div>

---

## `whoami`

```python
rithin = {
    "institute"  : "Bannari Amman Institute of Technology, Sathyamangalam",
    "branch"     : "Electronics & Communication Engineering (ECE)",
    "focus"      : ["AI/ML", "Computer Vision", "Edge AI", "Generative AI"],
    "philosophy" : "Understand how things work at the deepest level — then build.",
    "approach"   : "First principles before frameworks. Always.",
    "portfolio"  : "https://rithinragunathan.github.io/Portfolio/",
}
```

---

## ◈ Skills

### 💻 Programming

| Language | Level | Notes |
|----------|-------|-------|
| Python | Intermediate → Advanced | Primary language for AI/ML work |
| Java | Solid | OOP, DSA problem solving |
| C++ | Basic | STL, strings |
| javaScript| Basic |Basic Function|

---

### 🤖 AI / Machine Learning

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Ultralytics](https://img.shields.io/badge/Ultralytics_YOLO-111F68?style=flat-square&logo=yolo&logoColor=white)

- **Computer Vision** — Object detection, tracking, image processing & feature extraction
- **Deep Learning Models** — YOLOv8, YOLOv11 integration into real-time systems
- **Model Integration** — Connecting models to production pipelines

---

### 📹 Video Analytics & Edge AI

![DeepStream](https://img.shields.io/badge/NVIDIA_DeepStream-76B900?style=flat-square&logo=nvidia&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLOv8%2Fv11-00FFFF?style=flat-square&logoColor=black)

- **NVIDIA DeepStream SDK** — Python-based real-time video analytics pipelines
- **Object Detection + Tracking** — Multi-class, multi-object real-time systems
- **ROI Analytics** — Polygon zone-based spatial filtering
- **Line Crossing Detection** — IN/OUT entry-exit counting logic
- **PeopleNet + YOLO** — Model integration & substitution within DeepStream

---

### 🎯 Generative AI & LLMs

- **Prompt Engineering** — Few-shot, structured output, chain-of-thought
- **RAG** — Retrieval-Augmented Generation (conceptual + from-scratch implementation)
- **Embeddings & Vector Search** — Basic understanding and implementation
- **Context Handling** — Grounding techniques, long context management

---

### 🧰 Tools & Systems

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![VSCode](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)

---

## ◈ Projects

<details>
<summary><b>🔹 YOLO-Based Object Tracking & Counting System</b> — <code>Complete</code></summary>

<br/>

> Real-time object detection and tracking with spatial intelligence — counts people and vehicles crossing defined regions.

**Tech Stack:** `Python` `OpenCV` `YOLOv8` `YOLOv11`

- Polygonal ROI selection with custom zone definition
- Line crossing logic — separate IN/OUT counters
- Logging and snapshot capture on detection events
- Supports both people and vehicle class tracking

</details>

---

<details>
<summary><b>🔹 DeepStream People Analytics Pipeline</b> — <code>Complete</code></summary>

<br/>

> Production-grade real-time people detection pipeline on NVIDIA hardware using DeepStream SDK and PeopleNet model.

**Tech Stack:** `NVIDIA DeepStream` `Python` `PeopleNet` `nvdsanalytics`

- `nvdsanalytics` plugin for line crossing detection
- ROI filtering with polygonal zone support
- Entry/exit counting system at scale
- Tracking accuracy optimization at the pipeline level

</details>

---

<details>
<summary><b>🔹 YOLO + DeepStream Integration</b> — <code>Complete</code></summary>

<br/>

> Replaced the default DeepStream inference engine with a custom YOLOv11 model — optimized for real-time throughput.

**Tech Stack:** `YOLOv11` `DeepStream SDK` `Python`

- Full model substitution within the DeepStream pipeline
- Adapted config files and custom parser for YOLO output format
- Pipeline-level optimization for FPS and latency

</details>

---

<details>
<summary><b>🔹 Real-World Object Size Measurement</b> — <code>Complete</code></summary>

<br/>

> Measures physical dimensions of objects from images using classical computer vision — pure geometric reasoning, no deep learning.

**Tech Stack:** `OpenCV` `Python` `NumPy`

- Contour detection for object boundary extraction
- Perspective transformation for top-down view alignment
- Calibration techniques for pixel-to-real-world unit mapping
- Preprocessing pipeline for improved measurement accuracy

</details>

---

<details>
<summary><b>🔹 Custom RAG Pipeline</b> — <code>🔧 In Progress</code></summary>

<br/>

> Building Retrieval-Augmented Generation entirely from scratch — no LangChain, no shortcuts. Understanding every layer before abstracting it.

**Tech Stack:** `Python` `Embeddings` `Vector Search`

- Document chunking strategies (size, overlap, semantic)
- Embedding generation pipeline
- Vector similarity search implementation
- Core retrieval logic without relying on any frameworks

</details>

---

<details>
<summary><b>🔹 DSA Practice — Java</b> — <code>⚡ Ongoing</code></summary>

<br/>

> Systematic problem solving with emphasis on complexity, edge cases, and clean internal logic.

**Focus:** `Arrays` `Strings` `Linked Lists` `Recursion`

- Structured recursion via 3-Question Framework (base case · recursive relation · progress)
- Time & space complexity analysis on every solution
- Debug-first approach — understand before optimizing

</details>

---

## ◈ Currently Learning

```
┌───────────────────────────────────────────────────────────────┐
│                                                               │
│   🌐  Backend Dev      →   Spring Boot, REST APIs            │
│   🎨  Frontend Dev     →   React, component architecture     │
│   ☁️  Cloud & DevOps   →   AWS (EC2, S3), Docker             │
│   🧬  Transformers     →   From scratch, code-first          │
│   🤖  Advanced GenAI   →   Agents, eval, long context        │
│   🐧  Linux Internals  →   Process mgmt, perf tuning         │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

---

## ◈ Approach

> *"I don't want to just use tools — I want to understand how they work at every level, so I can build better ones."*

```
  01. Understand systems deeply — before reaching for abstractions
  02. Build from scratch first — then leverage frameworks
  03. Debug thoroughly — internal clarity over speed
```

---

## ◈ Next Goals

- [ ] Build a full-stack AI application — **React + Spring Boot + AI model** — local to deployed
- [ ] Deploy projects using **AWS & Docker** with a repeatable CI/CD workflow
- [ ] Optimize real-time systems — push FPS, latency, and accuracy to production level
- [ ] Implement a **Transformer from scratch** — attention, encoder/decoder, training loop, zero frameworks

---

## ◈ Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Let's%20Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rithinragunathan)
&nbsp;
[![Portfolio](https://img.shields.io/badge/Portfolio-View%20My%20Work-38bdf8?style=for-the-badge&logo=githubpages&logoColor=white)](https://rithinragunathan.github.io/Portfolio/)
&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rithinragunathan)

</div>

---

## ◈ GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=rithinragunathan&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=38bdf8&icon_color=38bdf8&text_color=94a3b8" height="165"/>
&nbsp;&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=rithinragunathan&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=38bdf8&text_color=94a3b8" height="165"/>

<br/><br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=rithinragunathan&theme=tokyonight&hide_border=true&background=0d1117&stroke=38bdf8&ring=38bdf8&fire=fbbf24&currStreakLabel=38bdf8" height="165"/>

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer&text=Work%20in%20progress%20%E2%80%94%20learning%20every%20day&fontSize=16&fontColor=38bdf8&fontAlignY=65&animation=fadeIn"/>

</div>

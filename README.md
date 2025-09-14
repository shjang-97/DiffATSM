# DiffATSM: High Quality Adaptive Time-Scale Modification using Diffusion-based Post-Processing

This repository will host the official implementation of the paper:

> **DiffATSM: High Quality Adaptive Time-Scale Modification using Diffusion-based Post-Processing**  
> Sohee Jang, Yeon-Ju Kim, Joon-Hyuk Chang  


---

## 🔔 Notice
In accordance with institutional policies, the **full implementation will be released after the official publication** of the paper.  

For now, this repository provides:
- Paper abstract and citation information  
- Planned code structure and dependencies  
- Contact information for inquiries  

---

## 📖 Abstract
The advent of adaptive time-scale modification (ATSM) has marked a significant evolution in audio processing, applying adaptive speaking rates that surpass the performance of conventional time-scale modification (TSM) systems employing a fixed speaking rate. However, ATSM requires audio transcriptions and additional phoneme localization modules, which limit its applicability when such resources are unavailable. Furthermore, traditional signal processing approaches in the time domain often degrade audio quality due to artifacts resulting from phase mismatches.  

To overcome these limitations, we propose **DiffATSM**, a novel deep learning-based TSM framework that directly generates time-scaled speech from raw waveforms without requiring transcription. DiffATSM comprises two main components: an adaptive neural generator and a post-processing network using a diffusion probabilistic model. The adaptive neural generator modulates the temporal scale of the mel spectrogram by conditioning on phonetic posteriorgrams (PPG), which are extracted from a self-supervised speech model. These PPG features serve as auxiliary information to preserve phonetic structure during time scaling. The generated spectrogram is further refined by the diffusion-based post-processing network, which enhances fidelity by modeling complex speech distributions.  

Our experimental results demonstrate that DiffATSM significantly outperforms existing TSM algorithms, including ATSM, in subjective and objective evaluations.  

---

## 📂 Planned Repository Structure
```
DiffATSM/
├── data/              # scripts for dataset preparation
├── models/            # model definitions (Diffusion, PPG encoder, etc.)
├── training/          # training scripts and configs
├── inference/         # inference & evaluation scripts
└── README.md
```
---

## 📦 Dependencies
- Python >= 3.9  
- PyTorch >= 2.0  
- torchaudio, librosa  
- tqdm, matplotlib, numpy  

A full `requirements.txt` will be provided after release.

---

## 📜 Contact
For questions, please contact: 
- Sohee Jang (shjang97@hanyang.ac.kr)

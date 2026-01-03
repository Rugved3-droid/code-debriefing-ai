# 🏥 Automated Code Debriefing Timeline Generator

**AI-powered timeline extraction from medical simulation videos using Google Gemini**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/code-debriefing-ai/blob/main/Code_Debriefing_Tool.ipynb)

---

## 📖 Overview

This tool automatically analyzes medical code/emergency simulation videos and generates comprehensive debriefing timelines. It uses Google's Gemini multimodal AI to extract:

- **Timestamped event timelines** (30-50+ events)
- **All medications** with doses, routes, and timing
- **Team communication patterns** and closed-loop examples
- **Protocol adherence assessment** (ACLS/ALSO/ATLS)
- **Quality metrics** (time to CPR, shock, medications, ROSC)
- **Key teaching moments** for debriefing sessions

### Supported Scenarios
- ✅ ACLS Cardiac Arrest (VF/VT, PEA, Asystole)
- ✅ Postpartum Hemorrhage
- ✅ Trauma Resuscitation
- ✅ Respiratory Emergencies
- ✅ Any acute care simulation

---

## 🚀 Quick Start

### Step 1: Get a Free Gemini API Key
1. Go to [Google AI Studio](https://aistudio.google.com/apikey)
2. Click **"Create API Key"**
3. Copy your key (starts with `AIza...`)

### Step 2: Open in Google Colab
1. Click the **"Open in Colab"** badge above, OR
2. Upload `Code_Debriefing_Tool.py` to [Google Colab](https://colab.research.google.com/)

### Step 3: Add Your API Key as a Secret
1. In Colab, click the **🔑 Key icon** in the left sidebar
2. Click **"+ Add new secret"**
3. **Name:** `GEMINI_API_KEY`
4. **Value:** Paste your API key
5. Toggle **"Notebook access"** to **ON**

### Step 4: Run!
1. Run the notebook cells in order
2. Upload your simulation video when prompted
3. Wait 2-5 minutes for analysis
4. Download your debriefing timeline!

---

## 📋 Output Example

The tool generates structured output like:

```
QUESTION 1: SCENARIO IDENTIFICATION
ACLS Cardiac Arrest - Pulseless VT secondary to Anterior STEMI
70-year-old male with 2 hours of substernal chest pain

QUESTION 2: COMPLETE TIMELINE
[00:16] Patient handoff begins - [Communication]
[01:05] Monitor shows ST-elevation, "Anterior STEMI" confirmed - [Assessment]
[03:52] Patient becomes unresponsive - [Assessment]
[03:58] No pulse confirmed, "Start CPR" called - [Outcome]
[04:02] Chest compressions initiated - [Intervention]
[05:11] Shock #1 delivered at 200J - [Intervention]
[05:37] Epinephrine 1mg IV administered - [Medication]
...

QUESTION 13: QUALITY METRICS
- Time to first CPR: 4 seconds
- Time to first shock: 73 seconds
- Time to first medication: 99 seconds
- Time to ROSC: 4 minutes 33 seconds
```

---

## 🔧 Requirements

- Google Colab (free) OR Python 3.8+
- Google Gemini API key (free tier available)
- Video file (MP4, MOV, AVI, MKV, WEBM)

### Local Installation (Optional)
```bash
pip install google-genai
```

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `Code_Debriefing_Tool.py` | Main Python script for Colab |
| `Code_Debriefing_Tool.ipynb` | Jupyter notebook version |
| `README.md` | This file |
| `LICENSE` | MIT License |

---

## ⚠️ Medical Disclaimer

**FOR EDUCATIONAL AND RESEARCH PURPOSES ONLY**

This tool is designed for:
- Post-event debriefing of **simulation exercises**
- Medical education and training
- Quality improvement research

This tool is **NOT** intended for:
- Real-time clinical decision support
- Patient care documentation
- Diagnostic purposes

**Always follow your institution's policies regarding video recording and AI use in medical education.**

---

## 🔒 Privacy & Security

- **Your API key** is stored securely in Colab Secrets (never in code)
- **Videos are uploaded** to Google's servers for processing, then deleted
- **No data is retained** after analysis completes
- Review Google's [Gemini API Terms](https://ai.google.dev/terms) for data handling

**Recommendation:** Do not upload videos containing real patient information. Use simulation recordings only.

---

## 📊 Performance

Based on validation with 3 simulation scenarios:

| Metric | Result |
|--------|--------|
| Event Detection Rate | >95% |
| Temporal Accuracy | ±10-15 seconds |
| Medication Capture | 100% (14/14) |
| Processing Time | 2-5 minutes |

---

## 📚 Citation

If you use this tool in research, please cite:

```
Parmar R, Lee M. Multimodal AI for Automated Code Debriefing: Feasibility 
of Timeline Reconstruction Using Commercially Available Tools. 
Medical Teacher. 2025. [Submitted]
```

---

## 👥 Authors

- **Rugved Parmar, MD** - SUNY Downstate Health Sciences University
- **Megan Lee, MD** - SUNY Downstate Health Sciences University

**Contact:** parmarrugved@gmail.com

---

## 🙏 Acknowledgments

- [Antigravity AI](https://antigravity.ai) for technical consultation
- Google Gemini team for multimodal AI capabilities

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

**Ideas for contribution:**
- Additional prompt templates for specific scenarios
- Integration with other LLM providers
- Web interface development
- Multi-language support

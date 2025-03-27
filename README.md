# 🛡️ SecureGPT for Video Understanding  
_A simple guide for using Stanford Health Care's Secure GPT-4o to analyze local video files privately_

**Author:** Hee Jung Choi  
**Lab use only | HIPAA-conscious**

---

### 🧠 Project Context

This guide was developed at Stanford Medicine to help researchers securely analyze videos using the SHC/SoM deployment of GPT-4o. Since video data may contain patient-sensitive information, this workflow ensures all processing happens **locally**, and only **downsampled video frames** are sent securely to SHC’s GPT-4o API. The code is adapted from OpenAI’s cookbook but modified for **HIPAA safety and institutional deployment**.

---

## 📘 Overview

This short Python notebook demonstrates how to use Stanford Health Care & Stanford School of Medicine’s **Secure GPT-4o** deployment to analyze and describe videos **without uploading them to the cloud**. It’s adapted from [OpenAI's Cookbook](https://github.com/openai/openai-cookbook), but tailored for secure, local workflows.

🎯 **Key benefit**: The videos stay on your **local machine**, which helps **avoid HIPAA violations** by keeping patient data private.

---

## 🔧 What It Does

- ✅ Sends locally saved video frames (not the full video) to GPT-4o via SHC’s secure API
- ✅ Downsamples frames to avoid long transfer time
- ✅ Requests a high-level natural-language **description** of the video
- ✅ Displays sample frames inline for sanity check

---

## 🚀 How to Use

1. **Set up your environment**  
   - Python 3.8+
   - `cv2`, `requests`, `base64`, `IPython`

2. **Open the notebook**:  
   [`secure_gpt4o_video_guide.ipynb`](./secure_gpt4o_video_guide.ipynb)

3. **Replace the placeholder API key**  
   In the code cells that define `headers`, replace:
   ```python
   "Ocp-Apim-Subscription-Key": "XXX"

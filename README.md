# 🛡️ SecureGPT for Video Understanding  
_A simple guide for using Stanford Health Care's Secure GPT-4o to analyze local video files privately_

**Lab use only | HIPAA-conscious**

---

### 🧠 Project Context

This guide was developed to help researchers securely analyze videos using the SHC/SoM deployment of GPT-4o. It demonstrates how to process a locally saved video by encoding it into a Base64 data URL, ensuring HIPAA compliance by keeping all data processing local before interacting with Stanford's Secure GPT-4o. 

> **Note**: If you are off-campus, make sure your Stanford VPN is connected.

The code is adapted from OpenAI’s [cookbook](https://github.com/openai/openai-cookbook) but modified for HIPAA safety and institutional deployment at Stanford Medicine.

---

## 📘 Overview

This short Python notebook shows how to use Stanford Health Care & Stanford School of Medicine’s Secure GPT-4o deployment to analyze and describe videos *without uploading them to the public cloud.  

🎯 **Key Benefit**: The videos stay on your local machine, reducing the risk of HIPAA violations by keeping patient data private.

---

## 🔧 What It Does

- ✅ Sends locally saved video frames securely to GPT-4o via SHC’s API
- ✅ Downsamples frames to reduce transfer and processing time
- ✅ Asks GPT-4o for a high-level natural-language description of the video
- ✅ Displays sample frames inline for sanity checks

---

## 🚀 How to Use

1. **Check your network**
   - If you are on campus, you are already connected to the Stanford network.
   - If you are off campus, [connect to the Stanford VPN](https://www.uit.stanford.edu/service/vpn) before running this notebook.

2. **Set up your environment**
   - Python 3.8+
   - Required packages:
     ```
     pip install opencv-python requests IPython
     ```
   
3. **Open the notebook**  
   [`secure_gpt4o_video_guide.ipynb`](./secure_gpt4o_video_guide.ipynb)

4. **Insert your SHC API key**
   In the code cell where `headers` is defined, replace:
   ```python
   "Ocp-Apim-Subscription-Key": "XXX"

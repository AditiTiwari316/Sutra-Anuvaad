# 📜 Sutra-Anuvaad: AI-Powered Historical Land Record Decipherer
**Track:** AI for Communities, Access & Public Impact  
**Submission for:** AI for Bharat (Hack2Skill)

---

## 🌟 Vision & Problem Statement
In rural India, land disputes account for nearly 60-70% of all civil litigation. Many of these disputes stem from the inability to read 50-70 year old documents written in archaic scripts (Modi, Kaithi, Old Urdu) and complex revenue terminology. 

**Sutra-Anuvaad** bridges this gap using a multimodal AI pipeline to restore, decipher, and translate these records into simple, modern regional languages, empowering the "Next Billion Users."

---

## 🤖 Why AI? (Evaluation Focus)
Standard rule-based OCR and translation fail for this use case because:
1. **Visual Degradation:** 70-year-old paper has ink-bleeds and stains that rule-based binarization cannot clean. We use **GANs (ESRGAN)** for intelligent restoration.
2. **Extinct Scripts:** Scripts like 'Modi' are cursive and non-standardized. We use **Vision Transformers (TrOCR)** which understand the *context* of handwriting, not just shapes.
3. **Semantic Drift:** Legal terms change meaning over decades. Our **RAG (Retrieval-Augmented Generation)** system ensures the AI doesn't "hallucinate" but pulls from a verified **Indian Revenue Lexicon**.

---

## 🏗️ The AI Pipeline (Technical Architecture)
Our system follows a 4-stage pipeline designed for the "Bharat" environment:

1. **Edge Pre-processing :** OpenCV & TensorFlow Lite perform on-device document detection to work in low-bandwidth (2G/3G) rural areas.
2. **Vision Core :** GANs restore the image quality $\rightarrow$ TrOCR extracts text from archaic scripts.
3. **The "Legal Brain" :** LangChain orchestrates a RAG flow using **Pinecone/ChromaDB** to map historical terms to modern legal definitions.
4. **Vernacular Output :** **IndicTrans2** translates the result, and **Bhashini APIs** provide voice-overs in local dialects for low-literacy accessibility.

---

## 📁 Project Documentation
Developed and refined using **Kiro**, our documentation provides a deep technical roadmap:
- [📄 Requirements Document](./requirements.md) - Functional & Non-functional specs.
- [🏗️ Technical Design](./design.md) - System architecture, RAG design, and Data flow.
- [📋 Implementation Plan](./tasks.md) - 42 structured tasks and 39 property-based tests.

---

## 🛡️ Responsible AI & Design
- **Fact-Checking:** Every translation includes a "Confidence Heatmap."
- **Human-in-the-loop:** Low-confidence results are automatically flagged for Revenue Officer certification.
- **Privacy:** Land records are encrypted with AES-256; PII masking is applied to protect citizen identity.
- **Inclusion:** Voice-first interface and Neumorphic UI designed specifically for rural smartphone users.

---

## 🚀 Impact & Business Feasibility
- **Beneficiaries:** 100M+ rural landholders, Legal-tech startups, and Government Revenue Departments.
- **GTM Strategy:** Pilot via **Common Service Centres (CSCs)** and integration with the Digital India Land Records Modernization Programme (DILRMP).
- **Sustainability:** A freemium model (Basic reading is free; certified summaries for court are paid).

---

## 👥 The Team - 2A-Innovators
- **[Amber Gangrade]** 
- **[Aditi Tiwari]** 

---
*Developed with ❤️ for AI for Bharat 2026 ✨*

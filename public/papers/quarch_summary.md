# QuArch.ai: Design and Implementation Summary

## Overview
QuArch (Question-Answering in Computer Architecture) is a specialized full-stack platform and research dataset designed to bridge the gap between hardware engineering and Generative AI. While domains like software engineering and medicine have seen rapid AI adoption, computer architecture has lacked high-quality, domain-specific benchmarks. QuArch solves this by providing a curated dataset of thousands of human-validated Q&A pairs grounded in a 1-billion-token corpus called **Archipedia**.

## Platform Architecture

### 1. Full-Stack Data Collection
I built the QuArch platform to facilitate community-driven data collection. The system is designed to be a "living dataset" where researchers and students can contribute while benefiting from integrated AI tools.
- **Backend Orchestration**: Integrated with **OpenRouter** to allow testing against a wide range of state-of-the-art LLMs (GPT-4o, Claude 3.5 Sonnet, Llama 3, etc.).
- **User Verification**: Real-time email verification and contributor tracking using **Resend**.
- **Human-in-the-Loop**: The platform ensures that while AI helps generate and test questions, humans remain the ultimate authority through a multi-tiered review process.

### 2. The Submission Pipeline
- **Sketchpad**: An intuitive interface for drafting complex technical questions, supporting Markdown and image attachments.
- **LLM Panel Testing**: A unique feature where a panel of LLMs tests a submitted question in unison. This provides the user with immediate feedback on whether their question is "LLM-proof" or requires more domain-specific reasoning.
- **Rationale Integration**: Contributors provide detailed rationales for correct answers, which are then used to fine-tune smaller open-source models (improving accuracy by up to 8.3%).

### 3. Archipedia Corpus
The foundation of QuArch is **Archipedia**, a compilation of 50 years of computer architecture knowledge. It synthesizes:
- Academic literature and research papers.
- Technical documentation from industry leaders.
- Educational materials and lecture notes.

## Research Impact
- **Benchmarking**: Identified a significant "knowledge gap" where even the best closed-source models (84% accuracy) struggle with complex system-level trade-offs like memory hierarchy and interconnects.
- **Community Engagement**: Newest challenges like the **Architecture 2.0 Workshop (ASPLOS 2026)** incentivize contributions by offering acknowledgement as research co-authors.
- **Open Access**: The dataset and leaderboard are hosted publicly to advance AI-driven computer architecture research.

## Technical Stack
- **Frontend**: React / Tailwind CSS / Framer Motion (Warp Grid System).
- **Backend**: Node.js / OpenRouter API / Resend.
- **Database**: Systems engineering dataset (1,500+ validated pairs).
- **Deployment**: Architecture 2.0 Workshop Integration.

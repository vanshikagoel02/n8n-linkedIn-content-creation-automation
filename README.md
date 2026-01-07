# n8n-linkedIn-content-creation-automation

An end-to-end **LinkedIn content creation automation workflow** built using **n8n**, **Google Sheets**, **Tavily API**, and an **AI Chat Model (Google Gemini)**.  
This project automatically generates high-quality LinkedIn post content based on selected topics and updates the output directly into Google Sheets.

---

## 📌 Project Overview

Creating consistent, insightful LinkedIn content is time-consuming. This workflow automates the entire process:

1. Select a **topic** from Google Sheets  
2. Fetch **relevant context and insights** using Tavily (web search API)  
3. Generate **engaging LinkedIn post content** using an AI Agent  
4. Store the generated content back into Google Sheets  
5. Optionally trigger the workflow manually or on a schedule  

This makes the workflow ideal for **personal branding, content creators, founders, and marketers**.

---

## 🛠️ Tech Stack

- **n8n** – Workflow automation  
- **Google Sheets API** – Input/output data source  
- **Tavily API** – Contextual web research  
- **Google Gemini Chat Model** – AI-powered content generation  
- **GitHub** – Version control and project sharing  

---

## 🔁 Workflow Architecture
- Trigger (Manual / Schedule(7am daily))
- Read Topic from Google Sheets
- Fetch Context via Tavily API
- AI Agent (Content Generation)
- Update Content & Status in Google Sheets

---

## 🧩 n8n Workflow Breakdown

### 1. Trigger Node
- Manual execution (`When clicking "Execute workflow"`)
- Optional **Schedule Trigger** for automation

### 2. Get Topic (Google Sheets)
- Reads the selected topic (e.g., *AI Image Generation*)
- Uses status tracking (`To Do`, `Created`)

### 3. Tavily Node
- Fetches real-time insights and context from the web
- Enhances AI output quality

### 4. AI Agent
- Uses **Google Gemini Chat Model**
- Converts topic + research into a polished LinkedIn post
- Includes:
  - Hook
  - Value points
  - CTA
  - Relevant hashtags

### 5. Update Row in Google Sheets
- Writes generated content back to the sheet
- Updates status to `Created`

---

## 📸 Screenshots

### n8n Workflow
<img width="1365" height="434" alt="image" src="https://github.com/user-attachments/assets/855e035e-24ec-4b06-9889-86a2d86a3358" />

### Google Sheets Output
<img width="1919" height="677" alt="image" src="https://github.com/user-attachments/assets/3c5869b5-4770-4688-a7e2-e51db54430d3" />

---

## 📊 Google Sheets Structure

| Column | Description |
|------|------------|
| TOPIC | Topic for LinkedIn post |
| STATUS | To Do / Created |
| CONTENT | Generated LinkedIn post |

---

## 🚀 How to Use

1. Clone the repository
2. Import the workflow JSON into **n8n**
3. Set up credentials for:
   - Google Sheets
   - Tavily API
   - Google Gemini
4. Add topics in Google Sheets
5. Execute the workflow
6. Content will be auto-generated and updated 🎯

---
- Vanshika Goel
- Developer

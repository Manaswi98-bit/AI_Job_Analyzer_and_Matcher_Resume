🤖 **AI Recruiter Pipeline: Job Analyzer & Resume Matcher** 📄✨


An automated, data-driven recruitment intelligence system built with LangChain and Google Gemini-2.5-Flash. This pipeline ingests messy, unstructured job descriptions, extracts core professional parameters into clean schemas, and cross-evaluates candidate resumes to provide compatibility scores and actionable optimization tips.


🚀 Key Features

🔍 Automated Job Extraction: Parses unstructured job postings to dynamically extract job titles, target experience levels, mandatory technical skills, and bonus qualifications.

🎯 Objective Match Engine: Critically evaluates resumes against extracted requirements, providing a concrete percentage fit score.

🛡️ Robust JSON Guard: Uses a customized structural parsing layer (RobustJsonParser) that strips out LLM conversational fluff, guaranteeing flawless pipeline data flow.

📊 Insight Dashboard: Generates clean, terminal-friendly evaluation summaries with actionable optimization recommendations for candidates.


🛠️ Technology Stack

Core Orchestration: LangChain (Expression Language & Prompts)

LLM Provider: Google Generative AI (gemini-2.5-flash)

Data Validation: Pydantic (Schemas & Blueprints)

Environment Management: python-dotenv


🏗️ Architecture & Component Flow

The application functions through a structured multi-stage execution workflow:


[Raw Job Description] ──> 🧾 Job Analyzer Chain ──> [Structured JSON Data]

                                                               │
                                                               ▼
                                                               
[Candidate Resume]     ──> 🎯 Matcher Engine   <───────────────┘

                               │
                               ▼
                               
                        📊 Final Dashboard Report


📊 Sample Output Report

When executed, the system renders structured insights directly to the reporting interface:

==================== FINAL RECRUITER INSIGHT REPORT ====================
 Evaluated Position  : Senior AI & Data Developer
 Candidate Fit Score : 35%

 Overlapping Skills  : Python, SQL
 Missing Skill Gaps  : FastAPI, MongoDB

** Actionable Resume Optimization Tips:
  • Gain at least 2 more years of experience to meet the '5+ years' requirement for a Senior role.
  • Acquire hands-on experience with FastAPI, as it is a mandatory skill for this position.
  • Develop proficiency in MongoDB, which is a critical mandatory skill.
  • Consider learning AWS to align with the preferred skills for the role.
========================================================================**

# Product Requirement Document (PRD) – Toxic Content Moderation

## Objective
Reduce toxic comment visibility by 70% and improve community trust by deploying an AI-powered moderation system.

## Problem
- Harassment and abuse are rampant on social platforms.
- Manual moderation is slow and inconsistent.
- Victims suffer before content is removed → reduced trust and engagement.

## Scope
- Detect harassment, hate speech, threats, profanity in comments.
- Auto-hide or flag comments based on toxicity score.
- Provide moderators with a dashboard to review flagged items.
- Support multilingual moderation (English + Hindi initially).

## User Stories
- As a **creator**, I want abusive comments hidden quickly so my community feels safe.  
- As a **moderator**, I want a clear review queue so I can focus on borderline cases.  
- As a **user**, I want to understand why my comment was flagged to maintain fairness.  

## Functional Requirements
- NLP-based toxicity detection (e.g., BERT, Perspective API).  
- Confidence thresholds for actions:
  - >90% → Auto-hide.  
  - 70–90% → Queue for moderation.  
  - <70% → Keep visible, but flagged for review.  
- Moderator dashboard with approve/reject flow.  
- Feedback loop to retrain the model.  

## Non-Functional Requirements
- Latency <2s for comment scanning.  
- Accuracy: precision ≥ 85%, recall ≥ 80%.  
- Data privacy compliance (no user PII stored).  

## KPIs
- Toxic content visibility ↓ 70%.  
- Moderation time per comment ↓ 60%.  
- Creator NPS ↑ +15 points.  
- Community engagement ↑ 20%.  

 

---

# Smart Recruitment Support System

### Using Large Language Models and Contextual Semantic Scoring

---

## 1. Overview

The Smart Recruitment Support System is an AI-driven web application designed to automate bulk resume screening and job–candidate matching using Large Language Models (LLMs).

The system addresses the limitations of manual and keyword-based recruitment processes by enabling semantic understanding of resumes and job descriptions, supporting multi-job matching, and ensuring scalable processing of large datasets.

---

## 2. Objectives

* To develop a system capable of processing multiple resumes and job descriptions in bulk
* To extract structured information using LLMs from unstructured documents
* To design a multi-criteria scoring framework for candidate-job matching
* To implement duplicate detection using SHA-256 hashing
* To enable automatic re-matching of resumes with newly added jobs
* To provide a dashboard for ranking candidates and managing recruitment workflows
* To integrate automated email notifications for candidate communication

---

## 3. Key Features

### 3.1 Bulk Document Processing

* Supports batch upload of resumes and job descriptions in PDF and DOCX formats
* Handles large-scale recruitment scenarios efficiently

### 3.2 LLM-Based Information Extraction

* Extracts structured data such as skills, experience, and contact details from resumes
* Extracts job attributes including required skills, role, and experience

### 3.3 Multi-Criteria Matching Engine

Each candidate is evaluated based on four weighted dimensions:

* Skills Alignment: 40%
* Experience Relevance: 30%
* Domain Fit: 20%
* Overall Suitability: 10%

Candidates receive:

* A score between 0 and 100
* AI-generated feedback explaining the evaluation

A candidate is considered matched if the score is greater than or equal to 50.

---

### 3.4 Duplicate Detection

* Implements SHA-256 hashing on extracted resume text
* Prevents redundant processing of identical resumes

### 3.5 Automatic Re-Matching

* Previously unmatched resumes are automatically evaluated against newly uploaded job descriptions

### 3.6 Multi-Job Candidate Identification

* Identifies candidates suitable for multiple job roles

### 3.7 Results Dashboard

* Displays ranked candidates per job
* Supports status management for each candidate-job pair

### 3.8 Email Notification System

* Sends automated notifications for:

  * Shortlisting
  * Selection
  * Rejection

---

## 4. System Architecture

The system follows a multi-stage pipeline:

1. Job descriptions are uploaded or entered manually
2. LLM extracts structured job data
3. Resumes are uploaded in bulk
4. Text extraction and preprocessing are performed
5. Duplicate detection is applied using SHA-256 hashing
6. LLM extracts candidate information
7. Matching engine evaluates each candidate against each job
8. Scores and feedback are generated and stored
9. Results are displayed through a dashboard
10. Email notifications are triggered based on status updates

---

## 5. Technology Stack

### Backend

* Node.js
* Express.js

### Frontend

* EJS (Embedded JavaScript)
* HTML, CSS, JavaScript

### Database

* MongoDB (with Mongoose ODM)

### AI Integration

* Cohere Command R+ Large Language Model

### Document Processing

* pdf-parse (PDF processing)
* textract (DOCX processing)

### Email Service

* Nodemailer (SMTP-based email delivery)

---

## 6. Matching Algorithm

The final score is computed as:

Score = (0.40 × Skills) + (0.30 × Experience) + (0.20 × Domain Fit) + (0.10 × Overall)

* Score range: 0 to 100
* Matching threshold: Score ≥ 50

Each candidate-job pair is evaluated independently, and results are stored with corresponding feedback.

---

## 7. Advantages

* Reduces manual effort in resume screening
* Enables scalable processing of large datasets
* Provides consistent and explainable evaluation
* Supports identification of candidates for multiple roles
* Prevents duplicate data processing
* Improves efficiency in recruitment workflows

---

## 8. Limitations

* Does not include interview scheduling or background verification
* Does not integrate with external Applicant Tracking Systems (ATS)
* Potential bias may still exist due to underlying LLM training data

---

## 9. Future Enhancements

* Integration with Applicant Tracking Systems
* Interview scheduling module
* Bias detection and fairness auditing mechanisms
* Advanced analytics and reporting dashboard
* Real-time job market insights

---

## 10. Contributors

* K. Teja Sri
* M. Akhila Sai
* B. Komali
* L. Rishitha

---

## 11. Academic Context

This project was developed as part of the Bachelor of Technology in Computer Science and Engineering (Artificial Intelligence and Data Science) at Shri Vishnu Engineering College for Women during the academic year 2025–2026 

---


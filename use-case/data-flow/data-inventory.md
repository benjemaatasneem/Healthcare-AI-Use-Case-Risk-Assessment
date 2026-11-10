olle ce contenu
Markdown
# Healthcare Data Inventory
 
## 1. Purpose
 
This document identifies and classifies the data that may be processed by the fictional Generative AI Medical Report Summarization Assistant.
 
The objective is to support data minimization, privacy, security, access control and retention decisions before deployment.
 
## 2. Data Inventory
 
| Data Category | Example | Personal Data | Health Data | Sensitivity | Purpose | Recommended Control |
|---|---|---:|---:|---|---|---|
| Patient identifier | Internal patient ID | Yes | No | High | Link the report to the correct patient | Replace direct identifiers with a pseudonymous internal ID |
| Patient identity | Name and surname | Yes | No | High | Patient identification | Remove before transmission to the AI service whenever possible |
| Date of birth | 15 March 1980 | Yes | Potentially | High | Patient identification and clinical context | Use age range instead of full date when sufficient |
| Contact information | Email, phone number, address | Yes | No | High | Administrative communication | Exclude from the AI input |
| Medical history | Previous conditions and consultations | Yes | Yes | Critical | Provide clinical context | Encrypt, restrict access and minimize input |
| Diagnosis | Diabetes, asthma or cancer diagnosis | Yes | Yes | Critical | Medical report summarization | Process only in an approved enterprise environment |
| Test results | Blood test or imaging results | Yes | Yes | Critical | Include clinically relevant information | Apply strict access and confidentiality controls |
| Prescriptions | Medication and dosage | Yes | Yes | Critical | Summarize current treatments | Require professional validation |
| Treatment information | Surgery, therapy or care plan | Yes | Yes | Critical | Summarize the patient's clinical situation | Encrypt and limit processing to necessary information |
| Medical report | Consultation or discharge report | Yes | Yes | Critical | Source document for the AI summary | Pseudonymize and restrict access |
| AI-generated summary | Preliminary report summary | Yes | Yes | Critical | Reduce administrative workload | Mark as AI-generated and require human review |
| User identity | Healthcare professional account | Yes | No | High | Authentication and accountability | MFA, RBAC and periodic access reviews |
| Prompt content | Instructions and medical text | Potentially | Potentially | Critical | Generate the requested summary | Filter, minimize and securely log prompts |
| AI response | Generated medical summary | Potentially | Potentially | Critical | Provide a preliminary summary | Validate before use and prevent automatic record insertion |
| Access logs | User, timestamp and accessed resource | Yes | Potentially | High | Security monitoring and auditability | Restrict access and define a retention period |
| Technical logs | Errors, processing time and system events | Potentially | Potentially | Medium to High | Performance and incident monitoring | Exclude medical content where possible |
| Security events | Failed logins or suspicious requests | Yes | Potentially | High | Detect attacks and misuse | Centralize monitoring and define alert thresholds |
 
## 3. Data Classification
 
The project uses the following classification levels:
 
### Public
 
Information that can be disclosed without causing harm.
 
No public patient or medical information is expected in this use case.
 
### Internal
 
Operational information intended only for authorized personnel.
 
Examples:
 
- General system documentation
- Non-sensitive technical instructions
- Internal process information
 
### Confidential
 
Information requiring restricted access.
 
Examples:
 
- Healthcare professional identities
- Access-control information
- System configurations
- Contractual information about the AI provider
 
### Critical
 
Information whose unauthorized disclosure, alteration or loss may significantly affect patients or the healthcare organization.
 
Examples:
 
- Medical reports
- Diagnoses
- Prescriptions
- Test results
- AI-generated medical summaries
- Prompts containing health information
 
## 4. Data Minimization Recommendations
 
The following information should be removed before transmission to the AI service unless strictly necessary:
 
- Patient name and surname
- Postal address
- Email address
- Phone number
- National or insurance identifier
- Exact date of birth
- Names of relatives
- Unnecessary administrative information
 
Where possible:
 
- replace the patient identity with a pseudonymous identifier;
- use an age range instead of the exact date of birth;
- submit only the relevant section of the medical report;
- exclude attachments not required for summarization;
- prevent users from entering unrelated personal information.
 
## 5. Access Requirements
 
| Role | Required Access | Prohibited Access |
|---|---|---|
| Healthcare professional | Submit authorized reports and validate summaries | Access records outside the professional's authorized scope |
| Medical records personnel | Access validated documents according to assigned duties | Modify clinical content without authorization |
| IT administrator | Maintain the technical platform | Use medical data for operational testing without authorization |
| Information Security team | Review security events and investigate incidents | Access clinical content unless required for an authorized investigation |
| Data Protection Officer | Review processing activities, risks and compliance evidence | Routine access to complete patient records |
| AI Governance team | Review the use case, controls and performance indicators | Access identifiable health information unless strictly required |
| AI service provider | Process the minimum technical input defined by contract | Reuse prompts or outputs for training or unrelated purposes |
 
## 6. Retention Principles
 
Retention periods must be validated by the Legal, Data Protection and Medical Records teams.
 
The following principles should apply:
 
- Source medical reports remain governed by healthcare record-retention requirements.
- AI-generated drafts should not be retained longer than necessary.
- Rejected or abandoned summaries should be deleted.
- Prompts should not be retained by the AI provider unless justified and contractually approved.
- Security logs should have a documented retention period.
- Data should be securely deleted when the retention period expires.
- Exceptions must be documented and approved.

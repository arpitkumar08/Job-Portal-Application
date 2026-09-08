# Job Portal & Application Management System

## 📌 Project Overview

The **Job Portal & Application Management System** is a web-based recruitment platform designed to simplify and manage the complete hiring workflow between **candidates, recruiters, and clients**.

The system allows recruiters to post job vacancies, candidates to create accounts and apply for jobs, and recruiters to manage applications on a job-wise basis. The platform also provides automated email notifications whenever an application's status changes.

The project is planned, scheduled, and monitored using **Microsoft Project**, including task duration, dependencies, resources, milestones, and budget estimation.

---

# 1. Scope and Objectives

## 1.1 Project Objective

The primary objective is to develop a centralized recruitment platform that manages the complete lifecycle of a job application.

The system will:

- Allow candidates to create accounts.
- Allow candidates to create and manage profiles.
- Allow candidates to upload resumes.
- Allow recruiters to create and publish job vacancies.
- Allow candidates to search and filter jobs.
- Allow candidates to apply for jobs.
- Allow recruiters to view applications job-wise.
- Allow recruiters to update application statuses.
- Automatically notify candidates through email.
- Allow recruiters to share candidate information with clients.
- Provide an administrative dashboard.
- Maintain organized candidate, job, client, and application data.

## 1.2 Project Scope

### Candidate

Candidates will be able to:

- Register and log in.
- Create and update their profile.
- Add education, skills, and experience.
- Upload resumes.
- Browse available jobs.
- Search and filter jobs.
- View job details.
- Apply for jobs.
- View submitted applications.
- Track application status.
- Receive email notifications.

### Recruiter

Recruiters will be able to:

- Register and log in.
- Create and manage recruiter profiles.
- Create job vacancies.
- Edit and delete job postings.
- View applicants for each job.
- Search and filter candidates.
- Review candidate profiles.
- Download candidate resumes.
- Update application status.
- Share candidate information with clients.

### Administrator

Administrators will be able to:

- Manage candidates.
- Manage recruiters.
- Manage clients.
- Manage job postings.
- Manage applications.
- Monitor application activity.
- View reports.
- Manage system data.

---

# 2. Application Status Workflow

The application will use predefined statuses to track candidates throughout the recruitment process.

```text
                    Candidate Applies
                           |
                           ↓
                 Application Submitted
                           |
                           ↓
                    Recruiter Review
                           |
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
         In Review      On Hold       Declined
             |
             ↓
         Shortlisted
             |
             ↓
          Selected
```

## Application Statuses

| Status | Description |
|---|---|
| Submitted | Application has been successfully submitted |
| In Review | Recruiter is currently reviewing the application |
| On Hold / Pending | Application is temporarily placed on hold |
| Shortlisted | Candidate has been shortlisted |
| Selected | Candidate has been selected |
| Declined | Candidate has not been selected |

Every important status change will be recorded and the candidate will receive an appropriate email notification.

---

# 3. Email Notification System

The system will send automated emails to candidates based on application status.

### Application Submitted

**Subject:** Application Submitted Successfully

The candidate receives confirmation that the application has been successfully submitted.

### In Review

**Subject:** Application Under Review

The candidate is informed that the recruiter is reviewing the application.

### On Hold / Pending

**Subject:** Application Status Update

The candidate is informed that the application has temporarily been placed on hold.

### Shortlisted / Selected

**Subject:** Application Progress Update

The candidate is informed that they have progressed to the next stage.

### Declined

**Subject:** Application Status Update

The candidate is informed that the application was not selected.

---

# 4. Major System Modules

## 4.1 Authentication Module

- Candidate registration
- Recruiter registration
- Login
- Logout
- Password management
- Authentication
- Role-based access control

## 4.2 Candidate Management Module

- Candidate profile
- Personal information
- Education
- Skills
- Work experience
- Resume
- Contact information
- Profile updates

## 4.3 Job Management Module

- Create job
- Edit job
- Delete job
- Publish job
- Close job
- Job description
- Required skills
- Experience requirements
- Location
- Salary information
- Job type

## 4.4 Job Search Module

Candidates can search and filter jobs based on:

- Job title
- Skills
- Location
- Experience
- Job type
- Salary
- Category

## 4.5 Application Management Module

- Apply for a job
- View applications
- Job-wise applications
- Candidate-wise applications
- Application status
- Application history
- Resume access
- Candidate filtering

## 4.6 Candidate Status Management

Recruiters can update candidate status:

```text
Submitted
    ↓
In Review
    ↓
Shortlisted
    ↓
Selected
```

Alternative paths:

```text
In Review → On Hold
In Review → Declined
On Hold → In Review
```

## 4.7 Client Management Module

- Create client
- Update client
- View client
- Assign jobs to clients
- Share candidate profiles
- Share resumes
- Track candidate submissions

## 4.8 Notification Module

The notification system will manage:

- Application confirmation
- Status change notifications
- Shortlisting notifications
- Selection notifications
- Decline notifications
- Recruitment updates

## 4.9 Admin Module

The administrator dashboard may display:

```text
Total Candidates
Total Recruiters
Total Clients
Total Jobs
Active Jobs
Total Applications
Applications In Review
Shortlisted Candidates
Selected Candidates
Declined Applications
```

---

# 5. Overall System Workflow

```text
Recruiter
    |
    ↓
Create Job
    |
    ↓
Publish Job
    |
    ↓
Candidate Searches Job
    |
    ↓
Candidate Applies
    |
    ↓
Application Stored
    |
    ↓
Recruiter Reviews Application
    |
    ↓
Update Application Status
    |
    ↓
Email Notification
    |
    ↓
Candidate Receives Update
    |
    ↓
Candidate Shortlisted
    |
    ↓
Candidate Information Shared With Client
    |
    ↓
Client Reviews Candidate
```

---

# 6. Proposed Database Structure

## Main Entities

```text
User
Candidate
Recruiter
Client
Job
Application
Resume
ApplicationStatus
Notification
EmailLog
```

## Basic Entity Relationship

```text
User
 |
 ├──────── Candidate
 |
 └──────── Recruiter
              |
              ↓
             Job
              |
              ↓
        Application
              |
              ↓
          Candidate
```

A candidate can apply for multiple jobs, and a job can have multiple applications.

---

# 7. Resource Persons

The project will require the following resources:

| Resource | Responsibility |
|---|---|
| Project Manager | Planning, scheduling, monitoring, and coordination |
| UI/UX Designer | User interface and user experience design |
| Frontend Developer | Candidate, recruiter, and admin interfaces |
| Backend Developer | APIs, authentication, and business logic |
| Database Developer | Database design and management |
| QA Tester | Testing and quality assurance |
| DevOps Engineer | Deployment and server configuration |

For a student project, one team member may perform multiple roles.

---

# 8. Technology Stack

## Frontend

- React.js
- Vite
- HTML5
- CSS3
- JavaScript
- Tailwind CSS

## Backend

- Node.js
- Express.js

## Database

- MongoDB

## Authentication

- JWT
- HTTP-only Cookies

## Email

- Nodemailer
- SMTP / Email Service

## File Storage

- Cloudinary or equivalent cloud storage

## Development Tools

- Visual Studio Code
- Git
- GitHub
- Postman
- Figma

## Project Management

- Microsoft Project

---

# 9. Project Timeline

The project schedule shown below follows the **Microsoft Project schedule** prepared for this project.

**Project Start:** 04 September 2026  
**Project Finish:** 18 December 2026

## 9.1 High-Level Schedule

| Phase | Duration | Start | Finish | Predecessor | Resource |
|---|---:|---|---|---:|---|
| Project Planning | 5 days | 04-Sep-2026 | 10-Sep-2026 | — | Project Manager |
| Requirement Analysis | 13 days | 11-Sep-2026 | 29-Sep-2026 | 1 | Project Manager |
| UI/UX | 7 days | 30-Sep-2026 | 08-Oct-2026 | 5 | UI/UX Designer |
| Database Design | 10 days | 09-Oct-2026 | 22-Oct-2026 | 13 | Database Designer |
| Backend | 15 days | 23-Oct-2026 | 12-Nov-2026 | 21 | Backend Developer |
| Frontend | 15 days | 13-Nov-2026 | 03-Dec-2026 | 28 | Frontend Developer |
| Email Notification | 4 days | 04-Dec-2026 | 09-Dec-2026 | 36 | Backend Developer |
| Testing | 7 days | 10-Dec-2026 | 18-Dec-2026 | 53 | Tester |

> **Note:** The predecessor numbers above correspond to the detailed task IDs in the Microsoft Project WBS, not necessarily the visible summary-task numbers.

## 9.2 Detailed WBS

### 1. Project Planning

- Define project scope
- Define objectives
- Identify stakeholders
- Identify resources
- Prepare project plan

**Duration:** 5 days  
**Start:** 04-Sep-2026  
**Finish:** 10-Sep-2026

### 2. Requirement Analysis

- Candidate requirements
- Recruiter requirements
- Client requirements
- Admin requirements
- Functional requirements
- Non-functional requirements
- Requirement approval

**Duration:** 13 days  
**Start:** 11-Sep-2026  
**Finish:** 29-Sep-2026

### 3. UI/UX

- User flow
- Wireframes
- Candidate interface
- Recruiter interface
- Admin dashboard
- Job listing interface
- Application interface
- Responsive design

**Duration:** 7 days  
**Start:** 30-Sep-2026  
**Finish:** 08-Oct-2026

### 4. Database Design

- Identify entities
- Create ER diagram
- Define relationships
- Create database schema
- Implement database structure

**Duration:** 10 days  
**Start:** 09-Oct-2026  
**Finish:** 22-Oct-2026

### 5. Backend Development

- Backend setup
- Database connection
- Authentication
- Candidate APIs
- Recruiter APIs
- Client APIs
- Job APIs
- Application APIs
- Application status management
- Notification APIs
- Email integration
- Resume handling
- Candidate sharing
- Admin APIs

**Duration:** 15 days  
**Start:** 23-Oct-2026  
**Finish:** 12-Nov-2026

### 6. Frontend Development

#### Candidate Portal

- Registration
- Login
- Dashboard
- Profile
- Resume
- Job listing
- Job search
- Job details
- Apply
- Application tracking

#### Recruiter Portal

- Dashboard
- Job posting
- Job management
- Applicant management
- Candidate filtering
- Status management
- Client management
- Candidate sharing

#### Admin Portal

- Dashboard
- User management
- Job management
- Application management
- Reports

**Duration:** 15 days  
**Start:** 13-Nov-2026  
**Finish:** 03-Dec-2026

### 7. Email Notification

- Configure email service
- Application confirmation email
- In-review email
- On-hold email
- Shortlisted/selected email
- Declined email
- Test email delivery

**Duration:** 4 days  
**Start:** 04-Dec-2026  
**Finish:** 09-Dec-2026

### 8. Testing

- Unit testing
- Integration testing
- API testing
- System testing
- UI testing
- Security testing
- Responsive testing
- Email testing
- Bug fixing

**Duration:** 7 days  
**Start:** 10-Dec-2026  
**Finish:** 18-Dec-2026

---

# 10. Project Milestones

| Milestone | Target Date |
|---|---|
| Project Planning Completed | 10-Sep-2026 |
| Requirements Finalized | 29-Sep-2026 |
| UI/UX Completed | 08-Oct-2026 |
| Database Design Completed | 22-Oct-2026 |
| Backend Completed | 12-Nov-2026 |
| Frontend Completed | 03-Dec-2026 |
| Email Notification Completed | 09-Dec-2026 |
| Testing Completed | 18-Dec-2026 |
| **Project Completed** | **18-Dec-2026** |

---

# 11. Project Budget

The following is the estimated project budget used for project planning.

## 11.1 Human Resource Cost

| Resource | Daily Rate | Estimated Days | Cost |
|---|---:|---:|---:|
| Project Manager | ₹800 | 20 | ₹16,000 |
| UI/UX Designer | ₹700 | 10 | ₹7,000 |
| Frontend Developer | ₹1,000 | 30 | ₹30,000 |
| Backend Developer | ₹1,000 | 30 | ₹30,000 |
| QA Tester | ₹700 | 15 | ₹10,500 |
| DevOps Engineer | ₹800 | 5 | ₹4,000 |
| **Total Labour Cost** | | | **₹97,500** |

## 11.2 Other Project Costs

| Item | Estimated Cost |
|---|---:|
| Domain | ₹1,000 |
| Hosting | ₹5,000 |
| Database | ₹2,000 |
| Email Service | ₹2,000 |
| Development Tools | ₹2,000 |
| Miscellaneous | ₹3,000 |
| **Total Other Costs** | **₹15,000** |

## 11.3 Total Estimated Budget

```text
Human Resource Cost       ₹97,500
Other Project Costs       ₹15,000
----------------------------------
Subtotal                  ₹1,12,500

Contingency (10%)         ₹11,250
----------------------------------
Total Estimated Budget    ₹1,23,750
```

**Estimated Project Budget: ₹1,23,750**

---

# 12. Project Deliverables

The project will produce the following deliverables:

1. Project proposal
2. Requirement specification
3. Microsoft Project schedule
4. Work Breakdown Structure (WBS)
5. Gantt chart
6. Resource sheet
7. Budget estimation
8. UI/UX designs
9. Database design
10. ER diagram
11. System architecture
12. Backend APIs
13. Frontend application
14. Email notification system
15. Admin dashboard
16. Testing documentation
17. Deployment setup
18. User documentation
19. Final project report
20. Final presentation

---

# 13. Risks and Mitigation

| Risk | Impact | Mitigation |
|---|---|---|
| Requirement changes | High | Finalize requirements early |
| Development delays | High | Track progress using MS Project |
| Email delivery failure | Medium | Use a reliable email service |
| Data loss | High | Maintain regular database backups |
| Security vulnerabilities | High | Use authentication and input validation |
| Server downtime | Medium | Use reliable hosting |
| API integration issues | Medium | Test APIs independently |
| Scope creep | High | Maintain the defined project scope |
| Testing delays | Medium | Test modules during development |

---

# 14. Functional Requirements

The system should:

- Allow users to register and authenticate.
- Allow candidates to manage their profiles.
- Allow candidates to upload resumes.
- Allow recruiters to create and manage jobs.
- Allow candidates to search for jobs.
- Allow candidates to apply for jobs.
- Store application information.
- Allow recruiters to view candidates job-wise.
- Allow recruiters to update application status.
- Send automated email notifications.
- Allow recruiters to share candidate information with clients.
- Allow administrators to manage users, jobs, and applications.

---

# 15. Non-Functional Requirements

## Performance

The system should provide fast responses under normal usage.

## Security

The system should protect:

- User credentials
- Candidate personal information
- Resumes
- Client information
- Application information

## Availability

The system should remain available during normal service operation.

## Scalability

The architecture should support an increasing number of candidates, jobs, recruiters, and applications.

## Usability

The interface should be simple and easy to understand for candidates and recruiters.

## Maintainability

The application should use modular architecture and maintainable code.

---

# 16. Future Enhancements

Future versions may include:

- AI-based candidate-job matching
- AI resume screening
- Automated candidate ranking
- Interview scheduling
- Video interviews
- WhatsApp notifications
- SMS notifications
- Advanced recruitment analytics
- Job recommendation system
- Resume parsing
- AI-powered job description generation
- Calendar integration
- Online assessments
- Candidate skill testing

---

# 17. Success Criteria

The project will be considered successful when:

- Candidates can successfully create accounts.
- Candidates can complete their profiles.
- Candidates can upload resumes.
- Recruiters can create and publish jobs.
- Candidates can search and apply for jobs.
- Recruiters can manage applications job-wise.
- Recruiters can update application statuses.
- Candidates receive appropriate email notifications.
- Recruiters can share candidate information with clients.
- Administrators can manage users, jobs, and applications.
- The system passes functional and integration testing.
- The application can be deployed successfully.
- The project is completed within the planned schedule.

---

# 18. Microsoft Project Management

**Microsoft Project** will be used to plan and monitor the project.

The project file will contain:

- Work Breakdown Structure (WBS)
- Task duration
- Start and finish dates
- Task dependencies
- Predecessors
- Resource allocation
- Resource costs
- Task costs
- Milestones
- Gantt chart
- Project baseline
- Progress tracking
- Critical path

### Project Schedule Summary

```text
Project Start  : 04-Sep-2026
Project Finish : 18-Dec-2026

Major Phases:

Planning
   ↓
Requirement Analysis
   ↓
UI/UX
   ↓
Database Design
   ↓
Backend Development
   ↓
Frontend Development
   ↓
Email Notification
   ↓
Testing
   ↓
Project Completion
```

---

# 19. Conclusion

The **Job Portal & Application Management System** provides a centralized solution for managing the recruitment lifecycle from job posting to candidate selection.

The platform connects **candidates, recruiters, and clients** while reducing manual recruitment activities through centralized application management and automated email notifications.

The project will be managed using **Microsoft Project**, with a planned schedule from **04 September 2026 to 18 December 2026**. The project plan includes scope definition, resource allocation, task scheduling, dependencies, milestones, duration analysis, and budget estimation.

The system can later be enhanced with AI-powered recruitment features such as resume screening, candidate-job matching, automated ranking, and intelligent recommendations.

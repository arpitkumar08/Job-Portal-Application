# Job Portal & Application Management System

## 📌 Project Overview

The **Job Portal & Application Management System** is a web-based recruitment platform designed to simplify and manage the complete hiring workflow between **candidates, recruiters, and clients**.

The system allows recruiters to post job vacancies, candidates to create accounts and apply for jobs, and recruiters to manage applications on a job-wise basis. The platform also provides automated email notifications whenever an application's status changes.

The project is planned and monitored using **Microsoft Project**, including Work Breakdown Structure (WBS), task duration, dependencies, resources, milestones, Gantt chart, and budget estimation.

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

### Client / Recruiter

Clients or recruiters will be able to:

- Access the recruitment system.
- Create and manage job postings.
- View applicants for each job.
- Search and filter candidates.
- Review candidate profiles.
- Access candidate resumes.
- Manage candidate applications.
- Update application status.
- Share suitable candidate information.
- Track recruitment activities.

---

# 2. Application Status Workflow

The application will use predefined statuses to track candidates throughout the recruitment process.

```text
Candidate Applies
       |
       v
Application Submitted
       |
       v
Recruiter Review
       |
       +----------------+----------------+
       |                |                |
       v                v                v
   In Review         On Hold          Declined
       |
       v
   Shortlisted
       |
       v
    Selected
```

## Application Statuses

| Status | Description |
|---|---|
| Submitted / Successful | Application has been successfully submitted |
| In Review | Recruiter is currently reviewing the application |
| On Hold / Pending | Application is temporarily placed on hold |
| Shortlisted | Candidate has been shortlisted |
| Selected | Candidate has been selected |
| Declined | Candidate has not been selected |

Every important status change will be recorded and the candidate will receive an appropriate email notification.

---

# 3. Email Notification System

The system will send automated emails to candidates based on application status.

### Successful

**Subject:** Application Submitted Successfully

The candidate receives confirmation that the application has been successfully submitted.

### In Review

**Subject:** Application Under Review

The candidate is informed that the recruiter is reviewing the application.

### On Hold

**Subject:** Application Status Update

The candidate is informed that the application has temporarily been placed on hold.

### Declined

**Subject:** Application Status Update

The candidate is informed that the application was not selected.

---

# 4. Major System Modules

## 4.1 Authentication Module

- Candidate registration
- Client/recruiter authentication
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
    |
    v
In Review
    |
    v
Shortlisted
    |
    v
Selected
```

Alternative paths:

```text
In Review -> On Hold
In Review -> Declined
On Hold -> In Review
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

# 5. Overall System Workflow

```text
Client / Recruiter
        |
        v
    Create Job
        |
        v
    Publish Job
        |
        v
Candidate Searches Job
        |
        v
 Candidate Applies
        |
        v
Application Stored
        |
        v
Recruiter Reviews Application
        |
        v
Update Application Status
        |
        v
 Email Notification
        |
        v
Candidate Receives Update
        |
        v
Candidate Shortlisted
        |
        v
Candidate Information Shared With Client
        |
        v
Client Reviews Candidate
```

---

# 6. Proposed Database Structure

## Main Entities

- User
- Candidate
- Client
- Job
- Application
- Resume
- ApplicationStatus
- Notification
- EmailLog

## Basic Entity Relationship

```text
User
 |
 +-------- Candidate
 |
 +-------- Client
              |
              v
             Job
              |
              v
        Application
              |
              v
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
| Frontend Developer | Candidate, client, and admin interfaces |
| Backend Developer | APIs, authentication, and business logic |
| Database Designer | Database design and management |
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

The project schedule follows the **Microsoft Project schedule** shown in the project Gantt chart.

**Project Start:** 04 September 2026  
**Project Finish:** 18 December 2026

## 9.1 High-Level Schedule

| Phase | Duration | Start | Finish | Predecessor | Resource |
|---|---:|---|---|---:|---|
| Project Planning | 5 days | 04-Sep-2026 | 10-Sep-2026 | - | Project Manager |
| Requirement Analysis | 13 days | 11-Sep-2026 | 29-Sep-2026 | 1 | Project Manager |
| UI/UX | 7 days | 30-Sep-2026 | 08-Oct-2026 | 5 | UI/UX Designer |
| Database Design | 10 days | 09-Oct-2026 | 22-Oct-2026 | 13 | Database Designer |
| Backend | 15 days | 23-Oct-2026 | 12-Nov-2026 | 21 | Backend Developer |
| Frontend | 15 days | 13-Nov-2026 | 03-Dec-2026 | 28 | Frontend Developer |
| Email Notification | 4 days | 04-Dec-2026 | 09-Dec-2026 | 36 | Backend Developer |
| Testing | 7 days | 10-Dec-2026 | 18-Dec-2026 | 53 | Tester |

> **Note:** The predecessor values correspond to the detailed task IDs in the Microsoft Project WBS.

---

# 10. Detailed Work Breakdown Structure (WBS)

## 1. Project Planning

**Duration:** 5 days  
**Start:** 04-Sep-2026  
**Finish:** 10-Sep-2026  
**Resource:** Project Manager

Tasks:

- Define project scope
- Define objective
- Prepare project plan

---

## 2. Requirement Analysis

**Duration:** 13 days  
**Start:** 11-Sep-2026  
**Finish:** 29-Sep-2026  
**Resource:** Project Manager

Tasks:

- Candidate requirement
- Client requirement
- Application workflow
- Email notification requirements
- Database design requirements
- Functional requirement
- Non-functional requirement

---

## 3. UI/UX

**Duration:** 7 days  
**Start:** 30-Sep-2026  
**Finish:** 08-Oct-2026  
**Resource:** UI/UX Designer

Tasks:

- User flow
- Candidate wireframe
- Client wireframe
- Job list
- Job details
- Application page
- Application tracking

---

## 4. Database Design

**Duration:** 10 days  
**Start:** 09-Oct-2026  
**Finish:** 22-Oct-2026  
**Resource:** Database Designer

Tasks:

- Candidate database
- Client database
- Job database
- Application database
- Application status
- Notification database

---

## 5. Backend Development

**Duration:** 15 days  
**Start:** 23-Oct-2026  
**Finish:** 12-Nov-2026  
**Resource:** Backend Developer

Tasks:

- Authentication
- Candidate API
- Client API
- Job API
- Application API
- Notification API
- API testing

### Backend Task Schedule

| Task | Duration | Start | Finish | Predecessor |
|---|---:|---|---|---:|
| Authentication | 2 days | 23-Oct-2026 | 26-Oct-2026 | 21 |
| Candidate API | 5 days | 27-Oct-2026 | 02-Nov-2026 | 29 |
| Client API | 4 days | 27-Oct-2026 | 30-Oct-2026 | 29 |
| Job API | 2 days | 03-Nov-2026 | 04-Nov-2026 | 30,31 |
| Application API | 1 day | 05-Nov-2026 | 05-Nov-2026 | 32 |
| Notification | 3 days | 06-Nov-2026 | 10-Nov-2026 | 33 |
| API Testing | 2 days | 11-Nov-2026 | 12-Nov-2026 | 34 |

---

## 6. Frontend Development

**Duration:** 15 days  
**Start:** 13-Nov-2026  
**Finish:** 03-Dec-2026  
**Resource:** Frontend Developer

### Candidate Module

- Registration
- Login
- Profile
- Resume
- Job Listing
- Job Search
- Application for Apply
- Application History
- Notification

### Client Module

- Dashboard
- Post Job
- Manage Job
- Candidate Filtering
- Update Candidate Status

### Frontend Task Schedule

| Task | Duration | Start | Finish | Predecessor |
|---|---:|---|---|---:|
| Registration | 1 day | 13-Nov-2026 | 13-Nov-2026 | 37 |
| Login | 1 day | 16-Nov-2026 | 16-Nov-2026 | 38 |
| Profile | 3 days | 17-Nov-2026 | 19-Nov-2026 | 39 |
| Resume | 2 days | 20-Nov-2026 | 23-Nov-2026 | 40 |
| Job Listing | 1 day | 24-Nov-2026 | 24-Nov-2026 | 41 |
| Job Search | 1 day | 24-Nov-2026 | 24-Nov-2026 | 41 |
| Application for Apply | 2 days | 25-Nov-2026 | 26-Nov-2026 | 42,43 |
| Application History | 2 days | 27-Nov-2026 | 30-Nov-2026 | 44 |
| Notification | 3 days | 01-Dec-2026 | 03-Dec-2026 | 45 |

### Client Module

| Task | Duration | Start | Finish | Predecessor |
|---|---:|---|---|---:|
| Dashboard | 3 days | 13-Nov-2026 | 17-Nov-2026 | 36 |
| Post Job | 2 days | 18-Nov-2026 | 19-Nov-2026 | 48 |
| Manage Job | 2 days | 20-Nov-2026 | 23-Nov-2026 | 49 |
| Candidate Filtering | 1 day | 24-Nov-2026 | 24-Nov-2026 | 50 |
| Update Candidate Status | 2 days | 25-Nov-2026 | 26-Nov-2026 | 51 |

---

## 7. Email Notification

**Duration:** 4 days  
**Start:** 04-Dec-2026  
**Finish:** 09-Dec-2026  
**Resource:** Backend Developer

Tasks:

- Successful application notification
- In-review notification
- On-hold notification
- Declined notification

### Email Task Schedule

| Task | Duration | Start | Finish | Predecessor |
|---|---:|---|---|---:|
| Successful | 1 day | 04-Dec-2026 | 04-Dec-2026 | 36 |
| In-Review | 1 day | 07-Dec-2026 | 07-Dec-2026 | 54 |
| On-Hold | 1 day | 08-Dec-2026 | 08-Dec-2026 | 55 |
| Declined | 1 day | 09-Dec-2026 | 09-Dec-2026 | 56 |

---

## 8. Testing

**Duration:** 7 days  
**Start:** 10-Dec-2026  
**Finish:** 18-Dec-2026  
**Resource:** Tester

Tasks:

- Unit Testing
- Security Testing
- Integration Testing
- Email Testing

### Testing Task Schedule

| Task | Duration | Start | Finish | Predecessor |
|---|---:|---|---|---:|
| Unit Testing | 2 days | 10-Dec-2026 | 11-Dec-2026 | 58 |
| Security Testing | 2 days | 14-Dec-2026 | 15-Dec-2026 | 59 |
| Integration Testing | 1 day | 16-Dec-2026 | 16-Dec-2026 | 60 |
| Email Testing | 2 days | 17-Dec-2026 | 18-Dec-2026 | 61 |

---

# 11. Project Milestones

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
| Project Completed | 18-Dec-2026 |

---

# 12. Project Budget

## 12.1 Human Resource Cost

| Resource | Daily Rate | Estimated Days | Cost |
|---|---:|---:|---:|
| Project Manager | ₹800 | 20 | ₹16,000 |
| UI/UX Designer | ₹700 | 10 | ₹7,000 |
| Frontend Developer | ₹1,000 | 30 | ₹30,000 |
| Backend Developer | ₹1,000 | 30 | ₹30,000 |
| QA Tester | ₹700 | 15 | ₹10,500 |
| DevOps Engineer | ₹800 | 5 | ₹4,000 |
| **Total Labour Cost** | | | **₹97,500** |

## 12.2 Other Project Costs

| Item | Estimated Cost |
|---|---:|
| Domain | ₹1,000 |
| Hosting | ₹5,000 |
| Database | ₹2,000 |
| Email Service | ₹2,000 |
| Development Tools | ₹2,000 |
| Miscellaneous | ₹3,000 |
| **Total Other Costs** | **₹15,000** |

## 12.3 Total Estimated Budget

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

# 13. Project Deliverables

The project will produce the following deliverables:

- Project proposal
- Requirement specification
- Microsoft Project schedule
- Work Breakdown Structure (WBS)
- Gantt chart
- Resource sheet
- Budget estimation
- UI/UX designs
- Database design
- ER diagram
- System architecture
- Backend APIs
- Frontend application
- Email notification system
- Admin dashboard
- Testing documentation
- Deployment setup
- User documentation
- Final project report
- Final presentation

---

# 14. Risks and Mitigation

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

# 15. Functional Requirements

The system should:

- Allow users to register and authenticate.
- Allow candidates to manage their profiles.
- Allow candidates to upload resumes.
- Allow clients/recruiters to create and manage jobs.
- Allow candidates to search for jobs.
- Allow candidates to apply for jobs.
- Store application information.
- Allow recruiters to view candidates job-wise.
- Allow recruiters to update application status.
- Send automated email notifications.
- Allow candidate information to be shared with clients.
- Allow administrators to manage users, jobs, and applications.

---

# 16. Non-Functional Requirements

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

The architecture should support an increasing number of candidates, jobs, clients, and applications.

## Usability

The interface should be simple and easy to understand for candidates and clients/recruiters.

## Maintainability

The application should use modular architecture and maintainable code.

---

# 17. Future Enhancements

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

# 18. Success Criteria

The project will be considered successful when:

- Candidates can successfully create accounts.
- Candidates can complete their profiles.
- Candidates can upload resumes.
- Clients/recruiters can create and publish jobs.
- Candidates can search and apply for jobs.
- Recruiters can manage applications job-wise.
- Recruiters can update application statuses.
- Candidates receive appropriate email notifications.
- Candidate information can be shared with clients.
- Administrators can manage users, jobs, and applications.
- The system passes functional and integration testing.
- The application can be deployed successfully.
- The project is completed within the planned schedule.

---

# 19. Microsoft Project Management

**Microsoft Project** will be used to plan and monitor the project.

The Microsoft Project file will contain:

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

## Project Schedule Summary

```text
Project Start  : 04-Sep-2026
Project Finish : 18-Dec-2026

Planning
   |
   v
Requirement Analysis
   |
   v
UI/UX
   |
   v
Database Design
   |
   v
Backend Development
   |
   v
Frontend Development
   |
   v
Email Notification
   |
   v
Testing
   |
   v
Project Completion
```

---

# 20. Conclusion

The **Job Portal & Application Management System** provides a centralized solution for managing the recruitment lifecycle from job posting to candidate selection.

The platform connects **candidates, recruiters, and clients** while reducing manual recruitment activities through centralized application management and automated email notifications.

The project is scheduled from **04 September 2026 to 18 December 2026** and is managed using **Microsoft Project**. The project plan includes scope definition, resource allocation, task scheduling, dependencies, milestones, duration analysis, Gantt chart, and budget estimation.

The system can later be enhanced with AI-powered recruitment features such as resume screening, candidate-job matching, automated ranking, and intelligent recommendations.

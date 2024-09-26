# HireNepal
## 1. Project Summary:
HireNepal will be a platform connecting freelancers in Nepal with clients looking to hire for short-term or long-term projects. It will allow freelancers to showcase their skills, bid on jobs, and get hired, while clients can post jobs, review freelancer profiles, and manage projects.

## 2. Core Features:
### User Roles:
- Client (Employer): Can post jobs, review bids, hire freelancers, and manage projects.
- Freelancer: Can create profiles, showcase skills, search for jobs, bid on projects, and get hired.
- Primary Features for Freelancers:
Profile creation (personal info, skills, portfolio, certifications, reviews).
Browse and search for jobs by category, price, location (remote or local).
Bid on job listings with proposal details.
In-app messaging with clients.
Get paid via the platform (integrate payment gateways like eSewa or Khalti).
Job history (past projects and earnings).
- Primary Features for Clients:
Post jobs/projects with detailed descriptions.
Review freelancer profiles and portfolios.
Accept or reject bids from freelancers.
Rate freelancers and leave reviews after project completion.
Manage payments to freelancers through the platform.
- Common Features:
Job categories (web development, writing, design, etc.).
Advanced search filters (budget, skills, location).
Real-time notifications (job updates, messages, etc.).
Dashboard for managing projects, bids, and earnings.
Dispute resolution system.
User reviews and ratings.
## 3. Database Schema (Core Models):
User Model:
role (client or freelancer)
name
email
password
location (city, region)
profile_picture
description
skills (for freelancers)
rating
reviews_count
- Job Model:
title
description
budget_min (minimum budget)
budget_max (maximum budget)
deadline
status (open, in-progress, completed, closed)
client_id (belongs to User as a client)
category (e.g., IT, writing, design)
Bid Model:
freelancer_id (belongs to User as a freelancer)
job_id (belongs to Job)
proposal (text)
amount
status (pending, accepted, rejected)
- Payment Model:
job_id (belongs to Job)
freelancer_id
amount
status (pending, paid)
- Message Model:
sender_id
receiver_id
content
job_id
- Review Model:
rating (1-5 stars)
comment
freelancer_id
client_id
job_id
## 4. Tech Stack:
- Backend:
* Ruby on Rails: A good fit for quick development and has built-in tools to handle MVC architecture.
* Database: PostgreSQL for handling complex queries and scalability.
- API: Use RESTful API or GraphQL for communication between frontend and backend (if planning a SPA frontend).
- Frontend:
* HTML/CSS/JavaScript: For simple frontend with server-side rendering via Rails.
* Vue.js or React: For building a modern, interactive user experience.
* Bootstrap: For quick and responsive UI development.
- Payments:
Integration with local payment gateways like eSewa or Khalti for Nepal-specific payments.
International payments via PayPal or Stripe (optional for later expansion).
- Authentication:
Use Devise gem for user authentication (including email confirmation, password recovery).
JWT tokens for API-based authentication (if planning to separate frontend).
## 5. User Flow:
- Client Workflow:
Sign Up/Login: Create an account, verify email.
- Post Job: Fill out job details (title, description, budget, skills required).
- Review Bids: Review incoming bids from freelancers.
- Hire Freelancers: Accept a bid, communicate via in-app messaging.
- Manage Project: Track progress, set milestones.
- Complete and Pay: Pay freelancer upon job completion.
- Freelancer Workflow:
- Sign Up/Login: Create an account, set up profile, list skills.
- Search Jobs: Browse or search jobs by category, location, budget.
- Submit Bids: Bid on jobs with a proposal and estimated cost.
- Communicate: Message clients directly for clarifications.
- Work and Get Paid: Complete the job and receive payments through the platform.
## 6. Admin Panel:
Admin dashboard to manage users, job postings, disputes, payments.
Ability to moderate content (reviews, bids, projects).
Generate platform earnings reports (e.g., percentage commission on transactions).
## 7. Revenue Model:
- Commission-Based: Take a percentage commission from every job completed (e.g., 10-15% from freelancers).
- Subscription Plans: Offer premium plans for freelancers (e.g., premium visibility, more bids).
- Job Posting Fees: Charge clients a small fee to post jobs.
## 8. MVP Development Phases:
- Phase 1 (Core Features):
User sign-up/login.
Freelancer profiles and job posting.
Bidding system.
In-app messaging.
Payment integration.
Job completion and reviews.
- Phase 2 (Advanced Features):
Admin dashboard.
Notifications (via email/SMS).
Advanced search filters for jobs and freelancers.
User reviews and rating system.
- Phase 3 (Optional Features):
Dispute resolution.
Freelancer verification (upload certificates, etc.).
Analytics dashboard for freelancers (job insights, earnings tracking).
## 9. Launch and Marketing:
Focus on marketing through social media, targeting both freelancers and clients within Nepal.
Use SEO and content marketing to attract organic traffic.
Consider partnering with local businesses or events to promote the platform.

# SkillBarter AI — Campus Skill Exchange Platform

A peer-to-peer learning platform for Mahindra University that enables students to exchange knowledge through a credit-based system. Students can teach skills, discover courses, book learning sessions, and earn credits by sharing their expertise.

*Live Demo:* https://skill-barter-v5w5.onrender.com

## Team

*Team name:* CiphEra

### Members

* V. Raghavendra — @ragh000987-cyber
* G. Dhiren Reddy — @Dhiren00
* Anantha Dheeraj Reddy — @dheeraj62811
* M. Sampath Kumar — @sampath2007mandadi-cmyk
* MAREDDY ROOPCHANDAN REDDY — @roopchandan
* A. Aswin Kumar — @aswin-12341234

## Problem

Students possess different academic strengths and technical skills, but finding someone who can teach a specific subject within their university can be difficult.

Traditional learning platforms often focus on courses provided by institutions or paid instructors. They do not always offer a simple way for students to exchange their knowledge directly with their peers.

Students need a platform where they can discover mentors, share their expertise, find learning opportunities, and identify skills that are in demand on  campus.

## Solution

SkillBarter AI is a campus-based peer-to-peer learning platform designed for Mahindra University students.

The platform creates a collaborative learning ecosystem where students can teach what they know and learn what they want through a credit-based exchange system.

### Key Features

* *University Email Validation:* Restricts the login workflow to email addresses accepted by the application's university-email validation logic.
* *Course Listings:* Allows students to publish courses they can teach and skills they want to learn.
* *Credit System:* Provides new students with two welcome credits and supports credit-based course bookings.
* *Course Discovery:* Displays courses offered by other students.
* *Session Booking:* Allows students to book learning sessions and specify a meeting slot.
* *Escrow-Style Credit Handling:* Holds credits when a session is booked and transfers them to the mentor after successful OTP verification.
* *OTP Verification:* Uses a four-digit code to verify session completion.
* *Email Notifications:* Sends booking information and the session verification code to the mentor when email delivery is configured.
* *Skill Demand Analytics:* Compares the number of students requesting skills with the number of students offering them.
* *Student Dashboard:* Provides information about courses offered, desired skills, credits, and learning sessions.

### How It Helps

SkillBarter AI encourages students to become both teachers and learners. By exchanging knowledge instead of relying exclusively on paid learning resources, students can discover new skills while contributing to their campus community.

## Technologies used

* *Python* — Application programming language.
* *Flask* — Web application framework and backend API.
* *HTML* — Web page structure through Flask templates.
* *CSS* — Web interface styling.
* *JavaScript* — Client-side interactions and communication with backend APIs.
* *Python Standard Library* — Email handling, random OTP generation, and time-related functionality.
* *Gmail SMTP over SSL* — Mentor email notifications.
* *Gunicorn* — Production WSGI server.
* *Render* — Web application deployment.
* *Git and GitHub* — Version control and source code hosting.

## How to run

### Prerequisites

Install the following before running the project locally:

* Python 3.10 or a compatible version.
* Git.
* pip, the Python package installer.

### 1. Clone the repository

bash
git clone https://github.com/dheeraj62811/skill_barter.git


### 2. Navigate to the project directory

bash
cd skill_barter


### 3. Create a virtual environment

bash
python -m venv venv


Activate the environment.

*Windows:*

bash
venv\Scripts\activate


*Linux or macOS:*

bash
source venv/bin/activate


### 4. Install dependencies

bash
pip install -r requirements.txt


### 5. Configure email notifications

The application uses Gmail SMTP to notify mentors about course bookings.

Set the following environment variables if you want to enable email delivery.

*Windows Command Prompt:*

cmd
set SENDER_GMAIL=your_gmail@gmail.com
set SENDER_APP_PASSWORD=your_gmail_app_password


*Linux or macOS:*

bash
export SENDER_GMAIL="your_gmail@gmail.com"
export SENDER_APP_PASSWORD="your_gmail_app_password"


Replace the example values with your actual Gmail address and Google-generated App Password.

Never commit email credentials or other secrets to GitHub.

Email notification functionality requires valid credentials and a working SMTP connection.

### 6. Start the application

bash
python app.py


The application starts on port 5000 by default.

Open the following address in your browser:

http://127.0.0.1:5000

### Production deployment

The application is deployed on Render.

*Live application:* https://skill-barter-v5w5.onrender.com

The repository includes a requirements.txt file containing the Python dependencies.

## Demo

*Live Website:* https://skill-barter-v5w5.onrender.com

*GitHub Repository:* https://github.com/dheeraj62811/skill_barter

The live application demonstrates a campus skill-exchange workflow, including course publishing, course discovery, credit-based bookings, session verification, and skill-demand analytics.

## Notes

* *In-memory storage:* The current backend stores user and session information in Python dictionaries and lists. Data is not permanently saved and may be lost when the application restarts.
* *Email configuration:* Mentor notifications require correctly configured Gmail credentials and a working SMTP connection.
* *University email validation:* The current validation checks accepted email-domain suffixes; it does not independently verify student enrollment.
* *Credit handling:* The application implements an escrow-style workflow in which credits are deducted during booking and transferred after OTP verification. It is an application-level mechanism rather than a banking or financial escrow service.
* *Future improvements:* Potential enhancements include persistent database storage, stronger authentication, improved session security, course recommendations, student ratings, and more detailed learning analytics.

---

*CiphEra — Learn Together. Share Knowledge. Grow Together.

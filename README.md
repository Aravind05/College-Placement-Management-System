# 🎓 College Placement Management System

A full-stack, multi-portal web application designed to streamline and automate campus placement drives, candidate management, job applications, and real-time recruitment analytics.

---

## 🚀 Key Portals & Architecture

The system is structured around four interconnected portals ensuring seamless separation of concerns between administrators, recruiters, and candidates:

1. **Candidates Portal (`demo.html`)**: Manages student profile directories, academic credentials, branch specifications, and live placement statuses.
2. **Job Portal (`apply.html`)**: Allows students to browse active company job drives and submit applications based on eligibility criteria (CGPA, backlogs, package).
3. **Recruiter Portal (`company.html`)**: Enables companies to register, post new placement openings, review candidate applications, and update statuses (*Shortlisted*, *Selected*, *Rejected*).
4. **Analytics Dashboard (`analytics.html`)**: Provides real-time KPI metrics, active drive counts, live application logs with instant search filtering, and **CSV Report Export** functionality.

---

## 🛠️ Tech Stack

* **Frontend**: HTML5, Modern CSS, Bootstrap 5, JavaScript (ES6+ Asynchronous Data Handling).
* **Backend & Database**: Supabase (Backend-as-a-Service), PostgreSQL.
* **Icons & Styling**: FontAwesome 6, Custom Responsive Gradients.

---

## 💡 Technical Highlights & Problem Solving

* **Client-Side Data Mapping Architecture**: Bypassed complex and fragile relational SQL joins by fetching raw data tables (`Student`, `job`, `company`, `application`) independently using asynchronous `Promise.all` requests and mapping them securely in JavaScript.
* **Robust Foreign Key & Constraint Handling**: Resolved PostgreSQL case-sensitivity constraints and strict relational schema blocks by configuring flexible client-side foreign key lookups and decoupled table updates.
* **Real-Time Synchronization**: Instant state propagation where recruiter actions (e.g., marking a student as *Selected*) automatically trigger database flags (`is_placed = true`) and instantly update analytics metrics and candidate badges.

---

## ⚙️ Setup & Installation

1. Clone or download this project repository to your local machine.
2. Ensure you have an active internet connection to load the external CDN dependencies (Bootstrap, FontAwesome, Supabase JS Client).
3. Open any of the entry HTML files (`demo.html`, `apply.html`, `company.html`, or `analytics.html`) directly in any modern web browser or via a local development server (like VS Code's *Live Server* extension).
4. The system connects out-of-the-box to the configured Supabase backend instance.

---

## 📸 Project Preview

* **Dashboard Analytics & Search**: Features real-time counters for total candidates, placed students, active drives, and instantaneous keyword filtering.
* **Recruiter Controls**: One-click status management allowing fast tracking of interview pipelines.
*
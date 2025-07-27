# Web-Security-Scanner 🛡️

A full-stack web application designed for comprehensive security assessments of websites. This project allows users to perform various security checks and analyze reports to identify potential vulnerabilities.

✨ Description
Web Security Scanner is an automated tool built to provide preliminary security assessments of web applications. It focuses on gathering critical reconnaissance information and actively testing for common web vulnerabilities. The goal is to provide transparent, detailed, and actionable security reports, enhancing a user's understanding of their website's security posture.

📸 Screenshots
(Example: You would insert actual screenshots here, like the dashboard, a report page, etc.)

Screenshot of the interactive dashboard
<img width="1919" height="906" alt="web-app" src="https://github.com/user-attachments/assets/d16f2b51-e692-43bd-b0e2-b50e1d15b51f" />

Screenshot of a detailed scan report with findings
<img width="724" height="839" alt="image" src="https://github.com/user-attachments/assets/5486b64b-77aa-4eb7-b7e3-a44f15f12cc3" />
<img width="721" height="839" alt="image" src="https://github.com/user-attachments/assets/9e6d4786-50fc-4af8-9375-0d93e070ecb2" />

Key Features
Automated Information Gathering: Conducts passive reconnaissance to collect vital data including WHOIS information, DNS records (A, AAAA, MX, NS, TXT), SSL/TLS certificate details, open ports, discovered subdomains (via crt.sh), HTTP security headers, cookie analysis, and tech stack fingerprinting.

Vulnerability Testing: Actively tests for common web application vulnerabilities such as SQL Injection, Cross-Site Scripting (XSS), Open Redirect, and Directory Traversal.

Vulnerable JavaScript Library Detection: Identifies known vulnerabilities in client-side JavaScript frameworks and libraries.

Interactive Dashboard: Features a modern, intuitive dashboard summarizing scan statistics, overall security scores, graphical trends of scans over time, and a filterable/sortable scan history table.

Transparent Reporting: Generates detailed HTML reports accessible via the web interface. Provides a comprehensive "Active Tests Performed" log, explicitly showing the success or error status of every module executed during a scan.

Historical Vulnerability Tracking: Compares current scan results against previous completed scans for the same URL, highlighting newly found issues, resolved vulnerabilities, and still-present risks for continuous monitoring.

Robust Error Handling & Fallbacks: Implements intelligent error reporting for external service failures (e.g., timeouts from crt.sh, connection issues). Includes a resilient fallback to a basic Python socket-based port scan if the Nmap executable is not available or encounters issues.

Flexible Report Exports: Allows downloading detailed scan reports in multiple formats: PDF, CSV, and JSON.

Tech Stack 🛠️
Frontend: EJS (No, this is from the example project. It should be Flask's Jinja2 templating for HTML), HTML, CSS, JavaScript, Bootstrap, Chart.js, date-fns (for time formatting).

Backend: Python, Flask, Flask-SQLAlchemy, multiprocessing (for background tasks).

Database: SQLite (managed via SQLAlchemy).

APIs & Libraries: requests (for HTTP requests), python-nmap (for port scanning, with socket fallback), python-whois (for WHOIS lookups), dnspython (for DNS lookups), builtwith (for tech stack fingerprinting), xhtml2pdf (for PDF report generation).

Getting Started
Follow these instructions to get a local copy of the project up and running for development and testing.

Prerequisites
Make sure you have the following installed on your system:

Python 3.x (includes pip)

Git

Optional (for full Nmap features): Nmap (install the Nmap executable for your OS).

Installation & Setup
Clone the repository:

Bash

git clone https://github.com/YourGitHubUsername/YourRepoName.git # Replace with your actual repo URL
cd YourRepoName # Replace with your actual repo directory name (e.g., Web-Scanner-App)
Create and activate a Python virtual environment:

Bash

python -m venv venv
.\venv\Scripts\activate   # On Windows PowerShell
# source venv/bin/activate # On Linux/macOS Bash
Install Node.js dependencies: (No, this is from the example. It should be Python dependencies)
Install Python dependencies: This installs all required packages like Flask, SQLAlchemy, requests, etc.

Bash

pip install -r requirements.txt
Running the Application 🚀
You need to run your Flask application server.

Start the Flask Server:
Open your terminal/command prompt, navigate to the project directory, and run:

Bash

python app.py
(Note: The first time you run it, the SQLite database file instance/scans.db will be automatically created in your project directory.)

Access the application:
Open your web browser and go to the URL provided in the terminal, typically:
http://127.0.0.1:5000

How to Use
Navigate to the application URL in your browser.

In the "Start a New Scan" section, enter the URL of the website you wish to scan (e.g., https://example.com).

Click "Scan Now". The scan will run in the background.

Once the scan is complete (status changes from "Pending" to "Completed" on the dashboard), click "View Report" next to the scan entry.

Explore the detailed report, including active tests, findings, and comparison with previous scans.

Use the "Download PDF," "Download CSV," or "Download JSON" buttons to export the report.

Deployment (Making it Live)
To make your Web Security Scanner a live, publicly accessible website, you'll need to deploy it to a Platform-as-a-Service (PaaS) provider.

Recommended Host: PythonAnywhere (offers a free tier suitable for hobby projects).

Database Note: For a multi-user public application, it's recommended to migrate from SQLite to a more robust database like PostgreSQL or MySQL in a cloud environment.

WSGI Server: On deployment, your application will be served by a production WSGI server (like Gunicorn) instead of Flask's development server.

Author & Acknowledgements 🤝
This project was developed by [Your Name] as part of [Your Course/Curriculum/Initiative, if any].

[Your Name] - GitHub: [YourGitHubUsername]

License
Distributed under the MIT License. See LICENSE for more information.

🔐 OWASP Top 10 2025:IAAA Failures(TryHackMe) 
🧠 1. Introduction
This room focuses on failures in the IAAA model:
Identity
Authentication
Authorization
Accountability
These are core security pillars. If any fails → attackers can:
Access other users’ data
Gain admin privileges
Stay undetected

🧩 2. What is IAAA?
Identity, Authentication, Authorisation, Accountability
🔍 Explanation:
Component	Meaning	Example
Identity	Who you claim to be	Username
Authentication	Proving identity	Password / OTP
Authorization	What you can access	Admin vs User
Accountability	Tracking actions	Logs

🚨 3. A01: Broken Access Control (Authorization Failure)
💡 Concept
Occurs when users can access data/actions they shouldn’t.
Common issues:
IDOR (Insecure Direct Object Reference)
Privilege escalation
Missing access checks

🧪 TryHackMe Tasks + Answers
❓ Q1:If you can view another user’s data without role change → what escalation?
✅ Answer:Horizontal Privilege Escalation

❓ Q2:Flag from millionaire account?
✅ Answer:THM{Found.the.Millionare!}

❓ Q3:Admin dashboard flag?
✅ Answer:THM{Account.confusion.FTW!}

🧠 Key Understanding:
Horizontal → user → another user
Vertical → user → admin

🔑 4. A07: Authentication Failures
💡 Concept
Weak login/authentication mechanisms.
Common issues:
Weak passwords
No rate limiting
Username enumeration
Poor session handling

🧪 TryHackMe Tasks
Scenario:Logs show multiple login attempts.
❓ Q1:What type of attack?
✅ Answer:Brute Force Attack

❓ Q2:Attacker IP?
✅ Answer:49.99.13.16

🧠 Key Understanding:
Attackers try many passwords → exploit weak authentication

📊 5. A09: Logging & Alerting Failures (Accountability Failure)
💡 Concept
When systems fail to log or detect attacks
Problems:
No logs
Missing details (who, when, where)
No alert system
Logs can be tampered
🧪 TryHackMe Learning
Scenario:System logs show suspicious activity
Key Tasks:
Analyze logs
Identify attack patterns
Detect anomalies

🧠 Key Understanding:
Without logs:
Attacks go unnoticed
No forensic investigation
No accountability

🔗 6. Mapping IAAA → OWASP Categories
IAAA Component	OWASP 2025 Category
Authorization	A01: Broken Access Control
Authentication	A07: Authentication Failures
Accountability	A09: Logging & Monitoring Failures
👉 These 3 are the core of this room

⚔️ 7. Real Attack Flow (Important for Exam)
Attacker logs in (Authentication weakness)
Accesses another user’s data (Authorization failure)
No logs generated (Accountability failure)
➡️ Full system compromise

🛡️ 8. Prevention (VERY IMPORTANT)
🔒 Access Control
Enforce server-side checks
Use RBAC (Role-Based Access Control)
🔑 Authentication
Strong passwords
MFA (Multi-Factor Authentication)
Rate limiting
📊 Logging
Log all critical actions
Monitor logs (SIEM)
Alert on suspicious activity

🧾 9. Final Summary (Exam Ready)
IAAA = Identity + Authentication + Authorization + Accountability
OWASP categories covered:
A01 → Broken Access Control
A07 → Authentication Failures
A09 → Logging Failures
Main attacks:
Privilege escalation
Brute force
Undetected intrusions
Main defense:
Strong auth + proper access control + logging





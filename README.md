Sample format
******
1. Header
Lab name (exact PortSwigger title)
Category (e.g., SQL Injection, XSS, Access Control)
Difficulty (Apprentice / Practitioner / Expert)
Link to the lab

2. Objective
One or two sentences — what does the lab ask you to achieve (e.g., "retrieve the administrator's password via a blind SQL injection using conditional responses").

3. Recon / Initial Observations
What you noticed poking around — endpoints, parameters, cookies, error messages, app behavior. This is often the most valuable part for your own learning since it shows how you found the vector, not just the final payload.

4. Vulnerability Identification
The specific flaw and why it exists (e.g., unsanitized input concatenated into a SQL query).

5. Exploitation Steps
Numbered, reproducible steps — requests sent, payloads used, tools (Burp Repeater/Intruder), and what changed in the response each time. Include the actual payloads in code blocks.

6. Proof of Success
Screenshot or the confirmation PortSwigger gives you ("Congratulations, you solved the lab").

7. Root Cause & Fix
A sentence or two on the underlying mistake and how it'd be remediated in real code (parameterized queries, output encoding, proper access control checks, etc.) — this is what separates a "walkthrough" from a genuine security writeup and is good practice for real bug bounty reports too.

8. Notes / Variations
Anything you tried that didn't work, or alternate ways to solve it — useful for your own reference later.

***************************


**1. Explain *why*, not just *how***
Anyone can copy the payload from PortSwigger's solution. What's rare is explaining the underlying mechanism — why does `' OR '1'='1` bypass this specific query, what does the database do internally, why does the WAF filter fail on this encoding. This was the explicit differentiator for the writer aiming for the Burp Suite Certified Practitioner exam — solving wasn't the goal, understanding why the solution worked was.

**2. Show your dead ends**
The polished "I did X, then Y, solved" narrative hides the real skill: how you got there. Document the payloads that *didn't* work and why, the wrong hypothesis you tested first, the moment you misread a response. This is what makes a writeup useful to someone actually stuck, versus just a solution key.

**3. Go one level deeper than the lab asks**
- Try to solve it a second way (e.g., manual SQLi after doing it with Burp's scanner)
- Ask "how would this look in real code" and sketch the vulnerable snippet yourself
- Ask "what would the fix look like" and write the patched version
- Try to break your own fix

**4. Automate something**
Writing a small Python/Bash script to reproduce the exploit (rather than just clicking through Burp) makes the writeup concrete and reusable, and shows a different skill than "I followed the UI." Several of the more technical repos include scripts alongside the writeup for exactly this reason.

**5. Add a "real world" angle**
Tie the lab to a real CVE, breach, or bug bounty report that used the same class of vulnerability. This turns a lab exercise into a piece of context that shows you understand where this fits in actual security work, not just an academic exercise.

**6. Develop a consistent voice/structure**
Ironically, uniqueness partly comes from consistency — a signature format, section headers, a recurring "root cause" section, maybe a personal rating of difficulty vs PortSwigger's official one. Readers start recognizing your style across posts, which is what separates a portfolio from a pile of disconnected writeups.

**7. Write for a specific reader**
Decide who it's for — future-you revising for a cert, a hiring manager, other learners stuck on the same lab — and let that shape depth and tone. "Explaining to a beginner" and "notes for my own exam prep" produce very different (and more focused) posts than trying to cover everyone.


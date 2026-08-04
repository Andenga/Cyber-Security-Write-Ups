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
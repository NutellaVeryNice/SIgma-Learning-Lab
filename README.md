Sigma Learning Lab 🛡️

Welcome to the Sigma Learning Lab — a hands-on portfolio of curated custom Sigma detection rules aimed at demonstrating threat detection techniques, sharing detection logic, and refining alerting strategies.
 
📖 Overview
This repository contains Sigma rules that span multiple use cases aligned to real-world attack scenarios:

📅 Detection Categories
• HomoglyphRelatedRules/ – Detects domain and URL impersonation attempts using homoglyphs (e.g., Latin vs Cyrillic characters).
• BruteForce/ – Flags brute-force authentication attempts across different platforms.
• DefenseEvasion/ – Detects common methods used to disable or evade endpoint and network defenses.
• Phishing/ - Detects spearphishing emails containing potential malicious link indicators.
• Phishing/SuspiciousFileOpen/ – Targets suspicious file operations tied to email-based phishing attacks.

Each rule is:
• Written in Sigma YAML format
• Tagged with relevant MITRE ATT&CK techniques
• Labeled with metadata (title, id, author, level, etc.) for consistency and portability
 
🤖 Purpose
This lab serves as:
• A Detection Engineering Showcase
Build credibility by demonstrating structured detections for known threat patterns.
• A SIEM Rule Development Playground
Easily export rules to Splunk, ElasticSearch, Sentinel (KQL), etc. via sigma-cli.
• A Learning Resource
Designed to help new SOC analysts or aspiring detection engineers understand how good rules are structured.
 
🚀 Get Started

1.  Clone the Repo
git clone https://github.com/NutellaVeryNice/SIgma-Learning-Lab.git
2.  Install Sigma CLI
pip install sigma-cli
3.  Validate All Rules
sigma validate HomoglyphRelatedRules/ BruteForce/ DefenseEvasion/ Phishing/SuspiciousFileOpen/
4.  Convert a Rule to a SIEM Query (Optional)
sigma convert -t splunk BruteForce/example-rule.yml
sigma convert -t es-qs Phishing/SuspiciousFileOpen/rule.yml
 
📊 Contribution Guidelines

While this repository is currently personal and curated, I warmly welcome:

• Suggestions for improvement
• Detection logic reviews
• Conversations around threat hunting ideas

In the future, I may open contribution via pull requests. Feedback is always appreciated via LinkedIn or GitHub Discussions.
 
🤝 Let’s Connect

If you’re a recruiter, SOC lead, or fellow detection engineer, feel free to reach out!
• LinkedIn: www.linkedin.com/in/wong-shih-ning-b57087222
• GitHub: NutellaVeryNice

If this project helped you in learning or building, don’t forget to give it a star ⭐ :)
 
📄 License
MIT License © 2025 — See LICENSE for full terms.

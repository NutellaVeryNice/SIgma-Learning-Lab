# Sigma Learning Lab 🛡️

A curated collection of custom **Sigma detection rules** to showcase threat-hunting patterns and hone your alerting strategies.

---

## 📘 Repo Overview

This repository contains Sigma rules organized into key detection categories:

- **HomoglyphRelatedRules/** – Detects domain or URL impersonation using homoglyphs (e.g., Cyrillic “о” vs Latin “o”).
- **BruteForce/** – Detects brute-force login attempts across various platforms.
- **DefenseEvasion/** – Identifies attempts to disable or evade security tools.
- **Phishing/SuspiciousFileOpen/** – Flags suspicious file operations commonly seen in phishing attacks.

Every rule uses clear metadata (`title`, `id`, `author`, `date`, `level`, `tags`), making them easy to integrate into SIEM systems or use as test cases.

---

## 🤖 Why This Matters

- **Threat-Hunting Ready**  
  Each rule maps to known attack behaviors (e.g., MITRE ATT&CK tactics), perfect for analysts refining detection pipelines.

- **Sigma-Native Format**  
  Written in standard YAML—portable and convertible across Splunk, Elastic, Kusto (Azure Sentinel), etc.

- **Testbed for Security Tools**  
  Ideal for engineers and security teams to test rule parsing, correlation engines, or ingestion pipelines.

---

## 🚀 Usage Guide

1. Clone this repository:
   ```bash
   git clone https://github.com/NutellaVeryNice/SIgmaTestRules.git
   ```

2. Validate rules using [sigma-cli](https://github.com/SigmaHQ/sigma-cli):
   ```bash
   pip install sigma-cli
   sigma validate HomoglyphRelatedRules/ BruteForce/ DefenseEvasion/ Phishing/SuspiciousFileOpen/
   ```

3. (Optional) Convert a rule to Kusto or Elastic:
   ```bash
   sigma convert --target kusto HomoglyphRelatedRules/example.yml
   sigma convert --target elasticsearch BruteForce/another-rule.yml
   ```

---

## 📈 How to Contribute

Contributions welcome! You can:

- Add new detection rules under existing or new folders.
- Propose improvements (names, detection logic, tags).
- Enable CI validation using `sigma-cli` or GitHub Actions.

Just fork the repo, add your files, and open a pull request. I’ll review it promptly.

---

## 🔗 Connect with Me

I’m always looking to connect with fellow security enthusiasts:

- **LinkedIn**: [@NutellaVeryNice](https://www.linkedin.com/in/your-profile)
- **GitHub**: [NutellaVeryNice](https://github.com/NutellaVeryNice)

Feel free to star ⭐ the project if it helps your learning or hunts!

---

## 📝 License

MIT License © 2025 — See [LICENSE](LICENSE) for details.

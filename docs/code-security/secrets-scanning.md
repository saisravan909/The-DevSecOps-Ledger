# Pre-Commit Secrets Detection

### The "Why"
Hardcoded credentials (like AWS keys or API tokens) in your code history are a primary cause of cloud breaches. Once a secret is pushed to GitHub, it is considered compromised.

### The "How"
Implement a tool like `gitleaks` or `trufflehog` as a "pre-commit hook." This stops the code from being saved if it looks like a password is inside it.

### Verification Step
Try to save a file with a fake key (e.g., `AKIAIMNOOIEARIEXAMPLE`). If the tool is working, it will block your save!

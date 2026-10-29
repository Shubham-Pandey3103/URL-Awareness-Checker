# EWB Phishing URL Awareness Checker

## Overview
Phishing is a trick that uses fake links or messages to persuade people to share private information. This beginner Python project checks URL text for a small set of visible warning signs. It does not open URLs or send data anywhere.

## Features
- Detects an `@` symbol in the URL
- Flags unusually long URLs (over 100 characters)
- Flags IP-address hostnames
- Flags hostnames with 5 or more segments
- Flags punycode-style hostnames (`xn--`)
- Flags the HTTP scheme
- Repeats checks until the user types `q`, `quit`, or `exit`
- Handles malformed URL text without crashing
- Shows a “REVIEW CAREFULLY” summary when warning signs are found

## Requirements
- Python 3.10 or later
- No extra packages are required

## How to Run
Open a terminal in this project folder.

**Windows**
```bash
python phishing_checker.py
```

If needed, try:
```bash
py phishing_checker.py
```

**macOS/Linux**
```bash
python3 phishing_checker.py
```

Enter one of the sample URLs from `tests/test_samples.md`. Type `q` to quit.

## Example Output
```text
EWB Phishing URL Awareness Checker
Text checks only - this program does not open URLs.

Enter a sample URL (or type q to quit): http://192.0.2.10/account

Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: 2 warning sign(s) found.
Never enter passwords from unexpected links.
```

## Testing
The five sample cases and the observed results are recorded in [`tests/test_samples.md`](tests/test_samples.md). Please run the samples on your own computer and update the Python version, operating system, date, and actual results to reflect your own run.

## Screenshots
After running the project on your computer, save genuine screenshots using these exact paths:
- `screenshots/sample_run.png`
- `screenshots/test_results.png`

The first screenshot should show the terminal command, sample URL, and output. The second should show the completed test table or evidence of all five test runs.

## Improvements
1. **Repeat checks with a quit command** — the user can check multiple sample URLs without restarting the program. Tested by entering more than one sample and then `q`.
2. **Malformed-input handling** — catches a `ValueError` from URL parsing and prints a clear message instead of crashing. Test with the workbook's malformed sample `http://[bad`.
3. **Review summary** — counts warning messages and displays a summary when warnings are present.

## Limitations
This is an educational tool. It only reads URL text. It does not visit URLs, scan for malware, query reputation services, or prove that a URL is safe. “No listed warning signs found” does **not** mean a URL is safe.

## Ethical Use
Use only the sample strings supplied in the workbook. Do not collect credentials, send phishing messages, or probe websites without written permission. Do not upload passwords, tokens, or confidential data to GitHub.

## Author
- Name: [Write your name]
- Batch/Course: [Write your internship batch/course]
- GitHub username: [Write your GitHub username]

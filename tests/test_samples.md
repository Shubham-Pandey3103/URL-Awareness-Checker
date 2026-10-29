# Test Results

Python version used: [Fill in your version, e.g. 3.13.1]  
Operating system: [Fill in Windows/macOS/Linux]  
Date: [Fill in the date you ran the tests]

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs; not a safety guarantee. | No listed warning signs found. This does NOT prove safety. | PASS |
| 2 | `http://192.0.2.10/account` | IP address + HTTP. | Uses an IP address instead of a familiar domain.; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3 | `http://example.com@sample.invalid/login` | @ symbol + HTTP. | Contains an @ symbol; inspect carefully.; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments. | Contains many hostname segments/subdomains. | PASS |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname. | Contains a punycode-style hostname. | PASS |

## Notes

- The program checks the URL as text only and never visits the link.
- The six checks are clues, not proof that a URL is malicious or safe.
- Re-run these samples on your own computer and confirm/update the actual results above.


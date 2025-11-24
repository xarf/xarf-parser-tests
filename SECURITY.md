# Security Policy

## Supported Versions

This test suite follows the XARF specification versioning:

| Version | Supported          |
| ------- | ------------------ |
| 4.x.x   | :white_check_mark: |
| 3.x.x   | :x:                |

## Reporting a Vulnerability

We take security seriously. If you discover a security issue in our test samples or test definitions, please report it responsibly.

### How to Report

**Please DO NOT report security vulnerabilities through public GitHub issues.**

Instead, report security vulnerabilities by:

1. **Email**: Send details to security@xarf.org
2. **Private Advisory**: Use GitHub's [private security advisory feature](https://github.com/xarf/xarf-parser-tests/security/advisories/new)

### What to Include

When reporting a vulnerability, please include:

- Description of the security concern
- Affected test samples or definitions
- Potential impact on parser implementations
- Any proof-of-concept or reproduction steps
- Your name/handle for credit (optional)

### Response Timeline

- **Acknowledgment**: Within 48 hours of report
- **Initial Assessment**: Within 5 business days
- **Status Updates**: Every 7 days until resolution
- **Fix Timeline**: Critical issues within 30 days

## Security Considerations for Test Samples

### Test Data Safety

All test samples in this repository:

1. **Anonymized Data**: No real personal or organizational information
2. **Safe Content**: No actual malicious payloads or exploits
3. **Synthetic Examples**: Generated or heavily sanitized data
4. **No Secrets**: No API keys, passwords, or authentication tokens

### Parser Security Testing

Test samples are designed to help parser implementations:

1. **Input Validation**: Test boundary conditions and edge cases
2. **Error Handling**: Verify graceful failure on malformed input
3. **Injection Prevention**: Include samples that test for injection vulnerabilities
4. **Resource Limits**: Test handling of large or deeply nested structures

### Known Security Patterns

Our invalid test samples specifically test for:

- Schema validation bypass attempts
- JSON injection patterns
- Malformed UTF-8 sequences
- Excessive nesting or recursion
- Resource exhaustion vectors

## Security Features

### Automated Checks

- **Dependency Review**: PR-based vulnerability scanning for GitHub Actions
- **Dependabot**: Automated updates for GitHub Actions
- **Secret Scanning**: Detects committed credentials (should never happen)

### Best Practices

When contributing test samples:

1. **Never include real data**: All samples must be synthetic or fully anonymized
2. **No executable content**: Test samples should be data only
3. **Document security tests**: Clearly label security-focused test cases
4. **Review carefully**: All PRs reviewed for security implications

## Contact

For security concerns or questions about this policy, contact: security@xarf.org

For general questions about test samples, use GitHub Issues.

---

**Note**: This is a test data repository. Security concerns here relate to the safety and appropriateness of test samples, not executable code vulnerabilities.

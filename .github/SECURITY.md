# 🔒 Security Policy

## 🛡️ Supported Versions

We release patches for security vulnerabilities. Which versions are eligible for receiving such patches depends on the CVSS v3.0 Rating:

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | :white_check_mark: |
| < 1.0   | :x:                |

## 🚨 Reporting a Vulnerability

The Dapr Init team takes security bugs seriously. We appreciate your efforts to responsibly disclose your findings, and will make every effort to acknowledge your contributions.

### Where to Report

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them to the maintainer [@mtnvencenzo](https://github.com/mtnvencenzo) or via email.

### What to Include

To help us better understand the nature and scope of the possible issue, please include as much of the following information as possible:

- 🎯 **Type of issue** (e.g., container escape, credential exposure, network vulnerability, etc.)
- 📁 **Service(s) affected** and version numbers
- 📍 **Location of the affected configuration** (file/line or direct reference)
- ⚙️ **Special configuration** required to reproduce the issue
- 🔄 **Step-by-step instructions** to reproduce the issue
- 💥 **Proof-of-concept or exploit code** (if possible)
- 🎯 **Impact of the issue**, including how an attacker might exploit the issue



## 🔐 Security Best Practices

### For Stack Users

- 🔄 **Keep Updated**: Always use the latest stable versions of Docker images
- 🔑 **Credential Management**: Use Docker secrets or environment variables for sensitive values, never commit secrets
- 🌐 **Network Security**: Implement proper network segmentation and access controls
- 📱 **Access Control**: Use principle of least privilege for container access
- 🏷️ **Image Pinning**: Pin image versions to avoid unexpected changes


## 📚 Additional Resources

- [Docker Security Best Practices](https://docs.docker.com/develop/security-best-practices/)
- [Dapr Security Documentation](https://docs.dapr.io/concepts/security-concept/)
- [Container Security Guidelines](https://kubernetes.io/docs/concepts/security/)

## 📋 Security Checklist

Our security measures include:

- ✅ **Container Scanning**: Automated security scanning of Docker images
- ✅ **Configuration Analysis**: Static analysis of Docker Compose configurations
- ✅ **Secrets Management**: No secrets in configuration files, proper environment variable handling
- ✅ **Access Control**: Services follow least privilege principles
- ✅ **Network Security**: Secure network configurations by default
- ✅ **Regular Updates**: Automated image and dependency updates
- ✅ **Configuration Validation**: Input validation and secure defaults

## 🔍 Service-Specific Security

### Container Security
- 🔒 **Image Security**: Use official images from trusted registries
- 🔐 **Runtime Security**: Run containers as non-root users where possible
- 🌐 **Network Isolation**: Proper network segmentation between services
- � **Resource Limits**: Set appropriate CPU and memory limits

### Dapr Security
- 🔑 **Data Security**: Secure transmission and storage of state and pub/sub data
- 🏷️ **Service Authentication**: Proper authentication between Dapr services
- 🌐 **Network Encryption**: Use TLS for service communication where applicable
- 📊 **Access Logging**: Enable audit logging for monitoring access

### Configuration Dependencies
- 🔄 **Image Versions**: Pin to specific versions for security fixes
- 📦 **Dependency Management**: Regular updates to Dapr runtime images
- 🔍 **Vulnerability Scanning**: Automated scanning for known vulnerabilities

---

**Thank you for helping keep our Dapr setup secure! 🛡️**
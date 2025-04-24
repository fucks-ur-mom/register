
# Welcome to the fucks-ur.mom Subdomain Registration Repository

This repository allows you to register your own subdomain under `fucks-ur.mom`. This is a fun, joke project where you can create and manage your own subdomains easily. Please follow the instructions carefully to register your subdomain.

## Project Overview

This project provides a simple way to register a subdomain by submitting a JSON file with your domain settings. Once your pull request is merged, your subdomain will be live!

## How to Register Your Subdomain

### 1. Star and Fork the Repository

- **Star** the repository to show your support.
- **Fork** the repository to make your own changes.

### 2. Create a New JSON File

- Inside the `/domains` folder, create a new JSON file. The file name should be the subdomain you want to register, like `example.json`. For instance, if you want a subdomain called `cool.domain.fucks-ur.mom`, create a file called `cool.domain.json`.

- The format of the JSON file should follow the template below:

### Example JSON Structure

```json
{
  "owner": {
    "username": "devmatei", 
    "email": "hello@example.com"
  },
  "record": {
    "A": ["1.1.1.1", "1.0.0.1"],
    "AAAA": ["::1", "::2"],
    "CNAME": "example.com",
    "MX": ["mx1.example.com", "mx2.example.com"],
    "TXT": ["example_verification=1234567890"],
    "CAA": [
      { "flags": 0, "tag": "issue", "value": "letsencrypt.org" },
      { "flags": 0, "tag": "issuewild", "value": "sectigo.com" }
    ],
    "SRV": [
      { "priority": 10, "weight": 60, "port": 5060, "target": "sipserver.example.com" },
      { "priority": 20, "weight": 10, "port": 5061, "target": "sipbackup.example.com" }
    ]
  },
  "proxied": false
}
```


### 3. Submit Your Pull Request

- **Review the Pull Request Checklist**: Ensure your JSON file is correctly formatted.
- **Submit your pull request**. If your pull request is not correctly formatted, it may be ignored.
- After submitting, **monitor your pull request** for any feedback or necessary changes.

### 4. Wait for Changes to Propagate

Once your pull request is merged, allow up to 24 hours for the changes to propagate. It usually takes between 5 to 15 minutes for DNS updates to go live, but sometimes it might take longer.

### 5. Enjoy Your New Domain!

Once your subdomain is live, you can use it however you wish. If you have any questions or run into issues, feel free to ask for help.

Happy domain registration! 🎉

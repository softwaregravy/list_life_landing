# List Life Landing Page

## Development
To test your website locally before deploying, use one of these methods:
Using Python (pre-installed on macOS):
```bash
# If you have Python 3
python3 -m http.server 8000
# Then visit http://localhost:8000 in your browser.

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```


## Deployment 

### Verify AWS CLI Installation and Configuration

First, check if AWS CLI is installed:
```bash
aws --version
```

If not installed, install using Homebrew:

```bash
brew install awscli
```

Check AWS CLI configuration:
```bash
aws configure list
```

If not configured, set up your AWS credentials:
```bash
aws configure
```

Verify S3 access:
```bash
aws s3 ls s3://list-life-landing-page
```

### Deploy Changes
To sync your local directory with the S3 bucket, run:
```bash
aws s3 sync . s3://list-life-landing-page --exclude ".git/*" --exclude "license.txt" --exclude "README.md"
```

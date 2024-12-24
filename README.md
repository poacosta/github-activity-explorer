# GitHub Activity Explorer 🔍

## A Data Science Journey Through Your GitHub History

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/username/repo/blob/main/github_activity_explorer.ipynb)

Ever wondered about your GitHub story? This Colab notebook turns your GitHub activity into a data science playground. Perfect for developers who love diving into data (and maybe procrastinating productively by analyzing their commit patterns 😉).

## What's This Notebook About?

This notebook is your personal archaeologist for GitHub activity - it digs through your commit history using the GitHub API and transforms raw data into delightful pandas DataFrames ready for exploration. Think of it as your personal data science playground where you can unearth patterns in your coding journey and draw your own conclusions about your developer story.

While I've crafted a guided expedition through your GitHub footprint, this notebook is ultimately your canvas. Feel free to fork, modify, or completely reimagine the analysis path - your insights, your rules!

## 🚀 Quick Start Guide

1. Click the "Open in Colab" button above
2. Get your GitHub token (Settings → Developer settings → Personal access tokens)
3. Set up your environment variables in Colab:

   ```python
   # Import ENV vars from Google Colab
   from google.colab import userdata

   # Set up parameters
   github_token = userdata.get('GITHUB_TOKEN')
   start_date = '2024-01-01'  # Beginning of your analysis period
   end_date = '2024-12-31'    # End of your analysis period
   ```

4. Let the data exploration begin!

💡 **Token Setup & Security:**

### 🔒 Read-Only Analysis

This tool is designed to be **100% read-only**. It will:

- ✅ Read your commit history
- ✅ Analyze repository metadata
- ✅ Access public organization data
- ❌ Never create commits
- ❌ Never modify repositories
- ❌ Never change any settings

### Required Permissions (Read-Only)

Your GitHub token needs only read access:

- `repo:status` and `public_repo` - Read-only access to repository data
  - Access commit status
  - Access public repositories
- `read:org` - Read-only access to organization data
  - View organization repository listings
- `read:user` - Read-only access to user profile data
  - Read user profile data

### Setting Up Your Token

1. Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Name your token (e.g., "GitHub Activity Explorer - Read Only")
4. Select ONLY the read permissions listed above
5. Set an expiration date (recommended: 30-90 days)

### Securing Your Token in Colab

- Store your token in Colab's secrets manager:
  1. Click the key 🔑 icon in the left sidebar
  2. Add a new secret named 'GITHUB_TOKEN'
  3. Paste your token value
  4. Toggle notebook access for secret 'GITHUB_TOKEN'
- Never hardcode tokens in your notebook
- Avoid sharing notebooks with token values exposed

### Pro Tips

- Create a dedicated read-only token for this analysis
- Regularly rotate your tokens
- Keep the minimum required permissions
- Consider shorter expiration periods for better security

## 📊 What Can You Explore?

### Core Analysis Features

- **Commit Patterns**: When do you code most? (Spoiler: probably right before deadlines)
- **Repository Impact**: Which repos have seen the most action?
- **Code Changes**: Track your lines of code (additions, deletions, and the eternal "why did I write this?")
- **Time Analysis**: Your coding schedule across different timezones (because git commits wait for no one)

### Data Science Goodies

- Clean pandas DataFrames ready for analysis
- Pre-built visualizations using popular libraries
- Extensible code for your own custom analysis
- Export capabilities for further exploration

## 📝 Pro Tips

- Start with recent data first (unless you really want to relive your first commits)
- Use the provided helper functions - they're your friends
- Add your own analysis cells - the more the merrier!

## 🤓 Fun Use Cases

- Track your most productive coding hours
- Generate activity reports for your portfolio
- Find patterns in your commit messages (how many times did you write "fix typo"?)

## 🎨 Customization

The notebook is your canvas! Feel free to:

- Add your favorite visualization libraries
- Create custom analysis functions
- Export data for use in other tools
- Share your insights with the community

## 📚 What You'll Learn

- Working with the GitHub API like a pro
- Data wrangling with pandas
- Time series analysis techniques
- Data visualization best practices
- And probably something about your coding habits you didn't know!

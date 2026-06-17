# Intellecap TA Copilot

A Streamlit Cloud-ready AI assistant for Talent Acquisition.

## What it does

- Screens resumes against a job description
- Generates fitment score and recommendation
- Creates 80-100 word stakeholder-ready candidate summary
- Highlights strengths and possible concerns
- Suggests interview questions
- Drafts hiring-manager update email
- Exports candidate comparison CSV and analysis ZIP

## Files

- `app.py` — Streamlit application
- `requirements.txt` — Python dependencies
- `.streamlit/config.toml` — basic UI configuration
- `sample_jd.txt` — sample JD for testing
- `.gitignore` — prevents secrets from being committed

## Deployment on Streamlit Community Cloud

1. Create a GitHub repository, for example: `intellecap-ta-copilot`
2. Upload these files to the repository.
3. Go to Streamlit Community Cloud and select **Create app**.
4. Choose your GitHub repository, branch, and entrypoint file: `app.py`.
5. Open **Advanced settings** and add your secret:

```toml
OPENAI_API_KEY = "your_api_key_here"
```

6. Click **Deploy**.

## Local testing

```bash
pip install -r requirements.txt
streamlit run app.py
```

For local testing, create `.streamlit/secrets.toml` with:

```toml
OPENAI_API_KEY = "your_api_key_here"
```

Do not commit `secrets.toml` to GitHub.

## Recommended first use case

Start with active hiring roles where resume screening and stakeholder summaries consume repeated HR time:
- Investment Banking
- ESG / sustainability consulting
- Rural development programs
- Finance / fund management
- Fundraising / investor relations

## HR Guardrails

This tool is AI-assisted and should not make final hiring decisions. HR and hiring managers should validate all outputs. Avoid using or inferring protected attributes such as age, gender, caste, religion, marital status, disability, or nationality.

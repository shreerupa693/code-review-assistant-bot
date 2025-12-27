# code-review-assistant-bot
Automatically reviews PRs for common issues
def analyze_request(pr_url):
 issues=[]
 if hardcoded_secrets(pr_code):
  issues.append({
  "type":"security",
  "message":"Hardcoded API keys detected",
  "severity":"high"
  })
  if cyclomatic_complexity(pr_code)>10:
   issues.append({
    "type":"maintainability",
    "message":"function too complex",
    "severity":"medium"
    })
  return generate_review_report(issues)

```markdown
# 🔐 Lambda Secret Rotate

This project rotates a secret (like a password) in **AWS Secrets Manager** using an AWS Lambda function.

---

## 📂 Files

- `lambda_function.py` – Lambda function code to generate a new password and update the secret.
- `policy.json` – IAM policy for the Lambda's role to access Secrets Manager and EC2 network permissions.

---

## ✅ What it does

1. Reads the existing secret from Secrets Manager.
2. Generates a new random password.
3. Updates the secret with the new password.

---

## 🛠 Setup

1. Replace `"SECRET_NAME"` and `"KEY_TO_ROTATE"` in `lambda_function.py`.
2. Create a Lambda function with this code.
3. Attach the IAM policy from `policy.json` to the Lambda’s role.
4. (Optional) Set up a CloudWatch schedule to trigger it automatically.


---

## 📌 Note

Make sure your secret has a key to update (e.g., `"password"`) and that your Lambda has network access if needed.

```

Take refrence from here 
https://youtu.be/_rUbHj_tJbY?si=z3G57tg9qnHrlq4H

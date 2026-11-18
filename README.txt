BANK EXAM MOCK TEST WEBSITE

Included:
- Candidate login: name, 10-digit Indian phone number, email
- 10 questions with options
- 15-minute countdown and automatic submission
- Manual submit confirmation
- Result summary and score
- EmailJS integration placeholders for sending results

IMPORTANT EMAIL NOTE
A static HTML website (including GitHub Pages) cannot securely send email by itself.
This project includes EmailJS browser integration, but email delivery will work only after
you configure your own EmailJS account.

SET UP EMAIL RESULTS
1. Create an account at https://www.emailjs.com/
2. Add an email service.
3. Create an email template with these template variables:
   {{to_email}}, {{admin_email}}, {{candidate_name}}, {{phone}}, {{score}},
   {{correct}}, {{incorrect}}, {{unanswered}}, {{time_used}}, {{details}}
4. Configure the template to send to {{to_email}}. Add {{admin_email}} as CC
   if you also want an administrator copy.
5. Open index.html and replace:
   YOUR_EMAILJS_PUBLIC_KEY
   YOUR_EMAILJS_SERVICE_ID
   YOUR_EMAILJS_TEMPLATE_ID
   YOUR_ADMIN_EMAIL@example.com
6. Upload index.html to GitHub Pages or any static web host.

SECURITY
- Do not place private API secrets in frontend code.
- EmailJS public key is intended for browser use; configure domain restrictions
  and email sending limits in your EmailJS dashboard.
- For high-stakes or official exams, use a backend to validate scores and prevent
  client-side answer tampering. This is a practice-test frontend.

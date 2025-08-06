# Cybersecurity-task-day2
Phishing Email Analysis
##  Sample Email Details

- **Subject**: SUJAIT S R, win $200 for 5 minutes of your time!
- **Sender Name**: Andrei from Novorésumé
- **Sender Email**: andrei@novoresume.net
- **Recipient**: 99220041055@klu.ac.in
- **Date**: July 10, 2025
- **Main URL in Email**: [https://tally.so/r/w2YZag?...](https://tally.so/r/w2YZag)
- **Attachment(s)**: None

---

##  Phishing Indicators Identified

1. **Too-Good-To-Be-True Offer**  
   - The email promises a chance to win a **$200 Amazon gift card** just for a 5-minute survey. This is a classic phishing tactic to lure the victim.

2. **Suspicious Tracking URLs**  
   - Links include very long UTM tracking parameters that mask their true destination. Example:
     ```
     https://tally.so/r/w2YZag?email=99220041055@klu.ac.in&utm_campaign=...
     ```

3. **Generic Survey Link & Urgency**  
   - Claims that the offer **expires soon** to pressure immediate action (social engineering).

4. **Spoofed Marketing Style**  
   - The sender appears to be legitimate, but domain `cioeu99889.novoresume.net` is **not the official Novorésumé website** — could be a spoofed subdomain.

5. **Header Analysis**  
   - `Return-Path`: postmaster@cioeu99889.novoresume.net  
   - **SPF**: Pass  
   - **DKIM**: Pass  
   - **DMARC**: Pass  
   > Although SPF/DKIM/DMARC passed, phishing emails can still pass these checks if sent from compromised or authorized third-party services.

6. **Marketing Disguised as Phishing**  
   - The email mimics legitimate newsletters but manipulates emotional triggers: winning money, fear of missing out, and personalization using recipient's name.

---

##  Tools Used

- 📬 Manual analysis of `.eml` content (email body + headers)
- 🔗 [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- 🔒 [VirusTotal](https://virustotal.com) (used to check URLs if needed)

---

## Files Included

- `SUJAIT_S_R_win_$200_email_sample.txt` – Raw email content extracted from `.eml`

---

##  Conclusion

Although the email appears to be a **legitimate marketing survey**, it contains multiple red flags common in **phishing and scam campaigns**:
- Overpromising incentives
- Generic marketing tone
- Potentially spoofed sender domains

⚠️ This kind of email should be flagged and reported if unsolicited.


# Phishing Email Detector

A simple web tool that scores how suspicious an email looks, from 0 to 10, and explains every reason behind the score. Everything runs in your browser. Nothing is uploaded.

**Live demo:** https://aakash2005ak17-hub.github.io/phishing-detector/

## How it works

You paste the sender and the message text. The page runs rule-based checks and adds points for each warning sign:

| Check | Points |
|---|---|
| Lookalike sender domain (for example `paypa1.com`) | +3 |
| Link text does not match where the link goes | +3 |
| Link uses a raw IP address | +3 |
| Pressure wording ("act now", "account locked") | +2 |
| Asks for passwords or card details | +2 |
| Display name and address do not match | +2 |
| Shortened link, link without HTTPS, generic greeting | +1 each |

Score meaning: 0 to 2 Probably safe, 3 to 5 Suspicious, 6 to 10 Likely phishing.

Each warning explains what was found, why it matters, and what to do. Suspicious results also play a warning animation and sound.

## Run it

Open `index.html` in any browser. No install needed.

## Limits

This is a learning project built on simple rules. It can miss real scams and can flag harmless emails. Do not use it as your only protection.

## Future improvements

- Check links against known bad-site lists
- Parse full email headers (SPF, DKIM, Reply-To)
- Upload `.eml` files directly
- Train a small machine learning model on real phishing samples

## Tech

HTML, CSS and plain JavaScript. No libraries.

# 🎯 I’ll Guess Your Job

> An interactive career field classifier built for the **UTM CC100 Reverse Career Fair** — March 26, 2026.

![Quiz Demo](https://img.shields.io/badge/Built%20For-UTM%20CC100-blue?style=flat-square) ![HTML](https://img.shields.io/badge/Tech-HTML%2FCS%2FJS-yellow?style=flat-square)

-----

## 💡 Overview

**I’ll Guess Your Job** is a single-page interactive quiz that predicts a user’s professional field based on 5 targeted questions. It was developed as a portfolio demonstration piece for the **UTM CC100 Reverse Career Fair**, showcasing core business and data analysis skills — specifically decision logic, classification thinking, and data-driven UX design.

Inspired by the viral “ladder career” format, the app engages employers and peers in a 60-second experience that opens conversations around data, career paths, and industry fit.

-----

## ✨ Features

- **5-question classifier** covering problem-solving style, work environment, data mindset, motivation, and personality
- **7 detectable career fields**: Tech/Software, Finance/Banking, Healthcare/Sciences, Consulting/Business, HR/People Ops, Sales/Marketing, Engineering/Operations
- **Confidence score** — dynamically calculated based on answer weight distribution, animated on reveal
- **Personality type + superpower** match tailored to each field
- **Live employer tags** — shows which companies at the fair hire for the predicted field
- **Confetti reveal** + shareable result text
- Fully responsive — works on mobile and desktop
- Zero dependencies — pure HTML, CSS, and vanilla JavaScript

-----

## 🧠 Skills Demonstrated

This project was built to reflect the thinking required in **Business Analysis** and **Data Analysis** roles:

|Skill                      |How It Appears in the Project                                |
|---------------------------|-------------------------------------------------------------|
|Classification logic       |Weighted scoring system maps answers to fields               |
|Data-driven decision making|Confidence score calculated from score distribution          |
|User research              |Questions designed around real behavioral/cognitive patterns |
|Stakeholder communication  |Results framed as insights, not just labels                  |
|UI/UX thinking             |Interface built for a high-energy, time-limited event context|

-----

## 🚀 Getting Started

No installation or dependencies required.

```bash
# Clone the repository
git clone https://github.com/YOUR-USERNAME/guess-your-job.git

# Open in browser
open guess-your-job.html
```

Or simply download `guess-your-job.html` and open it in any modern browser.

-----

## 🏗️ How It Works

Each of the 5 questions maps answer choices to a weighted scoring object across 7 fields:

```js
{ label: "Pull the data and find the root cause",
  fields: { tech: 2, finance: 2, consulting: 1, healthcare: 1 } }
```

After all 5 questions, scores are tallied and the highest-scoring field is selected as the prediction. The confidence percentage is derived from the ratio of the top score to the total possible score, normalized to a realistic range (55–98%).

```js
const confidence = Math.min(98, Math.round(55 + (topScore / totalScore) * 100));
```

-----

## 📁 File Structure

```
guess-your-job/
│
├── guess-your-job.html     # Complete self-contained app (HTML + CSS + JS)
└── README.md               # This file
```

-----

## 🎓 Context

This project was developed as part of **CC100 — Career Exploration and Development** at the **University of Toronto Mississauga (UTM)**. It was presented at the **March 26, 2026 Reverse Career Fair**, where students pitched themselves to employers across industries including finance, technology, healthcare, and consulting.

The quiz was used as an interactive conversation opener, connecting visitors with relevant employers at the fair based on their predicted field.

-----

## 🙋 Author

**[Minyoung Suk]**

-----

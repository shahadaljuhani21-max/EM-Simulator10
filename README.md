# EM Clinical Simulator — Three Deep-Dive Cases

## Deploy
Upload all files and folders at the root of your GitHub repository (index.html must be at root). Netlify: branch main, base directory blank, build command blank, publish directory `.`. This is a static app with no backend, build step or secrets.

## Features
- Three fictional EM cases: suspected inferior STEMI, severe asthma, VF cardiac arrest.
- Guided / Independent / Challenge modes.
- Five/4/4 staged decisions (13 total), 64 curated answer categories, keyword synonyms, basic negation checking and safety-first feedback.
- Simulated stage-by-stage patient vitals, action log and debrief.
- AI Case Pack Creator with copy/download prompt, exact JSON template and sample pack.
- JSON multi-case import with schema checks, local storage, export and delete.

## IMPORTANT LIMITATIONS
- This is an educational **prototype**. Patient-state progression is scripted and does not yet branch based on interventions. It does not provide genuine AI-based semantic understanding, robust medication-dose parsing, or all possible correct/incorrect answers. Complex or multiple-action answers can be misclassified. The result is a practice score, not a validated clinical competency measure.
- JSON structural validation does not verify medical correctness or citations. A qualified clinician must review cases, decision rules, contraindications, doses and guideline currency before instructional or clinical deployment.
- Cases use general guideline homepages as reading links, not a claim of point-by-point source verification.
- Imported cases are saved only in the user's browser and not synced across devices.
- Avoid entering patient-identifiable information in AI services or this app.

## Files
- `index.html`, `style.css`, `app.js`: static web application.
- `data/cases.json`: built-in case pack, editable as JSON.
- `netlify.toml`, `_redirects`: Netlify static deployment.
- `EM_AI_Case_Pack_Prompt.txt`: prompt to give any AI model.
- `EM_Case_Pack_Template_v2.json`: required schema-shaped template.

## Recommended next iteration
Add context-aware multi-action clinical rules, time-dependent patient branching, per-step required action tracking, full dose/route checks, faculty sign-off, automated test fixtures, and optional backend for semantic analysis. Keep a separate staging site while testing.

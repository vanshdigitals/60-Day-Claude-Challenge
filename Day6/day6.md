# Day 06 - AI Resume Optimizer

## Objective

The goal of this experiment was to test whether Claude could meaningfully improve an existing Graphic Design resume for both ATS (Applicant Tracking System) compatibility and human recruiter readability, without exaggerating or fabricating any part of my actual background. Since my professional experience is largely freelance and project-based, a secondary goal was to see whether Claude could represent that kind of work honestly and clearly, instead of forcing it into a traditional full-time job format.

## Challenge

I tested Claude as an ATS resume auditor and optimizer using my real, existing resume as a Graphic Design student targeting internship and entry-level roles.

ATS optimization matters specifically for this kind of role because most Graphic Design internship and entry-level applications for offline positions are still filtered through ATS software before a human ever sees them. A resume with heavy visual formatting, inconsistent section headers, or missing standard keywords can get filtered out automatically, regardless of the quality of the actual design work behind it. At the same time, over-optimizing for keywords at the cost of truthfulness creates risk during interviews, when a recruiter can easily ask a follow-up question that exposes an exaggerated claim.

The experiment was designed to test both sides of that balance: strict ATS structure, without inflating my actual skill level or experience.

## Prompt Used

I used a structured Resume Optimizer / Resume Auditor prompt with Claude, built around this format:

```
Act as a professional ATS resume auditor and recruiter for entry-level Graphic Design roles.

Evaluate my resume across:
1. ATS Parsing (structure, formatting, headings, file format)
2. Keyword Alignment (Graphic Designer / Junior Graphic Designer / Graphic Design Intern keywords)
3. Experience (freelance/project-based clarity, dates, titles)
4. Skills (correct categorization, no overstated tool proficiency)
5. Content Quality (summary, action verbs, repetition, weak wording)
6. ATS Risk
7. Recruiter Readability (10-second scan test)
8. Truthfulness Check (flag any potentially overstated claim)

Output format:
ATS READINESS: __/100
RECRUITER READINESS: __/100

Then:
A. ATS Strengths
B. ATS Problems
C. Missing Keywords
D. Content Problems
E. Formatting Problems
F. Experience Presentation Problems
G. Top 10 Changes

End with a verdict: READY TO APPLY / NEEDS MINOR FIXES / NEEDS MAJOR REVISION

Be strict. Do not give a high score simply to be encouraging.
```

I deliberately asked Claude to audit first, without making any changes, so I could review the analysis before approving any actual edits to the resume.

## Original Resume

The original resume analyzed was a single-column Graphic Design resume containing:

- Contact information and a professional summary
- Education (BCA, ongoing)
- Freelance/project-based experience with clients including Cuts & Curves, Ranjeet Raj Official, Keshvi Beauty Lounge, Waterplane, Builders Playground, and a sample project with Rich Route
- A Skills section covering Canva, Photoshop, Illustrator, and Figma
- Certifications and additional background context

The resume was already free of tables, icons, and graphics, but had not yet been audited for keyword coverage, date consistency, or repetition between sections.

## ATS Analysis

Claude's actual audit returned the following:

**ATS READINESS: 78/100**
**RECRUITER READINESS: 61/100**

**ATS Strengths**
- True single-column layout, confirmed by direct text extraction
- Standard, recognizable section headings
- No icons, columns, skill bars, or images
- Contact information in plain text, not in a header/footer field
- Consistent job-entry formatting
- Both DOCX and PDF formats provided

**ATS Problems**
- Tab-based right-aligned dates could collapse or merge with job titles in some older ATS parsers
- No experience entries had machine-standard MM/YYYY–MM/YYYY dates, since the work is genuinely freelance and irregular
- Font choice (DM Sans/Inter) carried low but non-zero rendering risk in older ATS preview environments

**Missing Keywords**
- "Carousel Design" underused outside the Skills section
- "Branding" / "Brand Identity" missing as standalone keywords
- The bare phrase "Graphic Designer" appeared only combined with "Freelance"
- "Adobe Creative Suite" as an umbrella term was absent
- "Print Design" and "Campaign Design" were not present

**Content Problems**
- Professional Summary opened with softer framing ("Early-career...") before the concrete value proposition
- Repetition between the Experience section and Selected Projects, where three clients were described twice with similar wording
- Some bullets used softer verbs ("Supported," "Assisted with") where stronger, number-led phrasing was possible

**Formatting Problems**
- Selected Projects section split awkwardly across the page break
- Noticeable empty space at the bottom of page 2
- Mixed use of em-dashes and en-dashes, which carries minor ATS compatibility risk

**Experience Presentation Problems**
- Freelance/project-based nature was already clearly labeled across all entries (flagged as a genuine strength)
- Ranjeet Raj Official had no time anchor at all (no year or span)
- Waterplane's timeframe was buried inside a bullet instead of the date field

**Recommended Changes (Top 10)**
1. Reduce repetition between Experience and Selected Projects
2. Move Waterplane's date range into the date field
3. Add a rough year/span to Ranjeet Raj Official's duration
4. Replace vague branding phrasing with standard keyword-matchable terms
5. Add "Branding" as a keyword where truthfully supported
6. Add "Adobe Creative Suite" as an umbrella term
7. Lead more bullets with numbers instead of soft verbs
8. Tighten the Additional Background paragraph
9. Standardize dash characters throughout
10. Rebalance the page break so sections don't split awkwardly

**Verdict: NEEDS MINOR FIXES**

Claude was explicit that the resume was not fabricated or misleading anywhere, and that the issues identified were presentation and structure problems rather than truthfulness problems.

## Resume Optimization

Based on the audit, the following actual changes were made:

- **Professional Summary**: Rewritten to lead with concrete capability (3+ years of Canva experience, real freelance client work) rather than opening with softer "early-career" framing.
- **Location positioning**: Added a clear, standalone line — "Noida, Delhi NCR | Open to Delhi / Gurugram Relocation" — placed near the top of the resume so it is visible within a 10-second recruiter scan.
- **Experience structure**: Renamed the section to a standard "EXPERIENCE" heading and kept every entry ordered newest to oldest.
- **Freelance/project-based labeling**: Preserved and reinforced — every entry explicitly states whether it was project-based freelance, unpaid, short-term, or a sample/prospect project.
- **Dates and timeline**: Moved Waterplane's approximate timeframe into the date field for consistency with all other entries.
- **Skills**: Reorganized into Design Software, Design Practice, Design Fundamentals, and a clearly separated Secondary/Supporting Skills group.
- **Branding keywords**: Added "Branding & Brand Identity (Basic)" to Design Practice, justified specifically by the Keshvi Beauty Lounge brand color/font/AI-logo work already documented.
- **Adobe Creative Suite**: Added as an umbrella term alongside the existing Photoshop and Illustrator listings.
- **Carousel Design**: Reinforced as a keyword within Design Practice and experience bullets.
- **Figma skill level**: Confirmed and kept as "Basic Familiarity" only, with no advanced or professional-level language used anywhere.
- **AI and technical skills positioning**: Kept fully separate from core design skills, under a "Secondary/Supporting Skills" label, covering AI-assisted workflows, prompt engineering, and basic HTML/CSS/JavaScript.
- **Education**: Left unchanged, since the original details were already accurate.
- **Certifications**: Left unchanged, since all listed certifications were already genuine and previously confirmed.
- **Areas of Interest**: Trimmed to a concise, relevant list matching the rest of the resume.
- **Additional Background**: Rewritten more concisely, retaining the honest framing of the 800+ Canva design estimate as a lifetime recollection-based figure, not an audited client-delivery metric.
- **ATS-friendly formatting**: Standardized dashes to plain hyphens, removed repetition between Experience and Selected Projects, and rebalanced the page break so no section split awkwardly across pages.

## Final Resume Positioning

The final resume positions me as a Graphic Designer, Visual Content Designer, and Graphic Design Intern candidate — not as a senior designer, not as an AI Engineer, and not as a Web Developer.

Key factual positioning points reflected in the final version:

- Graphic Design is presented as my primary career direction throughout.
- The resume is targeted at a paid, offline Graphic Design internship or entry-level role.
- Target locations (Noida, Delhi NCR, and Gurugram) are stated clearly and prominently.
- ₹20,000+ per month appears only as context in my own job-search process, never written into the resume as a current or past salary.
- Canva is presented as my strongest tool, backed by 3+ years of practical experience.
- Photoshop and Illustrator are labeled as developing/professional tools, not as fully mastered skills.
- Figma is labeled only as basic familiarity, with no advanced or expert language.
- My practical experience — social media posts, Instagram carousels, reel covers, posters, promotional creatives, and basic branding support — is presented as the core evidence of my ability.
- AI tools, prompt engineering, and HTML/CSS/JS are positioned as supporting, secondary skills, never as my primary professional identity.
- Every freelance engagement is labeled by its actual nature: project-based, unpaid, short-term, or sample/prospect work, with no entry implying full-time or continuous employment.

## Key Learnings

- **ATS parsing** depends heavily on structural simplicity — a single-column layout with standard headings and real selectable text matters more than visual polish.
- **Recruiter readability** is a separate concern from ATS parsing; a resume can pass ATS filters and still fail a human's 10-second scan if the most important information isn't immediately visible.
- **Keyword optimization** works best when new keywords are added only where they are already truthfully supported by real experience, not inserted purely to match a job description.
- **Resume structure** benefits from clear separation between "Experience" and "Selected Projects" — duplicating the same clients across both sections wastes space without adding new information.
- **Truthful optimization** is possible without sounding junior or unpolished. Strong, specific wording and truthful wording are not in conflict.
- **Freelance experience** can be represented professionally and clearly on a resume without exaggerating it into full-time employment, as long as duration and payment status are labeled explicitly.
- **Quantifying real work** (e.g., "50–60+ social media carousels") is more persuasive than vague descriptive language, as long as the numbers are genuine estimates I can defend if asked.
- The clearest distinction from this experiment was between **optimization and exaggeration**: optimization means presenting real experience as clearly and effectively as possible; exaggeration means changing what actually happened. Claude's audit consistently pushed toward the former.

## Before vs After

| Area | Before | After |
|---|---|---|
| Location visibility | Buried inside a longer contact line | Standalone, bold line near the top of the resume |
| Professional Summary | Opened with softer "early-career" framing | Leads with concrete experience and capability |
| Experience vs Selected Projects | Repeated the same three clients with similar wording | Selected Projects trimmed to add genuinely new information only |
| Waterplane dates | Buried inside a bullet | Moved to the date field, consistent with other entries |
| Ranjeet Raj Official | No time anchor at all | Retained honestly as "Recurring" since no verified date was available |
| Branding keywords | Not present as standalone terms | Added where truthfully supported by existing work |
| Adobe Creative Suite | Not mentioned | Added as an umbrella term alongside Photoshop/Illustrator |
| Figma | Basic familiarity | Basic familiarity (unchanged — confirmed correct both times) |
| Dash formatting | Mixed em-dashes and en-dashes | Standardized to plain hyphens |
| Page balance | Section split awkwardly across pages, uneven whitespace | Rebalanced for cleaner section boundaries |

## Limitations

- ATS scores produced by Claude are estimates based on general ATS parsing behavior, not a guarantee of how any specific ATS software will score the resume.
- Different companies use different ATS systems, and parsing behavior can vary between them.
- Some of my older design work from 2024–2025 is no longer accessible, since it was created on a third-party Canva account that has since been closed.
- Some historical design counts, including the 800+ lifetime Canva estimate, are based on recollection rather than an audited record.
- Freelance and project-based work does not follow standard employment date formats, which means some experience entries cannot include exact start/end dates without inventing information I don't actually have.

## Conclusion

Using Claude as an AI Resume Optimizer for Day 6 showed that the most valuable part of the process wasn't generating new content — it was the audit step that came first. Having Claude evaluate the resume strictly, flag real problems, and explain exactly why each one mattered made it possible to fix genuine ATS and readability issues without touching the truthfulness of any claim. The clearest takeaway is that good resume optimization is really an editing and clarity problem, not a content-invention problem: almost every meaningful improvement came from presenting real experience more clearly, not from adding anything that wasn't already true.

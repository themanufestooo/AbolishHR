# Profile Schema

Your profile has **two separate records**. They are stored apart and used for different things. This separation protects your sensitive information.

## Record 1 — Career record

**Used for:** scoring jobs, writing your resume, drafting cover letters, preparing for interviews.
**Never contains:** passwords, legal answers, or identity details beyond your name and city.

| Field | Required? | How it's validated |
|---|---|---|
| Employers, titles, dates | Yes | You confirm; resume import if you have one |
| Day-to-day responsibilities | Yes | Your own words from the workbook |
| Tools and software | If any | Your own words |
| Measurable results | If any | You confirm; marked "user-verified" or "estimated" |
| Transferable experience (caregiving, gig, volunteer, informal) | If any | Structured interview in plain language |
| Skills list | Yes | Derived only from confirmed experience |
| Languages | If any | You confirm fluency level |
| Job strategy (roles, pay floor, schedule, location, hard no's) | Yes | Ranked preferences + hard constraints |
| Evidence (certifications, portfolio, references) | If any | Attach source or mark user-verified |

**Rule:** anything not confirmed is labeled unknown — never filled in by guessing.

## Record 2 — Identity record

**Used for:** filling in application forms only. Never used to write resumes or score jobs.
**Access:** least privilege — the assistant retrieves only the fields a given form actually asks for.

| Field | Required? | How it's validated |
|---|---|---|
| Legal name | Yes | You enter it directly |
| Phone, email | Yes | You enter them directly |
| Address (city/state/ZIP) | Yes | You enter it directly |
| Work authorization | Yes | You enter it directly; never inferred |
| Sponsorship needs | Yes | You enter it directly; never inferred |
| Education | Yes | You enter it directly |
| Earliest start date | Yes | You enter it directly |
| Relocation willingness | Yes | You enter it directly |

## Data separation

Keep these five kinds of data apart:

1. **Public job data** — listings, company info, salary ranges (not sensitive)
2. **Career evidence** — your verified work history (used for matching and documents)
3. **Sensitive identity data** — legal name, address, authorization, demographics (forms only)
4. **Credentials** — passwords, login sessions (never stored in the profile; handled per-session)
5. **Application outcomes** — what you applied to and what happened (your history)

Search and scoring need only #1 and #2. Resume writing needs only #2. The browser/form step retrieves only the specific #3 fields the current form asks for. #4 never appears in the profile at all.

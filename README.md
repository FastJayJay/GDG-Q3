# Housing Funding Finder

> Helps a Rhode Island affordable-housing developer see which funding sources fit their project, when each one is due, and how much more committed funding they need before they can start construction.

Built at [Build for Good: AI Lab for Housing](https://gdgpvd.dev/housing-jam), DevFest Providence 2026 (GDG Providence, Fri Oct 16, 2026).

**Challenge:** 3. How does this project get funded?

**App:** [link to app](https://claude.ai/artifact/U4zPaHn2nXMbESPVs2q49v)
**Team:** Jacob Burdick, Sebastian Coso (Coders). Reinaldo Gonzalez, Bancroft Soto (Housing experts)

![Screenshot](https://github.com/user-attachments/assets/d83de49f-4749-40ed-bef7-da97a0ae965f)

## The problem

A subsidized project has to find, qualify for, and apply to several capital sources, each with its own forms, cycle, and conditions. Developers usually track this in spreadsheets and by reading separate program documents. Each added source costs about four months and $20,000 per unit, and projects often wait a year or more between awards.

## What it does

What someone can do with your app, step by step. Keep it to what works today.

1. Shows the capital stack on a dashboard, with each source colored by status: committed, applied, in prep, prospect, or denied/overdue.
2. Compares committed funding against total development cost and shows the gap that has to close before construction.
3. Lists 19 Rhode Island and federal programs (RIHousing, Housing 2030, ARP, ZEOS, HOME, HTF, LIHTC, FHLB Boston AHP, LISC and others). Each shows who can apply, roughly how much, the next deadline, and a link to the source. Where a deadline or amount isn't published, it says "check the source."
4. Takes the project's AMI mix, checks it against the LIHTC set-aside test, and shows which programs that mix keeps open.
5. Finds sources by development phase (predevelopment, acquisition, construction, permanent/gap, operations) and by use (land, design, energy, infrastructure and so on).
6. Scores each program's eligibility against a threshold you set, and shows the criteria behind the score.
7. Calculates total cost minus selected sources to show the remaining gap.
8. Tracks deadlines and requirements in one place, and offers a funding chat that answers questions about the project's stack.

Every program card says which document it followed: the 2026 Round 2 RFP, the Round 1 RFP, the October 2025 Handbook, or the draft 2027 QAP. Dates from the draft 2027 QAP are labeled "Expected, not final."

## How it uses AI

- **Models and tools:** for example Gemini in Google AI Studio, Google Maps Platform.
- **What the AI does:** for example drafts the checklist from the town's ordinance.
- **What it does not do:** for example it never fills in a setback; the user reads it from the ordinance.

## Responsible use

- **Where it can be wrong:** Program details come from the RIHousing documents and RFPs I could read. They were not checked with the agencies. The Round 2 RFP did not state that it overrides the Handbook, so the app names the document each card followed. Round 2 closed June 18, 2026, and later dates are expected, not final. Phase and use tags are my own reading of the documents. Confirm every amount, deadline, and rule on the linked source page before relying on it.
- **Data:** Project figures are stored in the app's own storage, with a browser fallback. The only data sent elsewhere is the chat text and project summary sent to Claude. No API keys or personal data are in this repo.
- **Accessibility:** Status is shown with text labels as well as color, controls can be used by keyboard, and the layout works on a phone.

## Run it

No install is needed. Open the app link above. It needs a claude.ai account to use the chat. The source is a single HTML file.

## What's next

Fill in the lender and bank programs that aren't published, such as LISC loan terms.
Share one set of project facts across several applications instead of retyping them.
Add Spanish, Portuguese, Kriolu, and Haitian Creole versions, and a plain-language summary for neighbors and the public hearing.
Test it with a RIHousing program officer and a developer's executive director.

## License

Code under the [MIT License](LICENSE): put your team name on the copyright line. You keep the rights to your work; the license lets others learn from it and build on it.

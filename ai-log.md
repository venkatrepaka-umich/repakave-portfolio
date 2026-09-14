## Project context
- Purpose: Present a student's skills and projects to internship reviewers.
- Existing system: an HTML/CSS/JavaScript portfolio template.
- Allowed changes: content, styling, and small front-end corrections only.
- Do not add: a backend, login system, analytics tracker, or external data collection.

## Acceptance criteria
1. The static contact card on the left side shows updated contact details — name, title, email, phone, birthday, location. Social links have a single X icon.
2. The About Me section has the correct info about me. Template content should be updated to show correct information.
3. The "What am I doing" section title is changed to "What am I studying," and its 4 cards show my graduate coursework instead of template services.
4. There should be no clients section
5. The testimonial section should be professional certifications. 

## Constraints: 
- Do not invent education, work history, awards, links, or technical skills. 
- Preserve required license and attribution.
- Keep the site usable on mobile screens.
- Maintain readable contrast, keyboard navigation, meaningful link text, and useful image alternative text.
- Do not expose private information.

## First provide: 
1. A file-by-file implementation plan. 
2. Any Assumptions or risks.
3. A proposed test checklist. 
4. Any questions that must be answered before implementation.

## Do not modify the file until the plan is reviewed.


```
Plan: Personalize Portfolio Content
Update the verified About experience while preserving the static architecture, license, attribution, and mobile behavior.

Implementation

Update the sidebar in index.html:
Name, title, email, phone, birthday, and location.
Correct avatar alternative text.
Replace Facebook/Twitter/Instagram with one accessible X link.
Replace the template About Me text with the approved content from content-notes.md.
Rename “What I’m doing” to “What I’m studying” and replace the four service cards with:
Machine Learning
Software Engineering
Deep Learning
Data Mining
Replace Testimonials with Professional Certifications using the two approved AWS certifications and descriptions.
Preserve the certification card/modal interaction, adjusting script.js only if needed.
Remove the Clients section and safely remove unused client CSS.
Leave Resume, Portfolio, Blog, and Contact unchanged until verified content is provided.
Relevant Files

index.html: primary content and markup changes.
script.js: possible certification-modal adjustments.
style.css: responsive/accessibility cleanup and obsolete client styles.
content-notes.md: source of truth; no changes planned.
LICENSE: preserve unchanged.
Assumptions and Risks

Exact phone and birthday values will be displayed as approved, despite the privacy warning in the assignment guide. This should be reconsidered before public deployment.
University of Michigan-Flint is the selected institution for future education updates.
No certification IDs, dates, exam scores, or links will be invented.
Existing external dependencies and the Google Maps embed remain out of scope.
Existing unsupported Resume, Portfolio, Blog, and Contact template content will remain temporarily.
Test Checklist

Search for and remove requested template identity, testimonial, and client strings.
Confirm no Clients section remains.
Verify the page at mobile and desktop widths without overflow or clipped text.
Keyboard-test navigation, sidebar toggle, X link, certification cards/modal, and form controls.
Confirm visible focus states, meaningful link labels, and useful image alternatives.
Run an HTML/CSS/JS or browser smoke check and confirm no console errors.
Confirm LICENSE and attribution remain unchanged.
No project files have been modified.
```

```
Do not invent any date for certification. Leave the verification details for now.
```

```
Confirmed. The certification cards and modal contain no dates, credential IDs, exam scores, or verification claims beyond the approved descriptions. No files were modified.
```

```
alt text should show text "avatar"
changing from 4 testimonials to 2 certifications. Scroll bar should not be removed. Make sure it get's enabled if more certifications are added later.
```

```
Updated index.html:311:

Replaced 4 testimonials with 2 AWS certification cards.
Set certification and modal image alt text to exactly avatar.
Removed the invented certification date.
Preserved testimonials-list has-scrollbar and horizontal overflow behavior for future certifications.
```

```
Make incremental changes.
First - contact card, About Me, study cards, single accessible X link
```

```
Completed the first incremental change in index.html:

Updated contact card details and profile image alt text to avatar.
Replaced About Me template content.
Changed the section title to “What am I studying”.
Replaced the four service cards with the four graduate coursework subjects.
Replaced social links with one accessible X link.
HTML diagnostics pass. Certifications, scrollbar behavior, and Clients content were left unchanged for the next incremental step.
```

```
Update title in header to reflect my name
```

```
Updated the page title in index.html:8 to:


HTML diagnostics pass.
```

I have used GitHub Copilot for planning and implementation. I have reviewed and edited all code generated by Copilot and take full responsibility for the content of this submission.

I have used Gemini for refining few of my sentences in the answers. I give the content and accept the suggestions made by Gemini.
e.g. 
My sentence: "The evidence is that a regression of the system should not be required after each build."

Gemini: "The evidence I'd want is that manual regression checking keeps being necessary after AI-driven changes; if that keeps happening, it justifies the automation investment."

The idea of putting "Pass" in the test checklist is to indicate that the test has been completed successfully is from Gemini.
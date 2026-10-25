# Prompt Log & Documentation

## Task #1 - Selector Selection
* **Sector:** Tourism & Cultural Innovation
* **Local Challenge:** Tourists and even local residents of Marinduque don't have a single, centralized web to explore cultural heritages, learn traditions, and plan itineraries.
* **Target Users:** Tourists and local residents
* **Proposed Project:** Marinduque Cultural & Heritage Explorer
* **Key Features:** Places gallery, Place information, Trip Planner Checklist

---

## Task #2 — Zero-Shot Prompting
**Objective:** Create an initial prototype layout for the Marinduque Cultural & Heritage Explorer web application.
**Exact Prompt:**
> Create a simple webpage for Marinduque tourism showing places and culture.
**Actual Copilot Output:**
`outputs/task2.html`
**What Worked / Observation:**
Copilot successfully created a HTML page layout with a title and general information about Marinduque, as well as a few popular tourist places.
**What Needs Improvement:**
Since it was basic, there were missing interactive features and responsive layouts that were not included in the prompt.
**Next Action / Verification:**
Include a trip planner checklist; Add responsive styles; Refine the prompt to add category filters.

---

## Task #3 — Structured Prompting
**Objective:** Build a responsive single-page web application with filters, modals, and an itinerary bookmark feature.
**Exact Prompt:**
> Act as a frontend web developer. Create a responsive single-page web application titled "Marinduque Cultural & Heritage Explorer" for tourists in Marinduque. Include a header with navigation, a filterable gallery of tourism cards (Categories: Culture, Heritage, Eco-Tourism), an interactive landmark modal, and an itinerary bookmark feature. Use semantic HTML, CSS, and vanilla JavaScript all contained within a single HTML file without external libraries or backend APIs. Provide the complete code.
**Actual Copilot Output:**
`outputs/task3.html`
**What Worked / Observation:**
The structured prompt successfully generated a trip planner list and added category filters (Culture, Heritage, Eco-Tourism). However, the image URLs used were not accurately correct to represent the Marinduque places.
**What Needs Improvement:**
Image sources need to be specified with verified direct image URLs.
**Next Action / Verification:**
Specify exact image URLs in the prompt to ensure accurate visual representations.

---

## Task #4A — Few-Shot Prompting
**Objective:** Standardize card data layout using few-shot examples with accurate, verified image URLs.
**Exact Prompt:**
> Using the single-file web app structure for "Marinduque Cultural & Heritage Explorer", update the card data using few-shot examples with verified and accurate image URLs and descriptions:
> 
> Example 1: - Title: Moriones Festival - Category: Culture - Image: https://lakbaypinas.com/wp-content/uploads/2024/07/449163598_8809426125741114_3678558316433235836_n.jpg - Description: A traditional Lenten festival celebrated every Holy Week on the island of Marinduque.
> 
> Example 2: - Title: Boac Cathedral - Category: Heritage - Image: https://upload.wikimedia.org/wikipedia/commons/9/91/Boac_Cathedral_facade.jpg - Description: A historic fortress church built in 1756 perched on a hill in Boac, Marinduque.
> 
> Apply this exact data layout and accurate image pattern across all cards in the gallery while keeping the filter, modal, and trip planner functionality completely working in a single HTML file.
**Actual Copilot Output:**
`outputs/task4A.html`
**What Worked / Observation:**
Providing examples guided the Copilot to produce more accurate visual representation for every tourist's spots in Marinduque. However, some links are broken displaying gray blank photos.
**What Needs Improvement:**
Replace any broken image links with valid, direct visual assets.
**Next Action / Verification:**
Test alternative image URLs to ensure all photos are displayed without broken gray placeholders, and finalize the web prototype.

---

## Task #4B — Role Assignment
**Objective:** Perform a specialized technical accessibility audit to evaluate HTML semantics, keyboard access, labels, and contrast.
**Exact Prompt:**
> Act as a frontend accessibility reviewer. Examine the generated Marinduque Cultural & Heritage Explorer. Identify problems involving HTML semantics, keyboard access, labels, and visual clarity. Recommend targeted improvements without changing the project's scope.
**Actual Copilot Output:**
`outputs/task4B.txt`
**What Worked / Observation:**
Assigning the AI a specialized reviewer role made it inspect technical quality, successfully catching source mismatches and low contrast issues that were missed in general generation.
**What Needs Improvement:**
Specific code fixes are required to improve visual contrast and focus handling.
**Next Action / Verification:**
Based on the accessibility review findings, ask Copilot to fix minimal code corrections to resolve contrast ratio and other issues.

---

## Task #5 — Analyze Structured Reasoning and Refinement
**Objective:** Request technical diagnosis and targeted code fixes for the top accessibility implementation weaknesses.
**Exact Prompt:**
> Review my Marinduque Cultural & Heritage Explorer code based on your accessibility review. Identify the two most important implementation issues, provide the smallest appropriate code corrections to fix them, and explain how I can test and verify the fixes.
**Actual Copilot Output:**
`outputs/task5.txt`
**What Worked / Observation:**
Copilot successfully applied targeted code fixes by adding a polite screen-reader announcement (`aria-live="polite"`) for itinerary updates and updating focus management to prevent focus loss. After applying the correction, I tested and verified based on the instructions provided by the AI.
**What Needs Improvement:**
None. Code changes are tested and verified.
**Next Action / Verification:**
All are verified and tested. Next action would be the final comparison and submission.

---

## Task #6 — Compare and Submit

### Final Comparison Table

| Technique | Observation |
| :--- | :--- |
| **Zero-Shot** | Copilot provided the basic layout and since it was basic, there were missing features that are not included in the prompt. |
| **Structured Prompt** | Better prompt to add features like filters and planner checklists that work properly because the requirements were defined. |
| **Few-Shot** | Giving instance/example images by using a clear format produced an accurate visual representation for the places. Although some images were broken, it was fixed by replacing the link. |
| **Role Assignment** | Assigning an accessibility reviewer role helped Copilot spot specific minimal code issues, such as contrast colors, etc. |
| **Structured Analysis** | Asking Copilot to fix those minimal code issues allowed it to fix the certain issues, specifically updates that fixed the overall process of adding and removing in the “Your Island List”/the planning checklist. |

### Final Reflection
Structured prompting worked best for building the initial layout since all required features were stated clearly. Few-shot prompting helped make the card data consistent, while role assignment showed accessibility details that were easy to miss. I learned that AI outputs still need to be reviewed and tested to make sure everything works properly.
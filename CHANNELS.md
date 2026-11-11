# Channel justification: prototype vs Week 5 proposal

Every channel below matches the proposal's channel justification table. The changes at the bottom are noted as the rubric asks.

| Data variable | Type | Mark | Channel | Principle | Justification | Matches proposal? |
|---|---|---|---|---|---|---|
| Charges | Quantitative | Point (scatter), bar (bar charts) | Y-position / bar length on a common scale | Effectiveness | Most important variable, so it gets the strongest channel (Cleveland & McGill). | Yes |
| Age | Quantitative | Point | X-position | Effectiveness | Second key quantitative variable; position shows the age trend precisely. | Yes |
| Smoker | Categorical (2) | Point | Colour hue (orange `#E69F00` / blue `#0072B2`) | Expressiveness | Hue is an identity channel for identity data. The pair is colourblind-safe and differs in lightness. | Yes |
| BMI category | Ordinal (4) | Bar | X-position in WHO order | Expressiveness | Ordered data on an ordered channel; never sorted by value. | Yes |
| Region | Categorical (4) | Bar | Y-position (rows), sorted by overall average | Effectiveness / similarity | Unordered categories get spatial separation; sorting makes ranking easy. One neutral grey avoids implying order. | Yes |
| Sex, children, BMI value | Categorical / ordinal / quantitative | none | Tooltip text | Details on demand | Low-priority dimensions kept out of the marks to protect the data-ink ratio. | Yes (BMI value added to the tooltip) |

Dimensions encoded on marks: 5 (charges, age, smoker, BMI category, region). Three more are available on hover.

## Changes from the proposal
1. **Tool:** D3.js v7 instead of Tableau Public. The assignment allows D3, and Tableau's web editor was too slow to build the dashboard reliably.
2. **Smoker toggle added** (Everyone / Smokers / Non-smokers). It answers the grader's feedback on the proposal, because most research questions depend on smoker status. It filters all views and the KPIs.
3. **Selection styling:** a selected bar is dark grey and the other bars light grey (lightness, not hue). Points outside the current selection fade to low opacity. No new hue was introduced.
4. **Filter semantics:** each view is filtered by every selection except its own, so the other bars stay visible for comparison while one is selected.

## Known gaps, planned for the final
Layout refinement, a greyscale/colourblind check of the final screenshots, usability testing with 2 peers, and the reflection are assessed at the final submission.

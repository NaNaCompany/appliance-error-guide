# Appliance error guide — source and scope review

- Dataset: `appliance-data.json`
- Slug: `appliance-error-guide`
- Checked: 2026-10-27
- Coverage: 24 code/context records; Samsung 8, LG 16; washer 14, dishwasher 6, refrigerator 4.
- Languages: ko, en, es, zh, ja, de. All 144 localized records contain title, summary, two checks, escalation and scope. Root title, description and three category labels are also localized.

## Source register

All references below are first-party HTML support articles. Each URL was opened through the web tool during this review. Source article scope and code meanings were checked against the returned article content and official search excerpts. No manual, PDF, external table, image, logo, diagram, installer or firmware was downloaded into the deliverable.

| Source | Verified context and records | Official URL |
| --- | --- | --- |
| Samsung US washer information codes | Washer 4C, 5C, Ub, SUd; spelling variants are drawn from the corresponding headings | https://www.samsung.com/us/support/troubleshoot/TSG10000997/ |
| Samsung US dishwasher codes | Dishwasher 4C, 5C, CE; LC/LE narrowed to rotary spray-arm models without Waterwall | https://www.samsung.com/us/support/troubleshoot/TSG10004499/ |
| LG US top-load washer list | Top-load dE, CL, tCL, PF; notification versus fault distinction preserved | https://www.lg.com/us/support/help-library/lg-top-load-washer-error-code-list-CT10000010-20154403824104 |
| LG US front-load washer list | Front-load IE/E02/E10, OE/E03/E21, UE, LE | https://www.lg.com/us/support/help-library/lg-front-load-washer-error-code-list--20155069413456 |
| LG refrigerator digital and analog codes | Refrigerator CF, CO, FS; internal fan, communication and freezer-sensor contexts kept separate | https://www.lg.com/us/support/help-library/lg-refrigerator-digital-and-analog-error-codes--20154835849096 |
| LG refrigerator Er FF article | Refrigerator Er FF, E FF, F; freezer-fan operation and possible frost involvement | https://www.lg.com/us/support/help-library/if-you-see-an-er-ff-e-ff-or-f-error-code-on-your-lg-refrigerator--20155452969338 |
| LG dishwasher OE article | Dishwasher drainage context, separate from washer OE | https://www.lg.com/us/support/help-library/lg-dishwashers-troubleshooting-an-oe-error-code-CT10000009-1440686618796 |
| LG DIOS dishwasher IE article | DIOS dishwasher supply context, separate from washer IE | https://www.lg.com/us/support/help-library/lg-dios-dishwasher-dishwasher-an-ie-error-appears-on-the-display-CT10000009-20155103088326 |
| LG top-load UE/Ub article | Top-load unbalance/rebalancing context and case-sensitive stages | https://www.lg.com/us/support/help-library/lg-washer-what-is-a-top-load-washing-machine-ueub-error-code-CT00000305-1394563702295 |
| LG pedestal washer codes | SideKick E7 installation/stacking-detection context | https://www.lg.com/us/support/help-library/error-codes-pedestal-washer--20150103764784 |

## Scope decisions

- These are product-family support articles, not a tested matrix of individual retail model numbers. `models` therefore names the actual supported product scope. No specific model number was invented and no universal model guarantee is implied. Each translated scope tells readers to consult their exact model manual where needed.
- Samsung washer and dishwasher 4C/5C have independent records. LG front-load, top-load and dishwasher IE/OE/UE contexts are not merged by code spelling.
- Samsung dishwasher LC/LE can have a Waterwall reflector interpretation. This record is explicitly limited to non-Waterwall rotary-spray models; Waterwall is not diagnosed as leakage by this dataset.
- Samsung washer ambiguous 3E and dC, and dishwasher 1E with two product-family meanings, are excluded. Samsung Ur is not presented as equivalent to a failed spin: it is omitted from the Ub aliases.
- LG top-load uE can be an active rebalance indication. UE/Ub can need load adjustment. The record states that case distinguishes stages rather than asserting that every spelling is a terminal failure.
- LG CL and tCL are settings/reminders; PF records an interruption. They are not labeled as proof of component failure.
- LG refrigerator display prefixes and positions differ by model. The exact full display is required. The F alias is used only in the refrigerator Er FF article context, not as a global appliance fault.

## Editorial and safety review

Every explanation and translation was independently written. References are citation-only; third-party prose, manuals and tables are not republished. Generic external observations are editorial triage, not claims of a manufacturer's physical diagnosis or successful repair.

Checks are restricted to readable displays, model labels, accessible visible hoses, ordinary settings, laundry redistribution after full stop and normal unlocking, externally visible frost/leakage, and food cooling observations. There are no disassembly instructions, live electrical checks, gas work, safety-sensor bypass, internal repair, forced opening, pump access or protection resets. E7 explicitly forbids pressing or fixing the stacking switch. Leak records direct users away from water/electrical parts and to official service. Refrigerator internal faults go to LG service rather than DIY sensor/fan repair.

Manufacturer articles contain additional repair/reset/defrost steps. They are intentionally not reproduced in this triage dataset. No fixed refrigerator defrost time is prescribed because guidance differs across articles and models; food storage and model-specific official procedure must be arranged first.

## Verification boundary

- Local parser/schema check passed: exact root slug/date; 24 unique ASCII IDs and slugs; all six languages; all required localized fields; 2 checks per language; nonempty models; first-party HTTPS sources; translated category labels.
- Counts verified: 144 localized records and 288 individual checks; 10 distinct official URLs.
- Additional direct HTTP recheck: both Samsung URLs and the LG DIOS IE article returned HTTP 200 with expected codes in HTML. Seven other LG URLs returned HTTP 403 to the shell client. Several follow-up web-tool fetches also timed out. The official web-tool article opens/search excerpts supplied the editorial source evidence; this is not a claim that all links returned 200 through every transport.
- No physical appliances were operated or inspected. No repair success, browser UI behavior, generated-page rendering, GitHub build, publication or production link behavior is claimed here. Parent integration owns those phases.

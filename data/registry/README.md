# OSC-Bench registry: Ofcom Codes measures and harms

Built on 2026-09-30 (the build date), using WebFetch / WebSearch only. No curl or python fetching was used. Python was used only to write the YAML files.

Files:
- `measures.yaml` has 163 entries: every measure in the ICU, ICS, PCU and PCS Codes, plus four draft crisis-response measures marked `uncertain`.
- `harms.yaml` lists the harm ids used by `risk`, `risk_any`, `risk_count` and `pc_risk_any`.

## Counts

| Code | verified | uncertain | total |
|---|---|---|---|
| ICU | 42 | 2 (C15, C16) | 44 |
| ICS | 34 | 0 | 34 |
| PCU | 50 | 2 (C11, C12) | 52 |
| PCS | 33 | 0 | 33 |

The ids the Codes leave unused are not in the registry. These are sections B and I in ICU, section B in ICS, sections H and I in PCU, and B, D3, E and F2 in PCS. ICU C11 to C13 are marked "intentionally blank" in the 9 Sep 2026 ICU Code.

## Sources opened

Ofcom:
- Regulatory documents index: https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/online-safety-regulatory-documents
- **ICU Code, amended version.** Cover: "Incorporates amendments issued: 9 September 2026 / Incorporates amendments in force: 30 September 2026". https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/information-for-industry/illegal-harms/detecting-intimate-image-abuse/illegal-content-codes-of-practice-for-user-to-user-services-9sep2026.pdf
- **ICU Code, Feb 2025 version.** Cover: "Issued: 24 February 2025 / In force: 17 March 2025". Used for the measure-id list and in-force dates. https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/information-for-industry/illegal-harms/illegal-content-codes-of-practice-for-user-to-user-services-24-feb.pdf
- **ICS Code, amended version.** Same cover wording as the amended ICU Code. https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/information-for-industry/illegal-harms/detecting-intimate-image-abuse/illegal-content-codes-of-practice-for-search-services-9sep2026.pdf
- **PCU Code.** Cover: "Issued: 4 July 2025 / In force: 25 July 2025". https://www.ofcom.org.uk/siteassets/resources/documents/consultations/category-1-10-weeks/statement-protecting-children-from-harms-online/main-document/protection-of-children-code-of-practice-for-user-to-user-services.pdf
- **PCS Code.** Same cover dates as the PCU Code. https://www.ofcom.org.uk/siteassets/resources/documents/consultations/category-1-10-weeks/statement-protecting-children-from-harms-online/main-document/protection-of-children-code-of-practice-for-search-services2.pdf
- Children's Codes at a glance: https://www.ofcom.org.uk/siteassets/resources/documents/consultations/category-1-10-weeks/statement-protecting-children-from-harms-online/main-document/codes-at-a-glance.pdf?v=395791
- Statement "Detecting intimate image abuse". Published 18 May 2026, updated 9 Sep 2026. It says the amendments were "issued 9 September 2026, in force 30 September 2026". https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/statement-detecting-intimate-image-abuse
- Statement "Crisis response protocol", updated 18 Jun 2026: https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/statement-crisis-response-protocol
- Draft consolidated ICU Code, marked "VERSION NOT IN FORCE". Source for the ICU C15 and C16 text. https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/protecting-children/illegal-harms/draft-consolidated-illegal-content-codes-of-practice-for-user-to-user-services.pdf?v=419247
- Statement "New priority offences: serious self-harm and cyberflashing", 25 Jun 2026: https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/statement-new-priority-offences-serious-self-harm-and-cyberflashing
- Draft consolidated U2U Code from that statement (not in force): https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/information-for-industry/illegal-harms/statement-new-priority-offences-serious-self-harm-and-cyberflashing/draft-consolidated-version-of-u2u-code.pdf
- Risk Assessment Guidance and Risk Profiles, updated 25 Jun 2026. Source for the list of kinds of illegal harm. https://www.ofcom.org.uk/siteassets/resources/documents/online-safety/information-for-industry/illegal-harms/updates/risk-assessment-guidance-and-risk-profiles.pdf
- Statement "Protecting people from illegal harms online" (17 Mar 2025 in-force date): https://www.ofcom.org.uk/online-safety/illegal-and-harmful-content/statement-protecting-people-from-illegal-harms-online

gov.uk:
- PCU Code as laid before Parliament. Source for the index cells of PCU G1-G3 and J1-J3. https://assets.publishing.service.gov.uk/media/680a04f7532adcaaab3a2718/FINAL_-_Protection_of_Children_Code_of_Practice_for_user-to-user_services__2025_Parli_AC.pdf
- Draft amendments to the PCU Code (crisis response). Submitted to the Secretary of State on 12 Jun 2026; page dated 18 Jun 2026. https://www.gov.uk/government/publications/online-safety-act-draft-amendments-to-the-protection-of-children-code-of-practice-for-user-to-user-services
- The same draft amendments as a PDF. Source for PCU C11 and C12. https://assets.publishing.service.gov.uk/media/6a301481a3674dfd3eb508f9/Draft_amendments_to_the_Protection_of_Children_CoP_for_user-to-user_services_PR_A_.pdf
- Explanatory Memorandum for the crisis response measures (negative procedure, no in-force date): https://assets.publishing.service.gov.uk/media/6a31621b45124bc4cb61e1e1/Shared_EM_to_for_Crisis_Response_Measures.pdf

legislation.gov.uk:
- OSA 2023 Schedule 7, as amended: https://www.legislation.gov.uk/ukpga/2023/50/schedule/7
- OSA 2023 sections 60, 61 and 62

Secondary sources, used only to find the measure ids for the crisis measures:
- https://bratby.law/ofcom-crisis-response-protocol/

## Blocked or partial fetches

- The gov.uk HTML Explanatory Memorandum page was rejected by the WebFetch proxy with "url exceeds the maximum fetchable length". The PDF version was used instead.
- **Truncated Code text.** WebFetch cut off long Code PDFs partway through. For the ICU Code, text stopped inside section 5 (Definitions), so the ICU paragraphs 5.4-5.10 and ICU Table C could not be read. For the PCU Code, text stopped before section 4 G/J, so the PCU G and J entries use the index-table cells instead of the paragraph X.1 text. Their locators say so.
- **WebFetch summaries can be wrong.** In one pass, the ICS index was wrongly summarised as "All services" for ICS A6, A7 and C3-C6. A re-check of both the index cell and section 4 shows "Large general search services or multi-risk services", and the registry uses that. Every `verified` entry rests on the "This measure applies to..." paragraph or on an index cell quoted in at least one targeted pass. Where there was doubt, a second pass was run: ICU C9, C14 and E1; PCU B1-B7, D11, D12 and E-F; the PCS section A-D paragraphs.
- Page numbers come from the fetch output and are approximate.
- The Register of Risks (25 Jun 2026) PDF was not opened separately. The harm grouping comes from the updated Risk Assessment Guidance.

## Verified vs uncertain

- `verified` means the applicability wording was read from an Ofcom Code, or from the gov.uk laid or issued version of it, and the in-force date comes from the Code's cover.
- `uncertain` applies to ICU C15, ICU C16, PCU C11 and PCU C12 (crisis response). They are not in the Code versions in force on 30 Sep 2026. The 9 Sep 2026 ICU Code runs C14 to D1. The text comes from Ofcom's draft consolidated Code ("VERSION NOT IN FORCE") and the gov.uk draft amendments. Ofcom's crisis page (updated 18 Jun 2026) says the measures were "laid in parliament" and that "From Autumn, relevant providers will need to take the measures". No in-force date was found, so `in_force` is null.
- **Not recorded.** Ofcom's "additional safety measures" amendments were submitted on 15 May and 1 Jun 2026 and are not in force. They presumably account for ICU C11-C13 and PCU C9-C10, but none of those ids appear with content in any Code in force, so they are not recorded.
- **Harms.** In `harms.yaml`, `harassment`, `intimate_image_abuse`, `fraud` and `proceeds_of_crime` are `uncertain`, only for their exact Sch 7 paragraph mapping.

## Key definitions

- **Large service.** "A service which has more than 7 million monthly active United Kingdom users" (Codes Table A). For search, a **large general search service** is "A general search service which has more than 7 million monthly active United Kingdom users".
- **Averaging.** ICS para 5.9 says the average is "the mean number of active United Kingdom users per month for: a) the six-month period ending with the month preceding the time in question; or b) where the service has been in operation for less than six months, the period for which the service has been in operation." Paras 5.7-5.10 also appear to keep a service above a threshold until its average has been at or below it for six months, but that was only seen in a summarised extraction and is not verified.
  - The corresponding ICU paragraphs could not be read because of truncation. ICU measures cross-refer to "paragraphs 5.7 to 5.10", the same numbering, so parallel wording is assumed.
  - The children's Codes at a glance say "an average user base greater than 7 million monthly active UK users".
- **Multi-risk service** (ICS para 5.6): "at medium or high risk of two or more kinds of illegal harm set out in table C".
- **Multi-risk (children)** (PCS s5): "at medium or high risk of two or more specific kinds of content that is harmful to children".

## Condition keys

Allowed keys from the brief, used as given: `size: large`, `users_over`, `multi_risk`, `risk`, `risk_any`, `feature`, `search_kind`, `children_likely`, `ppc`.

`pc_risk` (single children's harm) was not needed. The measures that name specific children's harms use `pc_risk_any` with a list of harms instead.

Extensions and added keys (each was needed to encode Ofcom's wording without exploding clause counts):

| key | meaning | used by |
|---|---|---|
| `size: not_large` | Not a large service. Added value, used for the "neither large nor multi-risk" measures. | ICU D9, ICS D8, PCU D9/D12, PCS D9/D12 |
| `multi_risk: false` / `multi_risk_children: false` | Negated forms. | same as above |
| `multi_risk_children: true` | "multi-risk (children)": medium or high risk of two or more specific kinds of content harmful to children. | PCU/PCS A, C, D, F |
| `risk_any: {min, harms: [...]}` | Existing key extended with an optional `harms` list. It means medium or high risk (per `min`) of at least one of the listed illegal harms. Without `harms`, it means any kind. | ICU C15/C16/J1-J3, ICU D3-D6, ICS D3-D5 |
| `risk_count: {groups, min, count}` | At least `count` of the listed groups at `min` or above. Each group counts once; for example, image-based CSAM or CSAM URLs counts as one paragraph. | ICU E1 |
| `pc_risk_any: {min, harms?, allowed?}` | At least one specific kind of content harmful to children at `min` or above, optionally limited to `harms`. With `allowed: true`, that kind must also be allowed on the service. | PCU B5-B7, C11/C12, D3-D6, E1/E2, F3-F5, J1-J3; PCS D4-D6 |
| `pc_risk_count: {min, count, exclude?}` | At least `count` specific kinds of children's harm at `min` or above, excluding the listed kinds. | PCU E3 |
| `pc: principal_purpose\|permitted_not_principal\|prohibited` | The `ppc` equivalent for priority content. | PCU B3, B5 |
| `takedown_infeasible: true` | The service prohibits the content, but it is "not currently technically feasible" to take down all such content. | PCU B4, B5 |
| `uses_heaa: true` | The service uses highly effective age assurance to identify child users. | PCU B1 |
| `principal_purpose: pornography` | The principal purpose is hosting or disseminating regulated pornographic content. Used instead of `feature: pornography` to avoid confusion with services that merely allow porn. | ICU C14 |
| `feature: [a, b]` | A list value means all of the features are required. | ICU C14 |
| `feature_any: [...]` | At least one of the features is present. | ICU J1, J3; PCU J1 |
| `category: "1"\|"2A"` | Categorised service. | ICU G2, PCU G2, ICS G2, PCS G2 |

Two conventions apply to how children's measures are encoded:
- Every PCU and PCS clause carries `children_likely: true`, because these Codes apply only to services likely to be accessed by children.
- Functionalities in PCU measures are those on a "child-accessible part of the service".

Feature ids used:

| feature id | meaning |
|---|---|
| `visual_ugc` | Enables photo, video or visual-image user-generated content |
| `file_sharing` | "File-storage and file-sharing service" (Table A) |
| `recommender` | Content recommender system |
| `recommender_testing` | The provider conducts on-platform testing of recommender systems |
| `user_profiles` | User profiles |
| `user_connection` | User connection |
| `posting_content` | Posting content |
| `user_communication` | User communication, including direct messaging and commenting |
| `commenting` | Commenting on content |
| `group_messaging` | Group messaging |
| `content_search` | User-to-user "searching content functionality" |
| `predictive_search` | Predictive search |
| `notable_user_scheme` | Notable user labelling scheme |
| `monetised_scheme` | Monetised labelling scheme |

## Known caveats for scorers

- **Minimum risk level.** `risk.min: medium` means medium or high. Some Ofcom clauses say "large service at medium risk", as in ICU C15 and F1/F2, but high risk at any size is covered by the other clause, so the union is the same.
- **ICU F1/F2 qualification.** These apply only "to the extent that it has an existing means to determine the age or age range" of users. This is recorded in `note`, not encoded as a condition.
- **Suicide and self-harm.** The Codes in force still say "encouraging or assisting suicide (or attempted suicide)". Harm id `suicide_self_harm` reflects Ofcom's 2026 combined risk-assessment kind.
- **Cyberflashing** is a separate kind of illegal harm. No Code measure in force is conditioned on it; a draft would add it to ICU J1 and J2. It still counts toward `multi_risk` and `risk_any`.

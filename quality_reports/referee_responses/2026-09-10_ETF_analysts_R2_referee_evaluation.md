# Referee Report Evaluation and Revision Plan
## "ETF Activities and Analysts' Forecasts" (TAR, Round 2)

**Date:** 2026-09-10
**Inputs:** R1 manuscript (55 pp.), Online Appendix (19 pp.), Referee report (10 points), Editor's letter (R&R with "outcome risk")
**Status:** DRAFT for co-authors

---

## 1. Overall read of the decision

**This is a favorable R&R.** One referee dropped out satisfied. The remaining referee opens by saying the paper "has improved considerably" and closes with "Hope these comments are helpful." None of the ten points attacks identification, data, or the core result. Every one of them is about *presentation* (points 1, 2, 3, 5a, 8, 9, 10) or asks for *additional confirmatory evidence* for the mechanism the paper already claims (points 4, 5, 6, 7). The editor's "outcome risk" language is standard TAR boilerplate for a second-round R&R, but the editor has also added one substantive request of their own (the passive-investing sentence) and a blanket "improve the writing" instruction. Treat the writing point seriously: the editor repeated it, which means the referee's frustration in point 1 ("Honestly, this is hard to follow") landed.

**Three things decide this round:**

1. A complete, well-organized summary-statistics table (points 2, 9) plus economic-magnitude sentences in plain probability terms for every main table (points 1, 2, 3). This is mechanical but it is the referee's dominant complaint and the editor's first area.
2. A new "does the sector component of the surprise shrink?" analysis (points 4, 7; editor's second area). This is the one genuinely new empirical piece. It is feasible with data you already have, and Footnote 14 shows you already ran a version of it.
3. Extending the Low_IndExp cross-section to Tables 6 and 8 (points 5, 6), and justifying every specification with a citation (point 5a).

**Honest risk assessment.** Restating Table 3 in probability terms will make the ETF-level effect look modest (roughly a 1.5 percentage-point increase in revision probability against a 73 percent base, see Section 3 below). That is fine. The paper already calls Table 3 "preliminary" and the launch and Russell tests are stronger. Lean the narrative on Tables 4, 5, and 11 and describe Table 3 as the descriptive starting point. Do not try to dress up the t = 1.73 interaction; the referee already noticed it.

---

## 2. Point-by-point assessment

Severity: **A** = must do, decides the outcome; **B** = should do, referee will check; **C** = do if cheap.

### Point 1: Economic significance in probability terms; estimation method not stated. Severity A.

**Is the referee right?** Yes on both counts.

- The manuscript never says the word "linear probability model" or "OLS" for the Revise regressions. Only Column (3) of Table 3 is described as "weighted ordinary least squares." Tables report adjusted R-squared and a constant, so a careful reader infers OLS, but the referee should not have to infer.
- "3.0 percent of a standard deviation" is a convention from the finance literature that accounting referees dislike. With an LPM the translation is trivial: coefficient × Δ|SUE| = Δ Pr(Revise). Because |SUE| is multiplied by 100 in regressions (Online Appendix Section A), the coefficient of 0.037 means a one-percentage-point-of-price increase in the surprise raises revision probability by 3.7 percentage points.

**What to do.**

1. Add one paragraph at the start of Section 3.2 (before Equation 1): "We estimate all revision regressions as linear probability models by OLS with high-dimensional fixed effects, with standard errors clustered by [announcing firm / analyst]. We use the LPM rather than a logit because (i) analyst and firm-by-cohort fixed effects would drop all analysts or firms without variation in Revise under conditional logit, and (ii) interaction coefficients in nonlinear models do not have the marginal-effect interpretation we need (Ai and Norton 2003). Online Appendix Table OA6 reports logit and conditional-logit estimates for the specifications that permit them; inferences are unchanged." Then actually add OA6.
2. State the estimator in every table note ("Estimated by OLS; Revise regressions are linear probability models").
3. Replace every "percent of a standard deviation" sentence with the template in Section 3 of this memo.
4. Soften the t = 1.73 language. Current text says the interaction "confirm[s] ... significantly stronger." Replace with "marginally significant (p = 0.08)" and add the supporting evidence that already exists: the interaction is significant at 5 percent in the star-firm and largest-holding constructions (Table OA1 Panels A and C) and in the unweighted industry-peer comparison (OA2, t = 2.23). Consider reporting p-values instead of t-statistics throughout, which is TAR house style anyway.

### Point 2: No summary statistics for Table 4 variables; report all variables. Severity A.

**Is the referee right?** Yes. Table 2 covers only the ETF-level pair sample. There are no descriptive statistics anywhere for the launch sample (Revise at analyst level, AFE_analyst, |SUE| in the launch sample, |SUE|_Firm, |SUE|_Sector), the conference-call sample (%FirmQ, %FirmQ_Chg), the portfolio sample (Sector_HHI, Single_Sector, Sector_Covered, Firms_Covered, FQ1, FQ2, Brokerage_Size, Exp_General, Frequency, Promotion, Low_IndExp), or the Russell sample (Revise, |SUE|, ownership variables). The only exceptions are |ARET| and Sector Exposure in Online Appendix Section D and the 6.52 / 1.54 information-point counts in Section B.

**What to do.** Rebuild Table 2 as a multi-panel table mirroring the structure of the Online Appendix variable-definition table (this is also the referee's point 9 suggestion). One panel per sample:

| Panel | Sample | Unit | Variables |
|---|---|---|---|
| A | ETF-level pairs (sector / broad / matched peers) | announcer-follower-quarter-horizon | current Table 2 content, plus SUE_LAG if it is used (see Section 4 below) |
| B | Sector ETF launch sample | analyst-firm-quarter-horizon | Revise, AFE_analyst (revisers / non-revisers), \|SUE\|, \|SUE\|_Firm, \|SUE\|_Sector, \|ARET\|, Sector Exposure, industry experience, controls |
| C | Conference-call sample | analyst-quarter and firm | %FirmQ, firm-specific count, industry-wide count, %FirmQ_Chg |
| D | Portfolio sample | analyst-quarter | Sector_HHI, Single_Sector, Sector_Covered, Firms_Covered, FQ1, FQ2, Brokerage_Size, Exp_General, Frequency, Promotion, Low_IndExp |
| E | Russell DID sample | analyst-firm-quarter-horizon | Revise, \|SUE\|, PostAssignment, switcher indicators |

Report N, mean, SD, p25, median, p75 for each. Report pre- and post-launch means side by side in Panels B through D; this costs nothing and pre-empts the "does |SUE| change post-launch" question (point 4). If the main text gets too long, keep Panels A and B in the paper and move C through E to the Online Appendix, but reference them explicitly at each table.

### Point 3: Economic significance for Tables 5 and 6, in the style of Table 7. Severity A.

**Is the referee right?** Yes. Table 7 has the one well-written magnitude sentence ("Given a sample mean Sector_HHI of approximately 0.42, this represents a 2.9 percent decrease"). Tables 4, 5, 6, 8, and 11 have none.

**What to do.** For each table, add one sentence using the template in Section 3. Specific notes:

- **Table 5.** The two components have different scales, so "one SD of |SUE|_Firm" and "one SD of |SUE|_Sector" must be reported separately. Also report the pre-launch baseline response to each component (the main effects) so the reader can see that the sector response goes from 0.142 to roughly 0.035 (a 75 percent reduction) while the firm response goes from about zero to 0.122. That framing is more compelling than the raw interaction coefficients.
- **Table 6 Panel A.** Be candid. The %FirmQ coefficient is 0.008 on a share whose mean is about 0.81 (6.52 / (6.52 + 1.54) from Section B), so the shift is about one percentage point of share. The cleaner way to present attention reallocation is to report the two counts separately: the number of industry-wide points should fall and the number of firm-specific points should rise. Add those as Columns (2) and (3) of Panel A. A decline in industry-wide questions is the direct test of "analysts stop asking about the sector because the ETF tells them."
- **Table 6 Panel B.** Report the SD of %FirmQ_Chg and compute the implied change in revision probability for a one-SD larger post-launch shift in question content.
- **Table 8.** FQ1 and FQ2 are percentile scores on [0, 1] with a mean near 0.5. A coefficient of 0.008 is 0.8 percentile points. Report it as "moving an average analyst from the 50th to the 50.8th percentile of accuracy across covered firms," and then translate into forecast-error terms using OA4-style raw AFE if available. If the raw-error effect is available and larger in relative terms, lead with that.

### Point 4: Do the information components themselves change after ETF launches? Severity A (the editor singled this out).

**Is the referee right?** Yes, and this is the most valuable comment in the report. The attention-reallocation story makes a second prediction beyond the response-coefficient results: if analysts incorporate sector information more fully into their forecasts once the ETF trades, then the sector-wide component of the *forecast error* should shrink post-launch, and the firm-specific share of the surprise should rise. Footnote 14 already says |SUE| falls post-launch in an untabulated test. That footnote should become a table.

**What to do.** New Table (proposed "Table 6" position, before the conference-call evidence, or as Panel B of Table 5):

1. Regress |SUE|_Sector, |SUE|_Firm, |SUE|, and the firm share |SUE|_Firm / (|SUE|_Firm + |SUE|_Sector) on Post_Launch with firm-by-cohort and forecast-horizon fixed effects, in the launch sample. Prediction: negative on |SUE|_Sector, small or zero on |SUE|_Firm, positive on the share.
2. Report the explained variance of Equation (5) pre versus post launch (the average R-squared or the average β̂ across announcers). Prediction: the sector aggregate explains less of the announcer's surprise post-launch.
3. Repeat (1) in the Russell sample: |SUE|_Sector should fall for R2000→R1000 switchers gaining sector ETF membership and rise for R1000→R2000 switchers losing it. This is optional but would tie the mechanism to the causal setting.

One caution to state in the paper: Equation (5) is estimated separately pre and post, so a decline in the sector component reflects both a smaller aggregate sector surprise and a lower announcer loading on it. Report both pieces (the aggregate sector SUE and β̂) so the reader can see which moves.

### Point 5: Table 8 discussed too briefly; add Low_IndExp interaction; justify specifications and controls. Severity A for 5 and 5a.

**Is the referee right?** Yes. Table 8 gets one paragraph. Table 7 Panel B has the experience interaction and Table 8 does not, which looks like an omission or a null result being hidden. The referee will assume the latter unless you show it.

**What to do.**

1. Add Panel B to Table 8: FQ1 and FQ2 with Post_Launch × Low_IndExp. Prediction: positive interaction. If the interaction is null, report it and say so; the story survives (inexperienced analysts diversify more without a quality penalty) but do not omit it.
2. Also add the OA4 split (existing versus newly covered firms) to the discussion in the text rather than just a footnote, since the referee found the quality results interesting.
3. Write a full paragraph on what Table 8 means for the conjecture: portfolio expansion did not degrade quality, which is what one expects only if the freed-up attention is real.

**5a, specification justification.** This applies to every table and it is currently missing everywhere. Add a sentence per table citing the source of the specification:

| Table | Specification source to cite |
|---|---|
| 3 | Bhojraj et al. (2020) for pair construction and controls (SIZE, INST_PERC, ANALYST_NO, BTM, LOSS, ROA); Clement et al. (2011) for the 10-day window |
| 4, 5 | Same controls; firm-by-cohort and analyst FE follow the stacked-cohort design (Gormley and Matsa 2011; Cengiz et al. 2019) |
| 6 | State the controls explicitly; the text currently says only "control variables" |
| 7 | Kini et al. (2009) and Sonney (2009) for the diversification measures; Clement (1999) for Brokerage_Size, Exp_General, Frequency; Hong and Kubik (2003) for Promotion as a career-concerns control |
| 8 | Hong and Kubik (2003), Hilary and Hsu (2013); state the controls |
| 10, 11 | Coles et al. (2022), Heath et al. (2022); explain why Table 11 has no firm-level controls (or add them) |

Also fix the "Controls: Yes" rows in Tables 6, 7 Panel B, 8, and 11 so that the note lists which controls are included. Right now Table 11 lists no controls at all and Table 7 Panel B says "Controls Yes" without showing them.

### Point 6: Cross-sectional tests in Table 6. Severity B.

**What to do.** Add Post_Launch × Low_IndExp to Panel A (%FirmQ and the two counts) and a triple interaction Post_Launch × %FirmQ_Chg × Low_IndExp to Panel B. Samples of 15,867 and 11,233 are large enough. If you add only one cross-section, use industry experience, since that is the one the referee asked for and it is the one that runs through the whole paper. Sector Exposure is the second candidate.

### Point 7: Strengthen the attention-reallocation evidence (forecasts within an analyst's portfolio should be less correlated). Severity A (editor's second area).

**Is the referee right?** Yes, and the suggested test is implementable with I/B/E/S alone. The logic: if analysts rely less on sector-wide information and more on firm-specific information, their forecast errors and revisions across same-sector firms should share less common variation.

**What to do.** Pick two of the following, both in the portfolio (analyst-quarter) sample around launches with analyst, broker, and year-quarter fixed effects:

1. **Within-analyst error correlation.** For each analyst-quarter, compute the average pairwise correlation (or the first principal component's share) of signed forecast errors across the sector firms the analyst covers, using a rolling eight-quarter window like FQ2. Regress on Post_Launch. Prediction: negative.
2. **Co-revision.** For each analyst revision after an announcer's EA, compute the fraction of the analyst's other same-sector firms revised on the same day (a sector-wide revision) versus revised alone. Prediction: post-launch, revisions become more idiosyncratic. This uses the launch sample you already have and directly reads as "analysts stop revising the whole sector in lockstep."
3. **Sector loading of analyst errors.** Regress each analyst's signed forecast error for firm i on the sector ETF's aggregate surprise; the loading should fall post-launch. This is the analyst-level analogue of the point-4 test.

Any of these makes a natural new Table in Section 4.2 or 4.3. Test 2 is the cheapest because it reuses the Revise data.

### Point 8: Conclusion too short; add broader implications and market impact. Severity B.

**What to do.** Expand to about one page: (i) restate the attention-reallocation finding in one paragraph; (ii) move the "countervailing benefit" framing from the current last paragraph up and develop it against Israeli et al. (2017) and Glosten et al. (2021), whose finding that ETFs impound systematic rather than idiosyncratic information is exactly the premise that frees analysts; (iii) discuss market implications: if analysts produce more firm-specific information, firm-specific price informativeness should improve, earnings-response coefficients on the firm-specific surprise component should rise, and post-earnings-announcement drift for follower firms should fall. You can offer these as conjectures. If you want one supporting test, a three-day market reaction to follower analysts' post-launch revisions (revision informativeness) is cheap and would answer the referee's "short-term market reaction" remark directly. Put it in the Online Appendix and cite it in the conclusion.

### Point 9: Similar variable names across analyst-level and firm-level tests; separate the summary statistics. Severity A (same fix as point 2).

**What to do.** Beyond the panelized Table 2, disambiguate the names. Revise is used for three different objects (firm-level in Table 3, analyst-level in Tables 4 through 6, and analyst-level in the Russell sample). Options: subscript them (Revise_F for the firm-level dummy, Revise_A for the analyst-level dummy) or keep the names but head each table with "Unit of observation:" and "Sample:" lines. The subscript approach is safer because the referee explicitly asked for "different labels." Same for |SUE|, which is defined identically but appears in four different samples with different distributions.

### Point 10: Title is generic. Severity C but free.

**Suggestions.** The referee wants the sector-to-firm shift in the title. Candidates, keeping "analysts" for discoverability:

- "Sector ETFs and the Reallocation of Analyst Attention from Sector-Wide to Firm-Specific Information"
- "Outsourcing the Sector: How Sector ETFs Redirect Analysts toward Firm-Specific Information"
- "Do Sector ETFs Free Analysts to Focus on Firm-Specific Information?"

The first is the safest for TAR. Whatever you pick, adopt "attention reallocation" as the paper's one-phrase identity and use it in the abstract's first sentence.

### Editor's own point: the "regulators are concerned about passive investing" sentence. Severity A because the editor raised it personally.

The editor is right, and the current sentence also misstates the cited source. Bhattacharya and O'Hara (2018) is about information linkages and fragility, not about herding into passive funds. Replace the second sentence of the introduction with something like: "A growing literature asks whether the growth of ETF trading weakens incentives to acquire firm-specific information, or otherwise impairs the incorporation of such information into individual security prices (Israeli, Lee, and Sridharan 2017; Bhattacharya and O'Hara 2018; Glosten, Nallareddy, and Zou 2021)." This also sets up the Grossman-Stiglitz paragraph more directly and makes the paper's "countervailing benefit" conclusion land harder.

### Editor's writing instruction. Severity A.

Concrete targets, beyond the magnitude sentences:

- Every results paragraph currently ends with a strong interpretive claim ("This confirms," "This establishes," "rules out confounding explanations," "powerful placebo test"). Cut the intensity by one notch throughout. Referees read over-claiming as a signal of weak evidence.
- Section 4 opens by restating the two explanations twice (pp. 22 and 23). Say it once.
- Run a proofreading pass for the mechanical items: "CAGR" is "compound," not "cumulative," annual growth rate; Table 2 lists SUE_LAG as a control but Table 3 does not report it and the text does not list it; "Revise" in Table 11 appears with a constant of 0.063 while the ETF-level mean is 0.73, so the Russell-sample revision rate needs to be reported and its lower level explained.

---

## 3. Magnitude sentence template (use for every table)

For a linear probability model with |SUE| in percentage points of price:

> "The coefficient of β on Post_Launch × |SUE| implies that, after a sector ETF launch, a one-standard-deviation larger announcer surprise (σ = X percentage points of price) raises the probability that a follower analyst revises within ten days by β × X = Y percentage points, relative to an unconditional post-launch revision rate of Z percent (a Y/Z percent relative increase). Before the launch the same surprise changes revision probability by only β₂ × X = W percentage points."

Worked example for Table 3 Column (1) with the numbers already in the paper (|SUE| SD = 0.004 in raw units, so 0.4 percentage points; Revise mean = 0.734):

> 0.037 × 0.4 = 1.5 percentage points on a 73.4 percent base, roughly a 2 percent relative increase.

This is the same quantity as the current "3.0 percent of a standard deviation" (1.5 / 0.442 = 3.3 percent), just stated in units the referee can use. Because |SUE| is skewed (mean 0.2, SD 0.4 percentage points), consider using the interquartile range instead of the SD; it usually reads as more credible.

For Table 4, the same arithmetic needs the launch-sample SD of |SUE| and mean of Revise, neither of which is reported. That is why the referee could not do it and why point 2 is severity A.

---

## 4. Issues the referee did not raise but will notice on the next read

1. **SUE_LAG** appears in Table 2 as a balanced control but is absent from Table 3's coefficient list and from the control-variable paragraph on p. 16. Either report it or drop it from Table 2.
2. **Table 7 Panel B main effect flips sign.** With the Low_IndExp interaction, Post_Launch becomes positive for Sector_HHI (0.010, t = 2.27) and Single_Sector, and negative for Sector_Covered. That means experienced analysts *concentrate* after launches. The text does not mention this. Offer an interpretation (experienced analysts deepen their sector specialization while inexperienced ones broaden) or the referee will supply a less flattering one.
3. **Table 11 has no controls** while every other revision table does. Either add the same controls or explain the omission in the note.
4. **Post_Launch main effect is negative** in Table 4 Column (1) (−0.023, t = −2.45): fewer revisions at zero surprise after launch. This is consistent with the story (less mechanical sector-driven revising) and worth one sentence; it also strengthens the point-7 co-revision test.
5. **"Establish a causal link" in the abstract** is strong for a Russell design where the ETF-membership first stage (Table 10) is itself an outcome. Consider "provide causal evidence consistent with."
6. **Gemini classification validation.** Section B reports an error rate but no human-coded validation sample. Add a 200-question hand-coded agreement rate. TAR reviewers of LLM-based measures increasingly ask for this.

---

## 5. Prioritized work plan

| Priority | Task | Addresses | Effort |
|---|---|---|---|
| 1 | Panelized summary-statistics table for all five samples, pre/post columns | 2, 9 | 1 to 2 days |
| 2 | Estimation-method paragraph, table notes, logit robustness (OA6) | 1 | 1 day |
| 3 | Magnitude sentences for Tables 3, 4, 5, 6, 8, 11 using Section 3 template | 1, 3 | 1 day after (1) |
| 4 | New table: sector and firm components of \|SUE\| pre vs post launch (tabulate Footnote 14) | 4, editor area 2 | 1 to 2 days |
| 5 | New table: within-analyst error correlation or co-revision test | 7, editor area 2 | 2 to 3 days |
| 6 | Table 8 Panel B with Low_IndExp; expand Table 8 discussion | 5 | half day |
| 7 | Table 6 with Low_IndExp interactions; add separate firm and industry counts | 6, 3 | 1 day |
| 8 | Specification-justification sentences and explicit control lists for every table | 5a | half day |
| 9 | Rewrite intro sentence 2, expand conclusion, soften claims, proofread | editor, 8 | 1 to 2 days |
| 10 | Retitle; rename Revise / \|SUE\| by level | 10, 9 | hours |
| 11 | Fix the six items in Section 4 | pre-emptive | half day |

Total: roughly two to three weeks of one person's time, most of it in items 4 and 5.

---

## 6. Suggested tone for the response letter

The referee is an ally. Open by thanking them for the summary-statistics and economic-significance points and say plainly that the previous draft under-served the reader on both. For points 4 and 7, present the new tables as tests the referee's reasoning suggested and that the results support (or, where they do not, say so and explain what it implies). Do not push back on any point; none of them warrants it. Where the t = 1.73 result is concerned, acknowledge the marginal significance, point to the stronger launch and Russell evidence, and let the reframed narrative carry the weight.

Run `/respond-to-referees` once the revised draft exists to generate the point-by-point response document from this plan.

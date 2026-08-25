# Pre-submission Review — *Social Alignment in the CEO Market: Evidence from Two-sided Matching*

**Target journal:** Journal of Accounting and Economics
**Manuscript:** `Prosocial_CEO_Matching_10.pdf`, 58 pp.
**Sample:** 689 CEO turnovers, 2007–2020
**Reviewed:** 25 August 2026

**Tally:** 4 critical text–table contradictions · 14 major · 21 minor/mechanical · 9 items on the Prosocial measure

---

## Summary

The paper is in good shape structurally and the model is well motivated. The problem is that the prose has not fully caught up with the rebuilt tables. There are four places where the text asserts the *opposite* of what the table shows, and one place where two tables report different values for the same object. Those are the things a referee will find in the first hour.

**What I verified as correct**, so you know the scope of the checking: the 18,329 inequalities equal Σ_t C(N_t,2) exactly; the year counts and industry counts both sum to 689 and the 402 / 286 / 1 sector split is right; the 3.1%, −8.9%, +13.6%, +4.9% and −12.5% counterfactual changes all reproduce from Table 7; the 4.06% random-accuracy benchmark is right; and Table C1's percentage shares are right given its own levels.

---

# A. Where the writing contradicts the tables

These are the ones to fix first.

## A1 — CRITICAL — Abstract, p.5, §4.3, Table 6

**The introduction reports a null for low-prosocial CEOs; Table 6 reports a significant positive effect.**

| Introduction, p.5 | Table 6, cols (3)–(4) |
|---|---|
| "we find **no relation** between social-dimension synergy and the pecuniary share for low-prosocial CEOs, consistent with social preference alignment generating no non-pecuniary payoff for these CEOs." | Δ(Social Score × Prosocial) = **+0.13\*\*\*** (t = 2.97) and **+0.08\*** (t = 1.71). Significantly *positive*, not null. |

There is a third version of this claim inside §4.3 itself: "low-prosocial CEOs experience disutility from social alignment and require a larger pecuniary share." So the paper currently says *null* (intro), *do not* (abstract), and *positive, driven by disutility* (§4.3) about one coefficient.

**Fix.** Adopt the table's result and propagate it. The abstract's "whereas low-prosocial CEOs do not" and the intro sentence both need rewriting to "low-prosocial CEOs require a *larger* pecuniary share." This is a more interesting result than the null — it is the compensating-differential prediction running in both directions. §4.3's closing sentence ("higher social-dimension synergy enables firms to transfer a smaller pecuniary share to the CEO") is then only true for the high-prosocial subsample. Separately, see C8: the "disutility" reading needs a statistically significant γ_l, which you do not have.

## A2 — CRITICAL — §5, p.31, Table 7 Panel B

**§5 says low-prosocial synergy "initially improves under mild shocks." Panel B shows it declining monotonically from the first step.**

| §5, p.31 | Table 7 Panel B, low-prosocial MV_fin |
|---|---|
| "For low-prosocial CEOs, productivity-dimension synergy **initially improves under mild shocks** but declines under broader mandates: the positive spillover effect weakens (MV_fin drops from 0.88 to 0.80)…" | A0 benchmark 0.88 · B1 bottom 20% 0.88 · B2 bottom 40% 0.87 · B3 bottom 60% 0.84 · B4 bottom 80% **0.80**. Never rises. |

Two errors in one sentence. There is no initial improvement, and a series that falls from 0.88 to 0.80 is not a "weakening positive spillover" — it is a negative spillover that strengthens with the size of the mandate. The high-prosocial series in the same panel (1.01 → 1.01 → 1.02 → 1.05) does behave as described.

**Fix.** Rewrite as a clean monotone contrast: as the mandate widens, productivity-dimension synergy rises steadily for high-prosocial CEOs and falls steadily for low-prosocial CEOs. That is a cleaner story than the one currently written, and it is what the table shows.

## A3 — CRITICAL — §5 closing, Intro p.6, Table 7 Panel A2

**The counterfactual section's concluding claim is contradicted by the panel it concludes.**

| §5, final sentence | Table 7 Panel A2 (S_f = 1) |
|---|---|
| "improving firms' social performance does not compromise the productivity dimension match synergy." | All CEOs 0.96 → **0.95** · High-prosocial 1.01 → 1.06 · Low-prosocial 0.88 → **0.77**. Aggregate −1.0%; low type −12.5%. |

The aggregate falls, and one of the two subsamples falls by 12.5%. The intro leans on this same sentence to argue the anti-ESG concern "is not necessarily warranted" — a referee reading Panel A2 will treat that as overreach and will discount the surrounding claims too.

**Fix.** State it conditionally: raising social scores *reallocates* productivity-dimension synergy toward high-prosocial CEOs (+4.9%) and away from low-prosocial CEOs (−12.5%), leaving the aggregate roughly unchanged (−1.0%). The distributional result is the finding; the "no cost" framing is not available to you.

## A4 — CRITICAL — Table 7 Panel A0 vs. Table C1 Panel A

**Two tables report different numbers for the same object — the observed match under the column (2) estimates.**

| Observed / empirical match | All CEOs | High-prosocial | Low-prosocial |
|---|---|---|---|
| MV_fin — Table 7, A0 | 0.96 | 1.01 | 0.88 |
| MV_fin — Table C1, Panel A | **0.93** | **1.05** | **0.73** |
| MV_soc — Table 7, A0 | 0.79 | 1.07 | 0.32 |
| MV_soc — Table C1, Panel A | **0.75** | **1.01** | 0.33 |

This is not a transcription slip. Each table is internally consistent with the 62% high-prosocial share — Table 7 gives 0.62(1.01) + 0.38(0.88) = 0.96, Table C1 gives 0.62(1.05) + 0.38(0.73) = 0.93 — so they are two genuinely different computations of the same quantity. Most likely one was regenerated on the new *Prosocial* measure and the other was not.

**Fix.** Rerun both from a single script and confirm they agree. This is exactly the kind of thing a replication-minded referee or the JAE data editor will check, and an unexplained mismatch between the appendix and the counterfactual undermines the counterfactual.

## A5 — MAJOR — Appendix C, p.54, Table C1

**The Appendix C text quotes the productivity column while describing the social column.**

| Appendix C, p.54 | Table C1 Panel A shares |
|---|---|
| "The match values based on **social-related attributes** of observed firm-CEO pairs account for approximately **26.4%** of the total match values and are even higher in groups with high-prosocial CEOs (**27.6%**)." | MV_fin **26.4%** / high **27.6%**; MV_soc 21.3% / high 26.5%. Both quoted figures are MV_fin. |

**Fix.** The social shares are 21.3% (all) and 26.5% (high-prosocial). The qualitative point — that the social share is higher among high-prosocial CEOs — survives, and is actually stronger with the right numbers (26.5% vs 10.9% for low-prosocial).

## A6 — MAJOR — §4.2.2, p.26, Table 5

**Two consecutive sentences in §4.2.2 make opposite claims about MV_fin at t+1.**

| §4.2.2, consecutive sentences | Table 5, col (1) |
|---|---|
| "…MV_fin exhibits a **marginally positive** association with performance in year t+1…" then "The **absence of significant effects** in year t+1 for both MV_soc and MV_fin may reflect transitional frictions…" | MV_fin 0.10 (t = 1.32). No stars. p ≈ 0.19. Not marginal by any convention. |

**Fix.** Delete "marginally positive." It reads like a survivor from the pre-update tables, which is precisely the class of error a referee treats as a signal about the rest of the paper.

## A7 — MAJOR — Table 5, compensation row

**Table 5's compensation row is labeled `Scomp`, but the equation, the text, and Table 5's own note all say it should be `Fcomp`.**

Equation (16) has `Fcomp`. §4.2.2 says "we examine the effects of financial compensation (Fcomp)." Table 5's note says "natural logarithm of financial-performance based compensation awarded to the CEO (Fcomp)." The row header says `Scomp`. Worth confirming which variable was actually estimated — the coefficients (0.01\*, 0.01\*\*, 0.01\*\*) are close enough to Table 4's `Scomp` row (0.01\*, 0.01\*, 0.01\*) that the wrong variable being run is a live possibility.

## A8 — MAJOR — §3.1, Table A1

**The initial sample size in the text appears nowhere in Table A1.**

§3.1 says "Our initial sample comprises **2,271** CEO turnover events identified from ExecuComp and successfully matched with BoardEx profiles." Table A1 Step 1 reports **2,467**; Step 3 reports 2,282; the attrition base is 2,123. The figure 2,271 does not appear. (The internal arithmetic of Table A1 is fine: 689 + 1,434 = 2,123.)

## A9 — MAJOR — §3.1, Table 1 Panel C, Appendix B

**The *Prosocial* range is stated three ways; only one is right.**

§3.1 says scores range "from 1 to 16." Table 1 Panel C reports min 0.00, max 15.00. Appendix B's scheme is 5 organization tiers × 3 role levels = 15, plus 0 for no recorded affiliation. Appendix B and Table 1 are right; §3.1 is wrong. Given the measure is new, this is the first thing a referee will check.

## A10 — CRITICAL — Table 1 Panel C note

**The reported mean of `1{High Prosocial}` is arithmetically impossible under its stated definition.**

| Table 1 note | Table 1 Panel C |
|---|---|
| "1{High Prosocial} is an indicator equal to one if the CEO's prosocial score is **above the calendar-year average**." | Prosocial mean 5.79 · Prosocial median 3.00 · 1{High Prosocial} mean **0.62**. Mean > median ⟹ ≤50% above mean. |

When the mean exceeds the median, at most half the sample can lie above the mean. With a median of 3 against a mean of 5.79 on a strongly right-skewed 0–15 score, the true share above the mean is closer to 30–40%. Year-to-year variation in the annual mean cannot bridge that gap. So either the note's definition is wrong, or the indicator was built on a different variable (the CDF rank, perhaps, where a median split would give 0.50 — still not 0.62).

**Fix.** Resolve this before anything else in the measurement section. Every γ_h / γ_l estimate in Table 3, every subsample in Table 6, and every subsample column in Tables 7 and C1 depends on this one split. If the split is not what the note says it is, the type-heterogeneity results are all mis-described.

## Smaller mismatches in the same family

- **A11 — Minor — Intro p.6 vs §5 p.30.** The introduction reports a **12.1%** decrease for low-prosocial CEOs; §5 and Table 7 give **12.5%** (0.88 → 0.77). The +4.9% figure matches in both places.
- **A12 — Minor — §3.2, Table 1 Panel B.** "except for the two industries with fewer than three firm-CEO pairs" — only SIC 0 has fewer than three (n = 1). SIC 9 has exactly 3, and it is the other out-of-range industry (0.86). Say "the two smallest industries (SIC 0 and SIC 9, n = 1 and 3)."
- **A13 — Major — §4.2.1, Table 4.** "The association disappears" describes a change in significance, not in magnitude. The `Scomp` coefficient is **0.01 in both** column (2) and column (3); only the t-statistic moves (1.96 → 0.49). Same at t+2 (1.93 → 1.17) and t+3 (1.83 → 0.60). The paper's headline — "CEO selection dominates incentive provision" — therefore rests on a difference in significance, which is not a significant difference. *Fix:* report `Scomp` to three or four decimals and test the difference directly. Without that, this is the softest load-bearing sentence in the paper.
- **A14 — Minor — Table 4 title.** Titled "Match Value and *Changes* in Social Performance," but the dependent variable is the *level* of Social Score at t+n. Table 5 is correctly titled. Either retitle or re-specify in changes — and see C2, where specifying in changes would also address a substantive problem.
- **A15 — Minor — §3.1, §4.2.2, Table A2.** `Fcomp` has two incompatible definitions: the text says "the natural logarithm of the CEO's total compensation minus Scomp" (i.e. log(C) − log(1+S)); Table A2 says "log(1 + total compensation − social compensation)."
- **A16 — Minor — Equation (16).** The left-hand side is written `ROA_{i,t+n}` (a level) while the text and Table 5 define it as a percentage change over n years. Write it as Δ%ROA_{i,t→t+n}.
- **A17 — Minor — Table 6.** Two different rows are both labeled `Δ Size`, with coefficients 0.04\*\*\* and 0.58\*\*\*. One is mislabeled.
- **A18 — Minor — Table C1 title.** The title promises "observed, random, *optimal*, and *counterfactual* firm-CEO pairs"; only Panels A (real) and B (random) exist. Leftover from an earlier draft.

---

# B. The new Prosocial measure

The scheme in Appendix B is careful and well documented, but it is doing more work than the paper acknowledges, and three of its properties are exposed.

## B1 — CRITICAL — Appendix B, tier 5

**The bottom of the scale encodes a data-matching failure, not low prosociality.**

Appendix B's lowest tier is "Recorded organizational affiliation that *cannot be matched* to the IRS EO BMF," scoring 1–3. Score 0 is "no recorded external organizational affiliation." So a CEO who chairs a foreign NGO, sits on a non-US university board, serves a private operating foundation outside the EO BMF, or whose BoardEx organization string simply fails to string-match, lands at the very bottom of the distribution — pooled with genuinely uninvolved CEOs.

Because *Prosocial* enters the estimation as an annual CDF rank, this compresses the bottom of the distribution and is a textbook attenuation channel on β. It also interacts badly with A10: if the high/low split sits anywhere near the bottom mass, some "low-prosocial" CEOs are just unmatched records.

**Fix.** Report the share of CEOs falling in each of the five organization tiers — this is one small table and it will pre-empt the question. Then re-estimate Table 3 (a) dropping CEOs whose only affiliations are unmatched, and (b) treating unmatched affiliations as missing rather than as a low score. If β is stable, say so in a footnote and the issue is closed.

## B2 — MAJOR — Appendix B p.53, §3.1

**The score is a maximum, so it measures the strongest single affiliation — but §3.1 sells it as measuring engagement.**

| Appendix B | §3.1 |
|---|---|
| "we assign each CEO the **maximum** affiliation-level score across all distinct organizations." | "Higher scores indicate affiliations with highly charitable organizations **and elevated engagement**." |

Under a max rule, a CEO with one 501(c)(3) chairmanship and a CEO with eight of them score identically at 15. That is a defensible design choice — it is robust to BoardEx coverage differences across CEOs — but it is not a measure of engagement intensity, and the paper should not claim it is.

**Fix.** Soften §3.1 to describe what the max captures (the quality of the CEO's strongest charitable commitment), and add a count- or sum-based variant as robustness. If both give the same β, that is a genuinely useful validation of the ordinal scheme.

## B3 — MAJOR — §3.1, p.18

**The relationship to Feng et al. (2024) is asserted, not specified — and the paper reads as though the measure never changed.**

§3.1 says the measure is constructed "following Feng et al. (2024)," but the tiered IRS-subsection × classification-code × role scheme in Appendix B is your own. Since Feng et al. is the closest paper to yours (and is currently discussed in footnote 4), a referee will want the comparison made explicitly rather than folded into a "following."

**Fix.** Three things, all cheap: (1) state in one sentence what is borrowed (the BoardEx → IRS EO BMF linkage) and what is new (the ordinal weighting by charitable status and role seniority); (2) report the correlation between your score and the Feng et al. measure; (3) re-estimate Table 3 on the Feng et al. measure as a robustness column. Given the tables were just rebuilt on the new measure, (3) is the check that closes the question.

## B4 — MAJOR — Appendix B closing, Table 1 Panel C, Table 2

**Appendix B's ordinality caveat is orphaned — and two tables violate it.**

Appendix B ends: "Because the score is ordinal, the numerical distance between two scores should not be interpreted as an equal difference in the CEO's underlying psychological prosociality." That caveat is *satisfied* by the CDF-rank transform used in Tables 3, 6, 7 and C1 — a monotone transform of an ordinal score is fine. But it is *violated* by Table 2, which enters raw *Prosocial* (0–15) linearly and interacts it linearly with Social Score, and by Table 1 Panel C, which reports a mean and standard deviation of an ordinal variable.

**Fix.** Move the caveat forward into §3.1 and immediately resolve it: say that the CDF transform is precisely why the ordinality is not a problem for the structural estimates. Then either re-run Table 2 on CDF ranks for consistency, or add a line acknowledging the linearity assumption there. Right now the caveat sits in an appendix with no connection to any empirical choice, which reads as a hedge rather than a design decision.

## B5 — CRITICAL — §3.1 p.17, Appendix B

**Nothing in the paper establishes that affiliations are measured before the appointment.**

§3.1 asserts that "CEO characteristics are based on the incoming CEO's background observed prior to appointment." For *Talent*, *Experience* and *Education* that is straightforward. For *Prosocial* it is not: BoardEx organizational affiliations frequently carry unreliable or missing start dates, and charitable board seats very often arrive *with* the CEO job rather than before it — a newly appointed CEO of a large firm is immediately recruited onto local nonprofit boards.

If post-appointment affiliations leak into the score, two results are contaminated at once: the matching estimate β (the CEO's "type" is partly an outcome of the match) and the Table 4 social-performance result (prosocial CEOs at high-ESG firms accumulate more board seats).

**Fix.** State explicitly in §3.1 or Appendix B whether affiliations are restricted to those with a start date strictly before the appointment year, and how affiliations with missing dates are handled. If they cannot be dated, say what fraction that is and show the estimates hold on the datable subsample. This is the single most attackable property of the new measure — a paragraph here is worth more than any other addition in the paper.

## B6 — MAJOR — Table 1 Panel C

**The distribution is strongly bimodal, which is never shown and matters for the type split.**

Median 3, 75th percentile 12, mean 5.79, SD 5.48 on a 0–15 scale. That is a distribution with mass near the bottom (no affiliation / unmatched / member-level) and mass near the top (leadership in a pure 501(c)(3)), with relatively little in between — which is exactly what the tier structure would generate. A binary type model is arguably *well suited* to this, and that is a point in your favor that the paper is not making.

**Fix.** Add a histogram or the five tier frequencies, and use the bimodality affirmatively: it justifies the two-type specification in §2.2 rather than leaving it as a modeling convenience. Then show robustness of γ_h/γ_l to a median split and to a substantive cut (e.g. score ≥ 10, i.e. any successfully-matched 501(c)(3) affiliation).

## B7 — MAJOR — §2.2, §3.1, §4.1

**The high/low prosocial threshold is defined only in a Table 1 footnote.**

γ_h and γ_l are introduced in §2.2, used throughout §4 and §5, and the split governs every subsample in the paper — yet the only statement of what "high-prosocial" means is in the note to Table 1, forty pages later. A reader following the model into the results has nowhere to look.

**Fix.** State the rule where the types are introduced (§2.2), restate it in §3.1, and resolve A10 at the same time.

## B8 — MINOR — §3.1, §2.2, Table A2

**The firm-side social variable has three names and two different content descriptions.**

*Content:* §3.1 says the Refinitiv Social Pillar covers "employee development, human rights, community involvement, and diversity and inclusion"; Table A2 says "workforce, community engagement, human rights, and product responsibility." Use Refinitiv's actual category list, once.

*Naming:* §3.1 calls it "Firm social preference," §2.2 and §4 call it "social orientation," Table 1 and Table A2 call it "social performance." These are three different constructs in the ESG literature — a *preference*, an *orientation*, and a realized *performance score*. Since the paper's contribution is about preference alignment, and the measure is a performance score, the gap between them is exactly what a skeptical referee will press on. Pick one term for the construct ("social orientation") and one for the measure ("social performance score"), and add a sentence defending the proxy.

## B9 — MINOR — §3.1, Table A2

Refinitiv/LSEG has retroactively restated historical ESG scores, and this is documented in the literature. Since the entire social dimension rests on this variable across 2007–2020, name the download vintage and, ideally, note whether results hold on a fixed vintage or an alternative provider.

---

# C. What a JAE referee will push on

Roughly in the order I expect them to come up in a report. C1, C2 and C11 are the ones I would prepare for most carefully.

## C1 — CRITICAL — Tables 4, 5, 6

**The social-dimension results in Tables 4–6 are a rescaling of S_f × S_m. The structural estimation contributes nothing to them.**

MV_soc = β̂ · S_f · S_m, and β̂ is a single constant. Regressing on MV_soc is therefore numerically identical to regressing on the raw interaction S_f × S_m, up to a scale factor on the coefficient. **The t-statistics are literally unchanged.** Every social-dimension result in Tables 4, 5 and 6 could have been produced without estimating the model at all.

MV_fin is different — it weights three interactions by α̂₁, α̂₂, α̂₃, so it is a genuine estimated composite that a reduced-form researcher could not construct.

**Fix.** Say this yourself, in the text, before a referee says it. Frame the consequences tests as using the structural estimates to build the *productivity* composite and to *weight the two dimensions against each other*, and be explicit that the social-dimension coefficient is a rescaled interaction. The honest version of this is not damaging; being caught overselling it is.

## C2 — CRITICAL — Table 4, Table 5

**Table 4 is close to mechanical: the dependent variable is Social Score_{t+n}, the regressor contains Social Score_t, and the level of Social Score_t is not controlled for.**

Refinitiv social scores are highly persistent. MV_soc = β̂ S_f S_m contains S_f multiplicatively, and the specification includes no control for S_f. A coefficient of 0.19 with t = 13.26 and R² = 0.69 is what persistence looks like, not what a match-synergy effect looks like. The controls (Size, RD, Advertising, Tangibility, Leverage, FCF, Sales Growth) do not touch this.

The same omitted-levels problem applies to Table 5 in the other direction: the negative MV_soc coefficient may simply be that high-ESG firms have lower subsequent ROA growth — a well-documented pattern that has nothing to do with matching.

**Fix.** Two changes, both standard. (1) Control for the *levels* of S_f, S_m, W_f and W_m so the interaction is identified off the interaction rather than off its components — this is the standard requirement for interpreting an interaction term and its absence will be the first methods comment. (2) In Table 4, control for Social Score_t directly, or specify the model in changes, which also fixes the title problem in A14. If the 0.19 survives with S_f controlled, the paper is much stronger. If it does not, better to know now.

## C3 — MAJOR — Table 3, Table C1, Appendix C

**Over half the estimated match value is the same-industry dummy, and the model validation is mostly that dummy.**

| Component of total match value | Real match | Random match | Share of real |
|---|---|---|---|
| MV_fin (three productivity pairs) | 0.93 | 0.85 | 26.4% |
| MV_soc (social pair) | 0.75 | 0.73 | 21.3% |
| ξ̂ × 1{Same Industry} | **1.84** | 0.52 | **52.3%** |
| **Total MV** | 3.52 | 2.10 | 100% |

ξ̂ = 6.25 dwarfs β̂ = 2.46 and α̂₁ = 2.51. The residual 1.84 is exactly 6.25 × 0.294, the sample mean of the same-industry dummy, confirming the decomposition. Of the 1.42 gap between real and random total match value, **1.32 comes from the industry dummy**. Note too that MV_soc under random matching (0.73) is almost identical to the real match (0.75) — on this metric, random assignment achieves nearly the same social-dimension match value as the observed market.

**Fix.** Report the real-vs-random comparison with and without ξ̂·Ind, and discuss why the industry control dominates. The out-of-sample exercise (C22) is the stronger validation; lead with it.

## C4 — CRITICAL — §2.3, §4.1

**The paper's central comparison rests on an incorrect inference rule.**

§2.3 states: "If two coefficients' confidence intervals overlap, the two coefficients are not significantly different." Overlap does not imply no difference; non-overlap does imply a difference. The rule is conservative in one direction only.

§4.1 uses exactly this rule to establish the paper's headline claim — that β is "not significantly different" from α₂ in column (1), and "on par with" α₁ in column (2).

**Fix.** You already have the machinery — Table 3 reports a subsampled CI for γ̂_h − γ̂_l. Do the same for β̂ − α̂₁ and β̂ − α̂₂ and add them as rows. This is a small computational change that converts the paper's main claim from a rule-of-thumb into a real test, and it will read as a strength.

## C5 — MAJOR — Table 3, cols (1) vs (2)

**β more than triples across specifications while α₁ barely moves, and this is not discussed.**

| Parameter | Col (1) | Col (2) | Change |
|---|---|---|---|
| β̂ — Social Score × Prosocial | 0.73 | 2.46 | **×3.4** |
| α̂₁ — Assets × Talent | 2.33 | 2.51 | ×1.1 |
| α̂₂ — Division × Experience | 0.77 | 0.84 | ×1.1 |
| Inequalities satisfied | 40.19% | 41.39% | +1.2pp |

Adding the non-pecuniary payoff changes the headline parameter by a factor of 3.4 while improving fit by 1.2 percentage points for three extra parameters. The two columns also support materially different claims — in column (1), β is comparable to the *weakest* productivity pair; in column (2), to the *strongest*. The abstract and introduction assert the column-(2) version; §4.1 leads with column (1).

**Fix.** Explain why introducing NP raises β, lead §4.1 with column (2) so the text matches the abstract, and be precise: β is comparable to the firm size–CEO talent complementarity specifically, not to "skill-productivity complementarities" generally — it is three times α₂ and opposite in sign to α₃.

## C6 — MAJOR — §2.3, Table 3

**Goodness of fit is reported without a benchmark, and it looks worse than a coin flip.**

"Satisfied inequalities: 40.19% / 41.39%." Because the objective in Eq. (12) counts the *joint* satisfaction of two inequalities, the correct random benchmark is roughly 25%, not 50% — so 41% is a real improvement. But the paper never says this, and a referee reading "40% of inequalities satisfied" against an unstated 50% prior will conclude the model fits badly.

**Fix.** State the null benchmark explicitly, and ideally simulate it (draw random parameter vectors, report the distribution of the objective). One sentence removes a serious misreading.

## C7 — CRITICAL — §5, footnote 11

**The counterfactual's headline result follows from the sticky-reservation-utility assumption, not from the estimated preferences.**

Footnote 11 holds each CEO's empirical total payoff — pecuniary *and* non-pecuniary — fixed as their reservation utility. Trace the two scenarios through that assumption:

- **A1 (S_f = 0):** high-prosocial CEOs lose their NP but keep a reservation utility that *included* it. They mechanically cannot rematch. Their productivity synergy falls 8.9%.
- **A2 (S_f = 1):** high-prosocial CEOs gain NP at every firm, so the constraint slackens and they rematch freely. Their productivity synergy rises 4.9%.

Both results are implied by the assumption before any parameter is estimated. The paper effectively says so — "a high-prosocial CEO is less likely to rematch because the potential firms need to offer the total pecuniary pay that at least beats the CEO's existing payoff from both pecuniary and non-pecuniary components" — but then presents the consequence as an economic spillover with policy content.

**Fix.** Add a scenario in which reservation utilities are recomputed under the counterfactual environment (or bounded), and report how much of the spillover survives. Failing that, drop the policy language in the introduction ("this concern is not necessarily warranted") and present §5 as a comparative-statics exercise conditional on sticky outside options. As written this is the section most likely to draw a rejection-grade comment.

## C8 — MAJOR — §4.3, §5, Table 3

**The low-prosocial mechanism requires γ_l < 0, which is not statistically distinguishable from zero.**

| §5 and §4.3 assert | Table 3, col (2) |
|---|---|
| "they experience non-pecuniary **disutility** for working at firms with high social scores, which raises their required pecuniary pay…" | γ̂_l = −0.23, 95% CI (−0.63, **0.53**). Insignificant. |

§4.1 states this correctly ("low-prosocial CEOs do not" obtain non-pecuniary payoffs). §4.3 and §5 then quietly upgrade the insignificant point estimate into an economic mechanism, and the entire low-prosocial counterfactual result depends on it.

**Fix.** Run the counterfactual at γ_l = 0 as the baseline and report γ_l = −0.23 as a bound. If the low-prosocial decline vanishes at γ_l = 0, that is important to know and to disclose. Either way, harmonize the language across §4.1, §4.3 and §5.

## C9 — MAJOR — §5, footnote 11

**The model is transferable-utility; the counterfactual uses a non-transferable-utility algorithm, on an incorrect justification.**

Footnote 11 states that "GS algorithm ensures that new stable matches maximize the aggregate matching values from all pairs." That is not a property of deferred acceptance. Under transferable utility the stable assignment *is* the surplus-maximizing assignment, but it is found by solving the assignment problem (linear programming / Hungarian algorithm), not by running firm-proposing DA. DA delivers a stable match under *non-transferable* utility, and the firm-optimal one at that.

**Fix.** Either solve the assignment problem directly — it is a few lines with any LP solver at N ≤ 72 per market — or state that DA is used as an approximation, justify it, and show the two agree on the empirical benchmark.

## C10 — MAJOR — §5, footnote 12

**S_f = 0 is given two incompatible interpretations within the same section.**

§5 describes S_f = 0 as "effectively shutting down the social preference channel." But footnote 12 argues that CDF ranks proxy for actual social practice, so that S_f = 1 means "all firms raising their actual social practices to the best level observed." By that same logic S_f = 0 means all firms adopting the *worst* observed practice — not that the channel is absent. The abstract compounds this by describing A1 as shutting down "the non-pecuniary payoffs related to social preference," when in fact it zeroes the whole social dimension including βS_fS_m.

**Fix.** Pick one interpretation of the CDF and apply it to both scenarios. If you want a true "shut down NP only" counterfactual (which is what the abstract promises), set γ_h = γ_l = 0 and leave S_f at its empirical values — that is a cleaner and more interpretable experiment than S_f = 0, and it isolates exactly the channel the paper is about.

## C11 — CRITICAL — §2.2, §4.1, §4.3, Abstract

**The units of P are never stated, and the abstract's "pecuniary share of match synergy" may not be a share.**

§2.2 says only that P_fm is "linked to the CEO m's total compensation, assuming risk neutrality." §4.1 says all firm and CEO characteristics are annual CDFs. Table A3's note says "Tcomp is the annual CDF of total compensation." The three readings have different consequences:

- If P is **log compensation**, risk neutrality is contradicted — log utility over money is risk aversion.
- If P is **dollars**, then MV is denominated in dollars and estimates of 2.46 and 6.25 are implausible.
- If P is a **CDF rank in [0,1]**, then Δ(P / MV) in Table 6 is a compensation *percentile* divided by an estimated match-value index. That is not a share of anything, cannot be read as a fraction, and is not bounded by 1.

The abstract, the introduction, and §4.3 all describe this object as "the pecuniary share of total match value" that the CEO "captures." If P is a rank, that language is not supportable.

**Fix.** State the units of P precisely in §2.2, reconcile them with the risk-neutrality assumption, and then re-calibrate the interpretive language in the abstract and §4.3 to match. This is the claim most exposed to a referee, because it sits in the abstract's third sentence and can be checked in five minutes.

## C12 — MAJOR — Table 6

**Table 6's standard errors ignore the pairing structure.**

The 5,624 and 1,418 observations are constructed from 689 matches, so each match appears in many rows and the observations are heavily dependent. Robust-only standard errors are not appropriate here, and t-statistics of 18.76 and 10.21 are not credible under any plausible dependence structure. Two-way cluster on f and f′.

## C13 — MAJOR — Table 6

**How a *pair* is assigned to a prosocial subsample is never stated, and the counts do not match the obvious rule.**

With 62% high-prosocial CEOs, both-high pairs should outnumber both-low pairs by about 2.7:1 (0.62² vs 0.38²). The reported ratio is 4.0:1 (5,624 vs 1,418). Under a "type of the first CEO" rule it would be 1.6:1. Neither matches, which suggests either a filtering step that is not described (the positive-synergy and non-negative-reserve-value screens are not type-neutral) or an inconsistency in the type assignment. Given A10, worth checking directly.

## C14 — MINOR — Tables 4, 5, 6

**Generated regressors.** MV_fin carries estimation error from α̂ into the second-stage regressions, but the reported standard errors treat it as data. Per C1 this does not bite for MV_soc (a pure rescaling), but it does for MV_fin. A bootstrap over the subsampling draws would settle it, and it is a natural thing to add given you already run 100 subsamples.

## C15 — MAJOR — Table 3, Tables 4–6

**α̂₃ is negative and never mentioned.**

Table 3 column (2) gives R&D × Education = −0.34 — by the paper's own sign convention in §2.2, firm R&D intensity and CEO technical education are *substitutes*. That contradicts Pan (2017), whom you cite as the source of this pair, and it means MV_fin — the regressor in Tables 4, 5 and 6 — embeds a negative weight on one of its three components. Neither fact is discussed anywhere. Add a sentence, even if only to note the interval covers zero.

## C16 — MAJOR — §3.3, p.20–21

**The Table 2 paragraph argues against itself within four sentences.**

It first reads the negative Assets × Talent and RD × Education coefficients as evidence of "a diminishing marginal effect between the two factors" — a claim about production technology. It then argues, correctly and at length, that pay is an equilibrium transfer and that interaction coefficients in a pay regression cannot identify production. The first reading contradicts the second, and it also sits badly against Table 3, where the same pair gets α̂₁ = +2.51.

Two smaller things in the same paragraph: RD × Education is significant only at the 10% level in both columns, so "both negatively significant" overstates it; and Eq. (14) shows both year and industry fixed effects although Table 2 column (1) has year effects only.

**Fix.** Delete the production reading and let the transfer argument carry the paragraph. It is the better argument and it is the one that motivates the structural model.

## C17 — MINOR — §2.1

**Market definition.** Each calendar year's turnover cohort is treated as a closed market with no unmatched agents. With 24–72 matches per year, this rules out the outside option and treats a CEO hired in January and one hired in December as competing for the same positions. Pan (2017) has the same structure, so cite the precedent and add a defensive sentence rather than leaving it to a referee.

## C18 — MINOR — §3.1

**Sample endpoints.** Why 2007 (Refinitiv coverage? Incentive Lab?) and why 2020 (the need for t+3 outcomes?) are never stated. One sentence each. Relatedly, Table A1 Step 8 drops zero observations, yet footnote 9 says `Scomp` is missing for roughly 270 firm-years post-hiring — worth one clause reconciling those.

## C19 — MINOR — §2.3

**The "non-interactive terms cancel" claim is only half true as stated.**

In the pairwise-swap condition — the *sum* of (8) and (9) — any additively separable firm- or CEO-specific term cancels. But Q in Eq. (12) counts the two inequalities separately as an intersection, and within inequality (8) alone a CEO-specific additive term does not cancel (m appears on the left, m′ on the right). The claim holds for firm fixed effects; restate it precisely rather than as a general property.

## C20 — MAJOR — §2.3, Table 3 CIs

**The confidence intervals are strikingly asymmetric, with several point estimates sitting at their lower bound.**

| Parameter | Estimate | 95% CI | Distance to lower bound |
|---|---|---|---|
| β̂ | 2.46 | (2.02, 7.50) | 0.44 vs 5.04 above |
| α̂₁ | 2.51 | (2.02, 3.99) | 0.49 vs 1.48 above |
| γ̂_h | 0.41 | (0.23, 2.01) | 0.18 vs 1.60 above |
| γ̂_h − γ̂_l | 0.64 | (0.62, 1.61) | 0.02 vs 0.97 above |

Every interval is right-skewed and several point estimates essentially touch the lower bound — γ̂_h − γ̂_l = 0.64 against a lower bound of 0.62. That pattern means the subsample estimates are systematically *larger* than the full-sample estimate, which is not what a well-behaved subsampling distribution looks like. It could be a genuine feature of the partially-identified set, a small-subsample bias, or an artifact of the recentering in Eq. (13). A referee will ask.

**Fix.** Explain the asymmetry. Also state whether N in n_k = ⌊N/2⌋ counts matches or inequalities, whether draws are stratified by matching market, and note that n/N = 1/2 is a large subsample fraction relative to the n/N → 0 that subsampling theory assumes. Reporting results for a couple of smaller rates would close this.

## C21 — MAJOR — §4.2.2 vs §5 vs Intro p.6

**Table 5 and Table 7 point in opposite directions and the paper never reconciles them.**

Table 5: social-dimension synergy *lowers* future ROA. §5 and the introduction: raising social scores does not hurt (and for high-prosocial CEOs helps) productivity-dimension match synergy, which is used to argue the anti-ESG concern "is not necessarily warranted." These are different objects — realized accounting performance versus an estimated match-value index — but no reader will make that distinction unaided, and as written the paper appears to argue both that social alignment is financially costly and that it is not.

**Fix.** Add a short bridging paragraph at the end of §5 distinguishing the two objects explicitly, and soften the introduction's policy sentence. The defensible synthesis is: social alignment is costly in realized financial performance, but a market-wide rise in social scores would not further degrade the *allocative* quality of CEO matching for prosocial CEOs — while degrading it for others (per A3).

## C22 — MINOR — §4.1, Appendix C

**The first validation is close to circular; the second is the real one.**

"The average match value in the real data is higher than that under random matching, suggesting that our model can better capture the true matching process" — the parameters were chosen to satisfy stability inequalities *at the observed matches*, so this comparison is largely mechanical (and per C3, mostly the industry dummy). The out-of-sample exercise (8.43% vs 6.61% logistic vs 4.06% random) is genuine evidence. Lead with it, and replace "significantly outperforms" with an actual paired test across the 30 splits — you have the replications, so this costs nothing.

## C23 — MAJOR — Introduction / framing

**The paper is framed for a finance/labor audience, not a JAE one.**

The introduction opens on CEO labor economics and stays there for six pages. The accounting content is present but buried: the reliance on *reported* ESG measurement (with all its measurement error — see B9), the contracting result pitting `Scomp` against selection, and the disclosure-regulation literature that appears only in footnote 10. Chen, Hung & Wang (2018, JAE), Christensen, Hail & Leuz (2021), and Cohen et al. (2023, JAR) are all cited but none of them shape the framing.

**Fix.** Bring the measurement and contracting angles into the first two pages. The strongest JAE hook you have is the §4.2.1 result — that selection substitutes for explicit ESG-linked incentive contracts — and it currently appears on page 4 as the second of several findings. Consider leading with it. (Do fix A13 first, since that claim rests on a difference in significance.)

## C24 — MAJOR — §6 Conclusion

**The conclusion overclaims in three places and omits limitations entirely.**

- "social firms benefit **reputationally** from prosocial CEOs" — you measure Refinitiv social scores, not reputation. Nothing in the paper speaks to reputation.
- "these benefits often **do not extend** to financial performance" — you find a *negative* association, which is stronger and more interesting. Understating your own result here is odd given the abstract states it correctly.
- "our study **introduces** the maximum score method … a **novel** approach in the accounting literature" — footnote 3 cites Li, McNichols & Raghunandan (2025) in *The Accounting Review* applying MSE to the audit market. The footnote's hedge (their main results use an NTU model) does not rescue "introduces" or "novel." Say "among the first" and cite them in the text rather than only in a footnote.

The conclusion also contains no numbers and no limitations paragraph, despite §3.1 honestly flagging that the estimation sample skews toward large, well-covered firms. That caveat belongs in the conclusion where readers will actually see it.

---

# D. Writing, structure, and mechanics

The prose is generally clear and the paper is well organized. These are the things that would tighten it.

## Structure

**The introduction runs long and repeats itself.** Six pages before the contributions block, and then the three contribution paragraphs restate the findings paragraphs almost sentence for sentence. Roughly a page is recoverable by rewriting each contribution as *what is new relative to the closest paper in that strand* rather than as a restatement of your results.

**Footnote 4 is doing load-bearing work.** Feng et al. (2024) is the closest paper to yours, and the paragraph distinguishing your design from theirs — which is a good paragraph — sits in a footnote on page 5. Move it into the text.

**The §3.1 paragraph on Scomp and Fcomp is misplaced.** It appears in the middle of the structural-variable construction, where the reader expects the definition of P_fm, but Scomp and Fcomp are used only as controls in Tables 4 and 5. Either move it to §4.2, or use it to define P properly and resolve C11.

## Terminology drift

Standardize these — each currently appears in more than one form:

| Appears as | Where | Pick one |
|---|---|---|
| SocialScore / Social Score / S Score | §3.1, Tables 1–7 | `Social Score` |
| social preference / social orientation / social performance | throughout | orientation (construct), performance score (measure) |
| Assets vs. Size | Tables 2–3 vs. Tables 4–6 | one label for one variable |
| R&D × Education vs. RD × Education | Table 3 vs. Table A4 | either, consistently |
| "with and without the transfers" | §4.1 | transfers (P) are in both columns — you mean non-pecuniary payoffs |
| "social-alignment" hyphenated | §4.2, §4.2.1 headings | no hyphen in a noun phrase |
| Sentence case vs. title case headings | §4.2.1 vs. §4.3 | either, consistently |

## Notation

- **Eq. (10).** α_k = ∂²MV / ∂W^k_f ∂**M**^k_m — should be W^k_m.
- **Eq. (10).** The underbrace labels only the interaction terms as v(f,m), but §2.1 defines v(f,m) as the total match value and Eq. (12) uses an MV that includes ξ·Ind. Also the left-hand side is written MV(f,m | α, β) though the function also depends on ξ.
- **Eq. (12).** NP_{f′m′}(γ_m) should be γ_{m′}; and "γ_m *or* γ_{m′}" is typeset with the "or" in math italic.
- **Eq. (12).** The CEO index m is never tied to the firm index f — define m = μ(f) for the observed matching.
- **Eq. (14).** Stray operator: λ₄·(· SocialScore × Prosocial).
- **Eq. (15) / (16).** Eq. (15) uses α for the intercept while α is the structural parameter vector; Eq. (16) uses δ₀. Unify on δ₀.
- **§4.3 and Table 6 note.** "the observed match of CEO m with firm f and CEO f′ with firm m′" — f′ and m′ are swapped. Table 6's note has the same problem ("between observed matches f and m").
- **§2.1, after Eq. (4).** "CEO m's utility from matching with firm f′ is *smaller than* his current match" — the condition is weak (≥), so "no greater than."
- **Fn. 7 vs Table A4.** NP = γS is called "constant marginal utility" in footnote 7 and "Linear Marginal Utility" in Table A4. Both describe something true, but pick one label.
- **Eq. (11).** √S_f gives decreasing marginal utility *in the CDF rank*, not in social practice. Footnote 12 half-addresses this; make it explicit at Eq. (11).

## Typos and table mechanics

- **§3.1** — "ranging from 1 to 16" → "0 to 15" (see A9).
- **§3.3** — "Table 2 show that" → "Table 2 shows that".
- **§5** — "each CEO' total pecuniary" → "each CEO's".
- **§5** — "a 8.9% decline" → "an 8.9% decline"; and "decline in productivity" → "decline in productivity-dimension match value" — productivity itself is not measured.
- **§5** — "In Table 7 Panels A, A1 and A2 report…" → "In Table 7 Panel A, A1 and A2 report…".
- **§5** — Mixed notation for the same scenario: "S_f = 100%" in the text, "S_f = 1" in the Table 7 panel header.
- **Table 6** — "SalesGrwoth" → "Sales Growth". Also the title ("The Effects of Relative Ranking on CEO Compensation Discrepancy") does not describe the dependent variable, which is a compensation-to-synergy ratio.
- **Table 7 note** — "Panel A presents the results of the empirical data benchmark, shutting down the social dimension or imposing all firms' social scores to be the highest level" — garbled; split into three clauses for A0, A1 and A2.
- **Table A4** — "Prosoical" ×2 → "Prosocial"; "Number of Inequality" / "Satisfied Inequality" → plural, to match Table 3.
- **Table A2** — "ExecComp" → "ExecuComp" (twice).
- **Table C2** — Titled "Model Out-of-sample Performance" but reports in-sample columns as well.
- **Figure 1** — The note says all variables are annual CDFs, but §3.3 describes the plot as showing "average prosocial scores." It shows average CDF ranks.
- **References** — Weisbrod (1988) is listed before Weisbrod (1977); initials differ ("B." vs "B. A."). Holmstrom → Holmström, for consistency with Terviö and Bénabou. Check whether Grewal, Serafeim & Yoon (2016, SSRN) now has a published version.
- **Title** — "Evidence from Two-sided Matching" names a method, not a setting. Consider "Evidence from a Two-Sided Matching Model of the CEO Labor Market."
- **JEL codes** — Add M41 for a JAE submission.

## Open questions I could not answer from the text

Each is a candidate for a referee's "please clarify."

- What exactly is P_fm — dollars, logs, or a CDF rank? (C11)
- Is *Prosocial* restricted to affiliations beginning before the appointment? (B5)
- How is the high/low prosocial split defined, and where is it stated? (A10, B7)
- How is a pair assigned to a prosocial subsample in Table 6? (C13)
- Why does Table 5's t+3 sample (368) differ from Table 4's (361) when both are said to require non-missing social compensation?
- Why does Table A1 Step 8 drop zero observations while footnote 9 reports substantial post-hiring `Scomp` attrition?
- In §2.3, does N in n_k = ⌊N/2⌋ count matches or inequalities, and are draws stratified by market? (C20)

---

# Suggested order of work

| Stage | Items | Why first |
|---|---|---|
| **1. Reconcile** | A10, A4, A7 | The high/low split, the two conflicting benchmark tables, and the Table 5 variable label all determine what the other numbers mean. Nothing downstream is safe until these resolve. |
| **2. Rewrite to the tables** | A1, A2, A3, A5, A6, A8, A9, A11–A18 | Pure text edits against numbers that are already final. A day's work, and it removes every "the text says the opposite" comment. |
| **3. Shore up the measure** | B1, B5, B3, B6, B7 | The measure is new, so it will be the focus of the report. Tier frequencies, the pre-appointment timing statement, and the Feng et al. comparison are the three that matter. |
| **4. Re-specify** | C2, C4, C12, C1 | Adding level controls, testing coefficient differences directly, and clustering Table 6 are all standard and all cheap. C1 is a framing change, not a re-run. |
| **5. Rebuild §5** | C7, C8, C9, C10, C21 | The counterfactual is the section most exposed to a rejection-grade comment. Recomputed reservation utilities, a γ_l = 0 baseline, and the assignment problem in place of DA. |
| **6. Reframe and polish** | C23, C24, D | JAE positioning, an honest conclusion with numbers and limitations, and the mechanical pass. |

---

*Reviewed against the manuscript text and all tables (1–7, A1–A4, C1–C2). Numeric cross-checks were recomputed independently from the reported table values; the arithmetic listed as verified in the summary reproduces exactly. Findings are labeled A–D by section and numbered within it, so they can be referenced directly in revision notes.*

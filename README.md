# Kill or Build

**Score a business idea on evidence, not opinions.**

Most idea validators give you a number like "7/10" based on how good the idea *sounds*. Kill or Build asks a different question: **how much real evidence do you have, and what is the cheapest next test to get more?**

It is a single HTML file. No sign-up, no backend, no cost. Open `index.html` or use the live demo.

> 🔗 **Live demo: [nataliapalacios.github.io/kill-or-build](https://nataliapalacios.github.io/kill-or-build/)** · Click **Load example** to see a full report in one click.

### The built-in example: *SDR on Demand*
An outsourced SDR (sales development) team sold as a monthly service to Spanish SMEs that can't hire in-house reps. B2B, Spain, US$24k/yr per client. The target-market count comes from official data: **203,270** small and medium firms (10–249 employees) in [Cifras PYME, Dec 2025](https://ipyme.org/Publicaciones/Cifras%20PYME/CifrasPyme_diciembre_2025.pdf). The report flags that this is an upper bound, because not every SME sells B2B.

The verdict is **Test**. The problem has Do-level evidence and the founder fit is strong, but competition is crowded and willingness to pay has only been *said*, not *done*. The riskiest assumption is willingness to pay, so the next step is a price conversation (what do they pay for lead generation today?), then a fake-door pricing page. Building the full service comes after that.

---

## How it works

### 1. Six dimensions
Taken from what Y Combinator asks in its application and from HBS-style market validation:

| # | Dimension | Where it comes from | Weight |
|---|---|---|---|
| 1 | Problem & urgency | YC: Problem · HBS: pain-point hypothesis | 25% |
| 2 | Target customer & segment | HBS: target demographics | 15% |
| 3 | Market size & timing | HBS: secondary research, bottom-up per country | 15% |
| 4 | Competition & unique insight | YC: unique insight · HBS: competitors | 15% |
| 5 | Business model & willingness to pay | YC: Business model · HBS: price hypothesis | 20% |
| 6 | Founder-market fit & go-to-market | YC: Team · channels | 10% |

The weights are set by hand. Problem and willingness to pay get the most weight because product–market fit (43%) and unit economics (19%) are among the most cited root causes in CB Insights' 2026 analysis of failed startups.

### 2. Two scores per dimension
- **Hypothesis strength (0–5):** three Yes / Partly / No questions about how well-formed the idea is (Jobs to be Done framing). Market size also adds a computed answer.
- **Evidence (0–5):** a Say → Do → Market ladder:

| Level | Type | What counts |
|---|---|---|
| 0 | None | Only my opinion |
| 1 | Say | Desk research, anecdotes, compliments |
| 2 | Say | 5+ interviews about real past behaviour |
| 3 | Do | Low-commitment action: sign-ups, waitlist, fake-door clicks |
| 4 | Do | High-commitment action: pre-orders, deposits, LOIs, paid pilots |
| 5 | Market | Paying customers who come back |

**Mom Test check:** if your evidence is "Say", you tick any red flags (compliments, hypothetical answers, friends and family, pitching first). Each red flag takes half a level off the evidence score.

### 3. Verdict
Per dimension:
- **Kill:** hypothesis < 2. Rethink the idea before you test it.
- **Investigate:** evidence < 2. Talk to customers.
- **Test:** evidence 2–3, or a hypothesis that is not yet strong. Move from Say to Do.
- **Build:** evidence ≥ 3 and hypothesis ≥ 3.

Overall: **Kill** if Problem or Willingness to pay is a Kill (fatal dimensions) or the weighted hypothesis is < 2. **Build** only if the weighted evidence is ≥ 3 *and* both Problem and Willingness to pay have Do-level evidence. Otherwise **Test** (weighted evidence ≥ 1.5) or **Investigate**.

The **riskiest assumption** is the dimension with the largest `weight × (5 − evidence)`. The report suggests a €0 experiment for it, chosen by its current evidence level. Each experiment comes with a success criterion you set *before* running it.

### 4. Real numbers, with references
- **Country data comes from the tool:** live from the [World Bank API](https://data.worldbank.org/) (population, % aged 15–64, internet users, GDP per capita, new business registrations). Every number links to its indicator and year.
- **The segment number comes from you:** the % of people (or the number of businesses) with the problem, *plus its source*. Unsourced inputs are flagged in the report.
- **Every dimension shows one benchmark** with its citation.

Bottom-up sizing (B2C): `population × % aged 15–64 × % internet users × your segment % × price` → serviceable market. Then × your realistic share → obtainable market.

---

## Benchmarks used

| Number | Claim | Source |
|---|---|---|
| 70% | of failed VC-backed startups ran out of capital (usually the final cause, not the root) | [CB Insights, Mar 2026](https://www.cbinsights.com/research/report/startup-failure-reasons-top/) |
| 43% | cited product–market fit | same |
| 29% | cited bad timing / macro | same |
| 19% | cited unsustainable unit economics | same |
| 72% | of innovations miss financial targets or fail outright | [Ramanujam & Tacke, *Monetizing Innovation*](https://www.simon-kucher.com/en/insights/monetizing-innovation) |
| 74% | of high-growth internet startups studied failed due to premature scaling | Startup Genome Report 2011, via [GeekWire](https://www.geekwire.com/2011/number-reason-startups-fail-premature-scaling/) |
| 40% | "very disappointed" PMF rule of thumb (with [caveats](https://measuringu.com/product-market-fit-item/)) | Sean Ellis |

Frameworks: [The Mom Test](https://www.momtestbook.com/) (Fitzpatrick) · [Jobs to Be Done](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done) (Christensen et al., HBR) · [How to Get Startup Ideas](https://paulgraham.com/startupideas.html) (Graham) · [Testing Business Ideas](https://www.wiley.com/en-us/Testing+Business+Ideas-p-9781119551447) (Bland & Osterwalder).

---

## Use it in a workshop
1. Each team fills the scorecard for its idea (about 15 minutes).
2. Click **Print / Save PDF** for a one-page report, or **Copy share link**. The whole report lives in the URL, with no database.
3. Compare the matrices side by side. Ideas in *Investigate* go out to do interviews, and ideas in *Test* run the suggested experiment.
4. Re-score after the experiment and watch the dots move right.

## Run / deploy
- **Locally:** double-click `index.html`.
- **GitHub Pages (free):** push this folder to a repo → Settings → Pages → Deploy from branch `main` / root.

## Roadmap
- [ ] Phase 1: paste interview notes and get an automatic Mom Test audit (Say / Do / compliment / hypothetical)
- [ ] Phase 2: funnel analytics (start → complete → share) and the public report as a growth loop
- [ ] More countries and sector-level data sources

## Credits & disclaimer
The evidence ladder is inspired by the Say/Do evidence concept in *Testing Business Ideas* and the Innovation Project Scorecard by Strategyzer AG. This project is independent and not affiliated with or endorsed by Strategyzer. Country data © World Bank, CC BY 4.0. Weights and thresholds are opinionated defaults. This is a thinking tool, not a prediction.

License: MIT

# Insure It or Risk It? 🎲

A free browser game about marine cargo insurance. Pick a cargo, pick an Incoterm and pick your cover. Then let the dice decide who pays when the voyage goes wrong: the insurer, the carrier, or **you**.

**Play it:** https://markfourman.github.io/cargo-insurance-explorer/

Built by [Mark Fourmanovskis](https://www.linkedin.com/in/mark-fourmanovskis/) for SCM930 Transportation, Seneca Polytechnic (Supply Chain Management).

> ⚠️ **All odds in this game are illustrative teaching numbers. They are not actuarial data and not real loss statistics.** The same note is on screen, next to every dice roll.

## What it teaches

- **Carrier liability is limited, and a limit is not insurance.** Road, ocean and air limits are shown against what your cargo is worth.
- **Only CIF (at least ICC C) and CIP (ICC A) force the seller to insure.** For every other Incoterm, whoever is at risk has to weigh the cargo's value against the cost of cover.
- **Insurable interest.** You can only claim for a loss that happened while you were at risk. A timeline shows where risk passes for each of the 11 Incoterms 2020.
- **General average.** Owners whose goods arrive fine still pay their share, and must post a cash deposit or an insurer's guarantee before release.
- **How a premium is built:** goods + freight, then the estimated premium, then +10% valuation, then the premium, line by line.
- **What ICC A, B and C cover**, and what nothing covers (bad packing, delay, the goods' own condition). Strikes and war need an add-on.
- **The claim race:** the notice deadline for each mode and the four documents every claim needs.
- **Why "I've never had a claim" proves less than it feels like.** Run 1,000 voyages and watch rare, big losses.

## How to play

1. **Cargo.** Choose from Niagara icewine, laptops, frozen seafood, steel coils or gold bars.
2. **Deal.** Choose mode, your role (buyer or seller) and Incoterm. The timeline shows who carries the risk at each step.
3. **Cover.** Choose none, ICC C, B or A, plus war and strikes. For air, you can also declare the value to the airline. The premium is worked out line by line.
4. **Voyage.** Four hazards are dealt, each showing its % chance. Roll the dice, ask for "a bad one", or run 1,000 voyages with and without insurance.
5. **Who pays?** A stacked bar splits each loss between carrier, insurer and you, with the reason for every line. Then try the same dice with different cover.
6. **Claim race (bonus).** Pick the right deadline and documents. Mistakes cut your payout.

Two **case files** sit under the game: a replay of the 2023 Toronto Pearson gold heist, and a no-cover FOB set-up in the spirit of a freight forwarder who reported never buying cargo insurance in five years.

## Simplifications (on purpose)

- A voyage has 7 steps (seller's dock to buyer's dock). Each Incoterm is placed at the step where risk passes. DAP and DDP use the buyer's dock, and DPU the destination terminal.
- One cargo policy follows the goods and pays whoever is at risk. The premium is counted as your cost.
- Four hazards are dealt per voyage from a pool for your cargo and route. When the pool is bigger than four, the % on each card is scaled up so the long-run chance per voyage matches the base figure (at the ×1 odds setting).
- Carrier liability is on or off per hazard. Storms, bad packing, delay and the goods' own condition are never the carrier's fault here. Fire, theft, handling and crashes are, up to the legal limit. Real liability depends on contracts, defences and facts.
- Air uses 26 SDR per kg everywhere. The W11 slide deck still shows the old 22.
- The perils table is the one on the course slide. Real Institute Cargo Clauses wording is more detailed, so read the actual policy.
- Cargo values, weights, routes and freight costs are my own examples. The gold shipment is sized like the 2023 heist.
- The heist replay assumes FCA with you as the buyer. The real Incoterms between the shippers and consignee are not in my sources.

## Numbers used

| What | Value | Source |
|---|---|---|
| Road carrier limit | CAD $4.41 per kg (CAD $2 per lb) | Seneca Polytechnic (2026) |
| Ocean carrier limit | 2 SDR per kg or US$500 per shipping unit (the game uses 2 SDR per kg) | Seneca Polytechnic (2026) |
| Air carrier limit | 26 SDR per kg since December 28, 2024 (it was 22) | Seneca Polytechnic (2026); ICAO (2024) |
| SDR to CAD | 1 SDR = C$1.92386 (November 16, 2026) | IMF (2026) |
| Standard cover | 110% of the CIF or CIP value | Seneca Polytechnic (2026) |
| CIF and CIP | Seller must buy ICC C (CIF) or ICC A (CIP) | ICC (2019); Seneca Polytechnic (2026) |
| ICC A rate | $0.27 per $100 of insured value | Seneca Polytechnic (2026) |
| War and strikes | $0.03 per $100 | Seneca Polytechnic (2026) |
| Claim notice | Sea: at delivery, or within 3 days if the damage is not visible. Air: 14 days. Road: 60 days | Seneca Polytechnic (2026) |
| Survey and claim time | Survey for losses over US$1,000. Claims take 30 to 90 days | Seneca Polytechnic (2026) |
| Gold heist | 6,600 gold bars (about $20M) and about $2.5M in foreign currency, April 17, 2023. Court limit 9,988 SDR, just over C$18,000. Settlement confirmed August 28, 2026, amount not disclosed | CP24 (2025); de Vries (2026) |
| ICC B and ICC C rates | $0.20 and $0.14 per $100 | **Illustrative** |
| Cargo risk factors | ×0.8 steel, ×1.0 seafood, ×1.2 icewine, ×1.5 laptops, ×2.0 gold, applied to the A, B or C rate. War and strikes and the refrigerated add-on are added flat | **Illustrative** |
| Refrigerated add-on | $0.10 per $100 | **Illustrative** |
| Declared-value fee (air) | 0.5% of the cargo's value | **Illustrative** |
| Hazard chances and loss sizes | Printed on each card. When you carry the whole trip's risk, something strikes your cargo on roughly 2% to 3.5% of voyages, depending on cargo and route | **Illustrative, not actuarial** |
| General average bill | 4% to 15% of the cargo's value | **Illustrative** |

The premium calculator is checked against the class worked example (goods $100,000, freight $3,000, rate $0.30 per $100 → insured value $113,639.90, premium $340.92) every time the page loads.

## Run it or publish it

It is one file with no build step and no external libraries. It stores nothing and sends nothing.

- **Run it locally:** double-click `index.html`.
- **Publish on GitHub Pages:**
  1. On GitHub, create a new public repository named `cargo-insurance-explorer`.
  2. Choose **Add file → Upload files**, drag in `index.html`, `og-image.png` (the picture LinkedIn shows in the link preview) and `README.md`, then **Commit changes**.
  3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick **main** and **/ (root)**, then **Save**.
  4. Wait about a minute. The game appears at `https://markfourman.github.io/cargo-insurance-explorer/`.
  5. Open the link on your phone to check it, then paste it into your LinkedIn post.

  If you use a different repository name, change the two `markfourman.github.io/cargo-insurance-explorer` links in the `<head>` of `index.html` (the preview-card address and picture).

## Sources

CP24. (2025, January 25). *Air Canada ordered to pay Brink's over $18K for $20M gold stolen at Toronto Pearson*. https://www.cp24.com/local/peel/2025/01/25/air-canada-ordered-to-pay-brinks-over-18k-for-20m-gold-stolen-at-toronto-pearson/

de Vries, T. (2026, August 30). *Air Canada settles the lawsuit over its $20 million Pearson gold heist*. AeroCorner. https://aerocorner.com/news/air-canada-brinks-gold-heist-settlement/

International Chamber of Commerce. (2019). *Incoterms® 2020: ICC rules for the use of domestic and international trade terms*. ICC.

International Civil Aviation Organization. (2024, October 18). *International air travel liability limits set to increase, enhancing customer compensation* [News release]. https://icao.int/Newsroom/Pages/International-air-travel-liability-limits-set-to-increase,-enhancing-customer-compensation--.aspx

International Monetary Fund. (2026, November 16). *Currency units per SDR for November 2026* [Data set]. Retrieved November 17, 2026, from https://www.imf.org/EXTERNAL/NP/FIN/DATA/rms_mth.aspx?reportType=CVSDR

Seneca Polytechnic. (2026). *SCM930 Week 10–11: Cargo insurance and claims* [Lecture slides; originals by L. Thomson, S. Varughese & M. Spies; source CIFFA].

---

Educational project. Not insurance or legal advice.

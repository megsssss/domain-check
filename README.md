# Domain Check

A small product prototype that helps a business owner judge a domain name before asking a broker for a price.

**Live demo:** https://megsssss.github.io/domain-check/

> An independent product case study inspired by domain brokerage and marketplace workflows. Scores and prices are illustrative, and no enquiry is sent anywhere.

## The problem

Buying a domain through a broker means asking for a price blind. Buyers can't tell whether a quote is fair, and some give up before sending the first message. Brokers, in turn, spend their first reply asking basic questions about budget, use case and timeline.

*This is an assumption to validate through buyer interviews, not a finding.*

## The idea

Show buyers why a domain is valued the way it is, then let them send a qualified enquiry in under a minute.

1. **Evaluate:** type a domain and get a score out of 100 with a plain-language breakdown.
2. **Understand:** see a rough price band, clearly labelled as illustrative.
3. **Enquire:** answer three quick questions and leave an email so the broker can reply with something useful.

## How the score works

Five factors add up to 100.

| Factor | Points | What it checks |
|---|---|---|
| Length | 25 | Shorter names are easier to type, say and remember |
| Extension | 20 | `.com`, `.in`, `.ai` and others, weighted by buyer trust |
| Easy to say and spell | 20 | Penalises hyphens, digits and hard consonant runs |
| Clear meaning | 20 | Checks whether the name reads as real business words, using a small word list |
| Memorability | 15 | Estimates syllables; fewer is easier to recall |

The price band is a lookup from the total score. It is a rule of thumb, not a valuation.

## Success metrics (if this were a live feature)

- **North Star:** enquiry-to-deal conversion
- **Funnel:** evaluation to enquiry-start rate, enquiry completion rate
- **Speed:** time to first broker response
- **Guardrails:** share of low-quality enquiries, complaints about score accuracy

## Tech

A single `index.html` with plain HTML, CSS and JavaScript. There is no framework, backend or database, so it loads instantly and is hosted free on GitHub Pages. It supports light and dark mode and works on mobile.

## Run locally

```bash
git clone https://github.com/megsssss/domain-check.git
cd domain-check
open index.html   # or double-click the file
```

No install or build step is needed.

## Known limitations

- The score is rules-based and the word list is small.
- There is no real sales or demand data behind the price band.
- Enquiries are not stored or sent.

## What I would do next

1. Interview 5 to 8 domain buyers to validate the problem and the question set.
2. Replace the rule-based score with comparable-sales data.
3. Route each enquiry to a broker queue with the buyer's answers attached.
4. A/B test a shorter enquiry form against the three-question version.

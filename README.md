# Oxylabs vs ScraperAPI: Which Is Cheaper at $49/Month, How Many Pages Does 100,000 Credits Really Buy, and Which One Fits Your Targets? (Full Plan Table + Credit Math)

Both services start at **$49/month**, but they charge in completely different ways. ScraperAPI sells API credits, and the same request can cost 1 credit or 75 depending on the flags you add. Oxylabs bills per 1,000 successful results, at a rate that changes with the target site.

That difference decides everything. On ScraperAPI's $49 Hobby plan you get 100,000 credits, which is 100,000 plain HTML pages or roughly **1,333 requests** against a protected site with ultra-premium proxies plus JavaScript rendering. On Oxylabs' $49 Micro plan, 100,000 Amazon pages would cost about $50 at $0.50 per 1,000 results. Same headline price, very different amounts of data.

Below: every ScraperAPI plan with current pricing, the full credit multiplier table, the limits that only show up in the billing FAQ, and the cases where Oxylabs is the better buy.

## Quick recommendation

> Most readers scraping Amazon, Google, Walmart, eBay or Redfin with a budget between $49 and $299 should start on ScraperAPI. One subscription covers every access mode and all 18 structured data endpoints, and the free tier is permanent rather than a trial. Pick Oxylabs instead if you need country-level targeting outside the US and EU on a cheap plan, or if procurement requires ISO 27001 and a named account manager.

For a first paid month, **Hobby at $49** (or $44.10/month billed annually) is the low-risk entry point, and you can upgrade mid-cycle if you run out of credits.

👉 [Start on the $49 Hobby plan and check your own targets with the free tier](https://www.scraperapi.com/?fp_ref=coupons)

## All ScraperAPI plans and prices

ScraperAPI publishes seven tiers plus a free plan. Prices below are monthly; annual billing takes 10% off every paid tier.

| Plan | Price / month | Credits & concurrency | Key limits | Get started |
| --- | --- | --- | --- | --- |
| Free | $0 | 1,000 credits, 5 threads | No geotargeting, no PAYG | [ Free plan, 1,000 credits monthly](https://www.scraperapi.com/?fp_ref=coupons) |
| Hobby | $49 ($44.10 annual) | 100,000 credits, 20 threads | US & EU geotargeting only, no PAYG | [ Hobby at $49/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Startup | $149 ($134.10 annual) | 1,000,000 credits, 50 threads | US & EU geotargeting only, no PAYG | [ Startup at $149/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Business | $299 ($269.10 annual) | 3,000,000 credits, 100 threads | No PAYG overage | [ Business at $299/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Scaling | $475 ($427.50 annual) | 5,000,000 credits, 200 threads | None beyond volume | [ Scaling at $475/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Professional | $975 | 10,500,000 credits, 300 threads | None beyond volume | [ Professional at $975/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Advanced | $1,975 ($1,777.50 annual) | 21,500,000 credits, 500 threads | None beyond volume | [ Advanced at $1,975/month](https://www.scraperapi.com/?fp_ref=coupons) |
| Enterprise | Custom | 22,000,000+ credits, 500+ threads | Negotiated | [ Talk to sales about Enterprise](https://www.scraperapi.com/?fp_ref=coupons) |

Two things in that table cost people money. **Credits never roll over** — your balance resets at renewal on every tier, including Enterprise. And **pay-as-you-go overage only unlocks at Scaling ($475)**. On Hobby, Startup or Business, running out means upgrading your plan or waiting for the reset.

A free plan sits underneath all of this: 1,000 credits and 5 concurrent threads every month, no credit card, and it does not expire. There is also a 7-day trial with 5,000 credits for testing real targets.

## How ScraperAPI credits actually work

Every request starts at a base cost that depends on the target, then adds multipliers for the features you switch on.

**Base cost per request:**

| Target | Credits |
| --- | --- |
| Standard page | 1 |
| E-commerce (Amazon, Walmart, eBay) | 5 |
| SERP (Google, Bing, including subdomains) | 25 |
| LinkedIn | 30 |

**Add-ons:**

| Parameter | Extra credits |
| --- | --- |
| `render=true` (JS rendering) | +10 |
| `premium=true` | +10 |
| `ultra_premium=true` | +30 |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | +10 |
| `screenshot=true` | +10 |
| `premium=true` + `render=true` | 25 total, not 20 |
| `ultra_premium=true` + `render=true` | 75 total, not 40 |

The last two rows are where budgets disappear. Combining premium proxies with rendering costs 25 credits rather than the 20 you would get by adding them separately, and ultra-premium plus rendering costs 75 rather than 40. Geotargeting, sessions, device type, output format and auto-parsing add nothing.

So what does $49 buy?

- **Plain HTML pages:** 100,000 requests.
- **Amazon product pages with JS rendering:** 15 credits each, about **6,667 pages**.
- **Protected sites with ultra-premium proxies plus rendering:** 75 credits each, about **1,333 requests**.
- **Google SERPs:** 25 credits each, about **4,000 queries**.

The `sa-credit-cost` response header reports the cost of every request, and the Domain Cost Estimator in the dashboard lets you price a URL before you commit to a tier. Run your three or four hardest target URLs through it before choosing a plan. That single step tells you whether Hobby covers your month or you need Startup.

One more billing detail worth knowing: failed requests caused by system errors do not burn credits. Successful responses and 404s are charged.

## How Oxylabs prices the same work

Oxylabs charges per 1,000 successful results (2xx responses) and varies the rate by target type. On the **$49 Micro** plan: Amazon $0.50/1K, Google $1.00/1K, other sites $1.15/1K, rendered pages $1.35/1K. Rates drop on higher tiers — other sites reach $0.75/1K on the $999 Business plan. Rate limits start at 50 requests per second on paid plans.

The **$249 Advanced** plan works out to roughly 622,500 results at the blended rates above, with 30 concurrent threads and JavaScript rendering always on. That last point cuts both ways: you never configure rendering, but you pay the rendered rate whether the page needed it or not. ScraperAPI only charges its 10-credit rendering fee when you set the flag.

Oxylabs has a structural catch for multi-product projects. Web Scraper API, SERP API, E-commerce API and residential proxies are separate subscriptions, and credits do not move between them. If your project needs both SERP data and product pages, you are sizing and paying for two plans. Every Oxylabs tier does support top-ups, which ScraperAPI only offers from $475.

Oxylabs' trial is 2,000 results, and account signup goes through a review that typically takes one to two days. Some users report waits of a week or longer, or flags when their location does not match their stated use case. ScraperAPI signup is self-serve; you can be running your first request in under ten minutes.

## What each plan quietly withholds

This is the section that decides whether a cheap plan actually works for you.

**ScraperAPI:**
- **Geotargeting is tiered.** Hobby and Startup only target US and EU proxies. Country-level targeting for anywhere else starts at Business ($299). If your project tracks prices in Japan, Brazil or India, the $49 and $149 plans cannot do it.
- **No overage billing below $475.** Hitting your credit ceiling mid-month leaves you with two options: upgrade or stop.
- **Credits expire at renewal.** Size the plan to actual usage rather than buying headroom.
- **A 10-minute forced cache applies to difficult targets.** For live pricing or stock levels, that data can be slightly stale.
- **DataPipeline bills on a separate, higher schedule.** A basic request costs 6 credits there versus 1 through the standard API.

**Oxylabs:**
- **Separate plans per product**, with no credit transfer between them.
- **Signup review** adds days before you can start.
- **No published per-site success rates**, same as ScraperAPI.

Both vendors keep per-site success rates out of public view, so any comparison claiming otherwise is working from benchmarks, not vendor disclosures.

If the geotargeting limit is the one that worries you, check whether your targets fall inside the US and EU before paying for Business you may not need.

👉 [Compare Business ($299) against Hobby to see which geotargeting tier you need](https://www.scraperapi.com/?fp_ref=coupons)

## Success rates and speed: what the numbers actually measure

Third-party benchmarks compiled from Proxyway's 2025 research give ScraperAPI a mixed picture by target:

| Target | ScraperAPI success rate |
| --- | --- |
| Zillow | 100% |
| Amazon | 98% |
| LinkedIn | 95% (30 credits per request) |
| Walmart | 93% |
| Google | 81.72% |
| Instagram, Twitter/X, Booking.com | 0% |
| Overall average | ~63%, 5.2–7.3s response |

Oxylabs, from the same research: 99.9% infrastructure success rate, Amazon around 93%, Google around 93%, average response 0.65s. That 0.65s figure describes the proxy infrastructure, not the Scraper API layer, which responds more slowly. ScraperAPI's own published range is 5–7 seconds, which it compares against an industry average near 9.8 seconds.

Read those two sets together and the pattern is clear. Oxylabs' proxy network is faster and more reliable at the transport level. ScraperAPI's structured endpoints for specific sites, Amazon in particular, post higher success rates in independent testing. If Amazon is your main target, the 98% figure and the 18+ parsed JSON fields from the Amazon Structured Data Endpoint matter more than raw proxy speed.

The 0% column is worth taking seriously. Instagram, Twitter/X and Booking.com failed entirely in that benchmark. Neither vendor is a safe bet for social platforms.

## Which one fits your project

**You mainly scrape Amazon, Walmart or eBay product data.** ScraperAPI. Amazon pages cost 5 credits, roughly $0.50 per 1,000 on Business, and the structured endpoints return parsed JSON including BSR, variants, seller info and reviews. All 18 endpoints across Amazon, Google, Walmart, eBay and Redfin work on every plan including Free.

**You need high-volume Google SERPs.** Oxylabs prices Google at $1.00/1K on Micro and $0.80/1K on Advanced; ScraperAPI charges 25 credits per query, about 4,000 queries on Hobby. Run your expected monthly query count through both models, because the cheaper option flips depending on volume.

**You need prices from countries outside the US and EU on a small budget.** Oxylabs targets all plans down to city and ZIP level. ScraperAPI requires Business at $299 for country-level targeting beyond US and EU.

**You need compliance paperwork and a named contact.** Oxylabs holds ISO/IEC 27001:2022 certification, is a member of the Ethical Web Data Collection Initiative, and assigns account managers with SLAs to enterprise clients.

**You are a solo developer spending under $100.** ScraperAPI Hobby at $49, or $44.10 annual. One plan covers API, async API, proxy port, structured endpoints and DataPipeline, so you are not buying add-ons later.

👉 [Start with Hobby at $49 and upgrade mid-cycle if you outgrow it](https://www.scraperapi.com/?fp_ref=coupons)

## Third-party ratings, with a caveat

On G2, Oxylabs scores **4.8/5** and ScraperAPI **4.4/5**. The gap looks significant until you check sample sizes. Oxylabs' sub-scores rest on 239 to 285 responses per category; ScraperAPI's rest on 5 to 6, and G2 marks several categories "Not enough data."

Where the samples do exist: Oxylabs scores 9.1/10 on meeting requirements and 9.1/10 on support quality, with recurring complaints about pricing (95 mentions) and expense (65). ScraperAPI scores 9.0/10 on meeting requirements, 9.0/10 on ease of use, 8.0/10 on ease of setup and 7.7/10 on support quality. Five reviews is not enough to call that support score a trend, but it is the number G2 displays.

## FAQ

**Can I use one ScraperAPI plan for all its products?**
Yes. The standard API, async API, proxy port, structured data endpoints and DataPipeline all draw on the same credit balance. Oxylabs sells its scraping products as separate subscriptions.

**Which is cheaper at $49?**
Depends on the target. ScraperAPI Hobby gives 100,000 credits: 100,000 plain pages, about 6,667 Amazon pages with rendering, or about 1,333 requests on protected sites with ultra-premium plus rendering. Oxylabs Micro gives you $49 of results-billed capacity, which at $0.50/1K is roughly 98,000 Amazon pages, at $1.15/1K about 42,600 pages on other sites, and at $1.35/1K around 36,300 rendered pages.

**Is ScraperAPI good for Amazon scraping?**
Its Amazon Structured Data Endpoint posted 98% success in independent benchmarks and returns 18+ parsed fields. Base cost is 5 credits per Amazon request.

**Do credits roll over?**
No, on any ScraperAPI tier. The balance resets each renewal.

**Is there a free plan?**
Yes. 1,000 credits and 5 concurrent threads per month, permanently, no card required. A separate 7-day trial adds 5,000 credits.

**Is there a discount code?**
Annual billing takes 10% off automatically with no code: Hobby drops to $44.10/month and Business to $269.10/month.

## Before you pay

Two checks decide your tier. First, run your actual target URLs through the Domain Cost Estimator or API Playground — the credit cost per URL is what determines whether 100,000 credits means a month of data or three days. Second, confirm whether you need geotargeting outside the US and EU, because that answer moves you from $49 to $299 with no middle option.

If both checks point to a plan you can size confidently, Hobby at $49 with the free tier underneath is the lowest-risk way to start, and the annual discount brings it to $44.10 without a code.

👉 [Check current ScraperAPI pricing and start on the free tier](https://www.scraperapi.com/?fp_ref=coupons)

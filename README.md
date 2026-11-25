# Best Web Scraping API: Which Benchmark Should You Trust, What Does $49 a Month Buy, and When Is ScraperAPI the Wrong Pick?

Three benchmarking teams tested the same scraping APIs and ranked them in three different orders. Proxyway's 2025 report put Zyte first with 93% success on heavily protected sites. String's benchmark placed the same API 11th at 68%. Firecrawl ended up last in Proxyway's protected-site test at 33.69% and 4th in String's at 80%. Any list that presents one of those numbers as the final word is selling you a ranking, not a decision.

ScraperAPI sits in the budget lane: third-party comparisons describe it as the pick for "budget scraping on less protected sites," and its official pricing starts at **$49/month for 100,000 credits and 20 concurrent threads**. There's a free plan with 1,000 credits and 5 threads, plus a 7-day trial that hands you 5,000 credits with no card. Third-party listings put its proxy pool around 40 million IPs.

Below you'll find every ScraperAPI tier, what each credit actually costs once rendering and bot-protection bypass kick in, why the public benchmarks disagree so wildly, and which readers should walk away from ScraperAPI entirely.

## Quick picks

> **Most readers:** ordinary product pages, directories, blogs, anything without aggressive bot protection, and a monthly budget under $100. Take **ScraperAPI Hobby at $49/month (100,000 credits, 20 threads)** and start on the free trial to price your real URLs first. 👉 [Check the Hobby plan at $49/month](https://www.scraperapi.com/pricing/?fp_ref=coupons)
>
> **Hardest protected sites:** Zyte or Bright Data.
> **Feeding an LLM or RAG pipeline:** Firecrawl, or Crawl4AI if you want to self-host for free.

## Every ScraperAPI plan on the current pricing page

ScraperAPI sells seven paid tiers plus a free plan. Annual billing takes exactly 10% off the monthly rate, and that's the only discount structure on the page.

| Plan | Monthly | Annual (per month) | Credits/mo | Threads | Sign up |
| --- | --- | --- | --- | --- | --- |
| Free | $0 | — | 1,000 | 5 | [ Start free](https://www.scraperapi.com/?fp_ref=coupons) |
| Hobby | $49 | $44.10 | 100,000 | 20 | [ Get Hobby](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Startup | $149 | $134.10 | 1,000,000 | 50 | [ Get Startup](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Business | $299 | $269.10 | 3,000,000 | 100 | [ Get Business](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Scaling | $475 | $427.50 | 5,000,000 | 200 | [ Get Scaling](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Professional | $975 | $877.50 | 10,500,000 | 300 | [ Get Professional](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Advanced | $1,975 | $1,777.50 | 21,500,000 | 500 | [ Get Advanced](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Enterprise | Custom | Custom | 22,000,000+ | 500+ | [ Request a quote](https://www.scraperapi.com/pricing/?fp_ref=coupons) |

Three differences between tiers matter more than the credit count:

- **Geotargeting.** Hobby and Startup cover the US and EU only. Country-level targeting anywhere in the world starts at Business, which is $299/month. If your project needs Brazil or Japan, your real entry price is six times the headline $49.
- **Overage.** Pay-as-you-go past your credit limit exists only from Scaling ($475) upward. On Hobby, Startup and Business, running out of credits returns a 429 and scraping pauses until the next renewal. You are not silently billed.
- **Credits expire monthly.** Unused credits reset at renewal and don't roll over, so there's no reason to buy a bigger tier than your measured monthly usage.

Every tier includes JS rendering, residential and mobile proxies, anti-bot bypass, CAPTCHA handling, automatic retries, custom headers and unlimited bandwidth. The company publishes a 99.9% uptime guarantee across plans.

## What one credit actually buys

The $49 headline is only accurate for plain pages. ScraperAPI charges per request *by target complexity*, and the multipliers are where budgets break. Here's the official credit table, with the effective price per 1,000 requests calculated at the Hobby rate of $49 per 100,000 credits.

| Request type | Credits | Cost per 1,000 on Hobby |
| --- | --- | --- |
| Standard page | 1 | $0.49 |
| Amazon, Walmart, eBay | 5 | $2.45 |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | 10 | $4.90 |
| JS rendering (`render=true`) | 10 | $4.90 |
| Premium proxies (`premium=true`) | 10 | $4.90 |
| Google or Bing SERP | 25 | $12.25 |
| Premium proxies + rendering | 25 | $12.25 |
| LinkedIn | 30 | $14.70 |
| Ultra premium + rendering | 75 | $36.75 |
| Geotargeting, sessions, device type, output format, autoparse | 0 | free |

Costs stack. ScraperAPI's own billing FAQ says bypass, rendering and premium proxies each add credits, so a Cloudflare-protected page that also needs rendering costs more than either line alone. That's the difference between 100,000 pages a month on Hobby and 5,000.

Run your target list through the **Domain Cost Estimator** in the dashboard before you pick a tier, and set the `max_cost` parameter so a single expensive URL can't drain the account. Every response also returns an `sa-credit-cost` header showing what that request consumed, which makes reconciliation against your own logs straightforward.

A realistic planning figure: one million plain pages fits Startup at $149. One million rendered pages needs ten million credits, which lands you on Professional at $975. Same page count, 6.5x the bill.

## Why the benchmarks disagree, and how to use them anyway

The three public tests measure different things, which is why the rankings look random.

Proxyway's 2025 report ran 11 participants against 15 heavily protected websites. Bright Data wasn't one of them, so its results can't be compared to Proxyway's numbers at all. String's benchmark uses its own site mix and configuration, and it showed ScraperAPI jumping from 64% to 84% success once it was tuned to its strongest settings. Scrape.do's 2026 benchmark tested 16 APIs on seven tough domains and counted a request as successful only when it returned validated HTML. HasData's comparison took a different route entirely: every service scored 99–100% on its test pages, so the useful differences were latency and output structure rather than success rate.

One product, four tests, four verdicts. Use the leaderboards to cut a long list down to three candidates, then run your own URLs through trial credits. ScraperAPI's 7-day trial gives you 5,000 credits, which is enough to measure your actual per-request cost before you commit to a tier. 👉 [Start the trial with 5,000 credits](https://www.scraperapi.com/?fp_ref=coupons)

## Matching the API to the job

**Plain pages at volume, tight budget.** ScraperAPI. It's cheap on 1-credit requests, the retry logic is automatic, and per-request cost is predictable once you've priced your domains.

**Cloudflare, DataDome or Kasada in the way.** Zyte posted 93% on Proxyway's protected-site test. Bright Data posted the highest average (98.87%) across 16 APIs in Scrape.do's 2026 benchmark, though it skipped Proxyway's test. Neither is budget territory: Zyte's smallest monthly commitment is $100, and Bright Data's Web Unlocker runs $1.50 per 1,000 successful requests on pay-as-you-go.

**Markdown or JSON for an LLM pipeline.** Firecrawl returns clean markdown by default, and its own documentation claims markdown output runs about 67% fewer tokens than raw HTML. That claim comes from the vendor, but the direction is right: with token-priced models, cutting two-thirds of the input is a real line item. Crawl4AI does the same job for free if you're willing to run Playwright yourself.

**Prebuilt parsers for specific sites.** Bright Data, Oxylabs and Apify all ship ready-made extractors for Amazon, Google, LinkedIn and similar targets, so you skip selector maintenance.

**Working out why a request failed.** Scrapfly's dashboards and session replay show what happened on each attempt, which is more useful than another success-rate table when you're debugging.

| Tool | Verified entry price | Strength | Weakness |
| --- | --- | --- | --- |
| Bright Data | $1.50 per 1K Web Unlocker requests; 5,000 free records/mo | 98.87% average across 16 APIs in Scrape.do's 2026 benchmark | Returns raw HTML; absent from Proxyway's test, so figures aren't comparable |
| Zyte | $5 free credit; $100/mo minimum commitment | 93% on protected sites (Proxyway); 1.43s median in HasData's test | 68% and 11th in String's benchmark |
| Firecrawl | 1,000 free credits; $19/mo ($16 annual) | Cleanest markdown/JSON output for LLMs | 33.69% on protected sites in Proxyway's test; AGPL license restricts commercial self-hosting |
| ScrapingBee | 1,000 free credits; $49/mo | Matched HasData's extraction rules field for field; 2.18s median | Thin control over hard targets |
| Scrapfly | 1,000 free credits, no expiry; $30/mo | Session replay per request | A rendered request through residential proxies costs 25–30 credits |
| Decodo | Free plan; $19/mo | About 87% in Proxyway, stable under load, flat pricing | 50.6% in String's benchmark |
| Apify | $19/mo | Thousands of prebuilt Actors; markdown crawler | 16.8s median latency; compute-unit billing is hard to forecast |
| Crawl4AI | Free, open source | LLM-ready markdown and JSON, ~87,000 GitHub stars | You host and maintain it |

## Three things the feature lists don't tell you

**ScraperAPI returns HTML first.** JSON comes from Autoparse and the site-specific structured endpoints, which cover a limited set of domains. In HasData's parsing fidelity study, ScraperAPI handed back the full page as markdown or text, which meant there was nothing structured to compare against. If your pipeline expects clean records out of the box, budget for writing a parser.

**Latency rules out live agent loops.** HasData measured a 9.07s median and a 12.57s P95 on standard requests, the widest spread in that test. With JS rendering on, the median response took 29 seconds. Batch jobs don't care. An agent that needs an answer mid-conversation does.

**AI extraction fails quietly.** Zyte's automatic product schema found all 20 products in the same fidelity study and priced them correctly, but half the product names came back truncated because it read the visible link text instead of the title attribute. Availability and star ratings, fields outside its schema, were missing entirely, and pages it has no schema for return raw browser HTML with no selector fallback. "AI-powered parsing" means someone else's field list, not yours.

Credit multipliers are the other quiet cost. Scrapfly charges 25–30 credits for a rendered request through residential proxies. Proxyway singled out Decodo for flat pricing that avoids cost spikes on difficult domains. ScraperAPI's multipliers are public and the Domain Cost Estimator is accurate, but you have to look them up before you buy, not after.

## Who should skip ScraperAPI

- **Anyone building sub-second agent loops.** 9 seconds is already slow; 29 with rendering is a non-starter.
- **Teams that need structured JSON from arbitrary sites without writing a parser.** Firecrawl or Crawl4AI will save you the engineering.
- **Projects aimed at heavily protected domains at scale.** 69% on Proxyway's protected set is a lot of failed requests to retry. Zyte and Bright Data earn their higher prices there.
- **Anyone who needs city-level or ASN-level proxy control.** ScraperAPI offers country, session and IP tier, nothing finer.

For everyone else, the decision usually comes down to whether a $49 plan covers enough credits after multipliers. 👉 [Compare all seven tiers on the pricing page](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## FAQ

**Which web scraping API has the highest success rate?**
Depends on the test. Proxyway's 2025 report put Zyte at 93% on heavily protected sites. Scrape.do's 2026 benchmark put Bright Data at 98.87% across 16 APIs, using a stricter definition that only counted validated HTML. String's benchmark ranked Zyte 11th at 68%. No single number transfers to your targets.

**Is ScraperAPI good for heavily protected sites?**
Proxyway measured 69% on its protected set. String recorded 64% rising to 84% once ScraperAPI was configured at its strongest settings, so tuning matters more here than the headline suggests. Bot-protection bypass adds 10 credits per request when it activates.

**How much does ScraperAPI cost for a million pages a month?**
Plain pages: 1 million credits, which is Startup at $149/month. Rendered pages: 10 million credits, which needs Professional at $975/month. Amazon pages at 5 credits each land at 5 million credits, or Scaling at $475.

**What's the best web scraping API for LLMs?**
Firecrawl for managed markdown and JSON output, Crawl4AI for a free self-hosted equivalent. ScraperAPI works if you already have a parser and only need the fetch-and-unblock layer.

## Before you pick a tier

Match the plan to your measured cost, not to the page count. If your targets are plain HTML and stay in the US or EU, Hobby at $49 covers 100,000 requests and there's no reason to spend more. If they sit behind Cloudflare, add 10 credits per request. If you need country-level geotargeting outside the US and EU, your entry point is Business at $299.

Two things to confirm before checkout: whether your domains trigger the bypass or rendering multipliers (the Domain Cost Estimator answers this in a minute), and what happens when credits run out. On Hobby, Startup and Business, requests get a 429 and stop until renewal, with no overage charge and no pay-as-you-go option. 👉 [Open the free trial and price your own URLs first](https://www.scraperapi.com/?fp_ref=coupons)

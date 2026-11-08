# Hirist Jobs Scraper & API - India IT & Tech Jobs, Last 24 Hours

Hirist jobs scraper and API: search every job on hirist.tech, India's tech job board, at once, live, and get each job's title, company, locations, remote or onsite, years of experience, skills, salary in lakhs when shown, company rating, posting date and link, newest first. Turn on full details for the description, the number of applicants and the city, state and country.

Use it as a Hirist API with no login, a hirist.tech scraper for IT jobs and tech jobs in India, or a daily job feed from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. It reads the same public API that hirist.tech's own pages call. Available as an [Apify Actor](https://apify.com/anshumanatrey/hirist-jobs-search). $0.000016 per job, $0.000019 with full details, $0.0068 per run start at the default memory, no login, no API key.

## What does it do?

- **Searches every job on Hirist at once.** On 2026-11-08 Hirist listed 28,770 open jobs at 4,654 companies, at employers such as Unisys, Capgemini, Infosys, Publicis Sapient, Oracle, Happiest Minds and NatWest. Hirist's own pages reach the newest 10,000 of one search; this actor reads the rest too.
- **The fields Hirist users filter on, on every row.** Years of experience as a range, skills (Hirist's skill tags, with the must-haves marked), pay in lakhs a year when the recruiter shows it, and the company's AmbitionBox rating.
- **One keyword is enough.** Type a job title or a skill and press Start. Leave the form empty for the newest jobs of every kind.
- **Newest first, read live.** Every job comes from Hirist at the moment of your run, sorted by the day Hirist shows, to the second for 95% of jobs.
- **Filters that take what people type.** Bangalore or Bengaluru, Delhi NCR, Karnataka, Remote, 3-6 years, last 24 hours, or a pasted Hirist search link with its city, experience and period.
- **Checks job links.** Paste Hirist job links, and each comes back open, closed or not found.

## How is it different from other Hirist scrapers?

- **It finds what Hirist's own search misses.** Hirist's search box reads words loosely and ranks by relevance: on 2026-11-08 it gave 687 jobs for python developer in Bangalore, 130 of them with both words in the title, while this actor found 246 such jobs, all 130 among them. For react it gave 40 jobs; 880 jobs on Hirist have React in the title, and 2,131 list React as a skill. In the 4 searches compared, all 232 of Hirist's own results with the words in the title were in this actor's rows, and 79 of Hirist's 80 top results.
- **Every job, past 10,000.** Hirist's API stops one search at 10,000 jobs, about 50 days of postings, and keeps a job up for 150 days. This actor splits a bigger search by place and by years of experience and reads every part: 28,768 of the 28,770 jobs Hirist counted (it counts 2 twice). The most used Hirist actor stops at 1,000 jobs a run.
- **Newest first by Hirist's own date.** The day Hirist shows on its job cards and in its job markup, with the exact time when that falls on the same day.
- **Experience the way Hirist reads it.** 5 years finds the jobs asking 4 to 8 years, as on Hirist's filter, and the rows keep the range.
- **You pay for what you get.** One charge per delivered row, plus the run start, and a spending limit stops the run cleanly with the jobs it paid for.

Every actor on the Apify Store that names Hirist in its title or slug and had 4 or more users in the last 30 days on 2026-11-08, ordered by users, as each one's listing and input form state it:

| Feature | themineworks | data_daemon | rt-solutions | crawloop | logiover | This actor |
|---|---|---|---|---|---|---|
| Users, 30 days | 110 | 22 | 6 | 5 | 4 | new |
| How words are matched | Hirist's search box | not stated | not stated | not stated | not stated | In the title, or the title and skills, of every job |
| Most jobs a run | 1,000 | the whole board, or 40 a keyword by default | 100 a search by default | 100 by default | 6,666 by default | every job, 28,770 on 2026-11-08 |
| Empty form | browses the backend category | searches python developer | not stated | not stated | the newest jobs | the newest jobs |
| Only jobs new since the last run | yes | yes | no | yes | no | no |
| Job link check: open, closed or not found | no | no | no | no | no | yes |

## When should I use it?

- **Job seekers and job boards:** new IT jobs in India by title, skill, city, experience and date, with pay where it is shown, on a daily schedule.
- **Recruiters and staffing firms:** see which companies are hiring for a skill right now, at what experience, and in which cities.
- **Sales and market research:** companies hiring tech teams in India, as a buying signal, and skill demand by city.
- **Data teams and AI agents:** one clean, stable feed of Hirist jobs through the API or MCP.

## How much does it cost to scrape Hirist jobs?

Pay per event: $0.016 per 1,000 jobs, or $0.019 per 1,000 with full details, plus $0.0068 per run at the default 512 MB of memory. Apify's free $5 monthly credit covers about 60,000 jobs in runs of 100. Platform usage is included, and there is no monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.000016 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.000019 | One saved job with full details on |
| Run start | $0.0068 per GB of memory | Charged by Apify when a run starts: once up to 1 GB and once more for each extra GB, so $0.0068 at the default 512 MB |

Hirist Jobs Scraper's Apify Store header, "from $0.011 / 1,000 jobs", shows the GOLD price, the lowest of the public discount tiers. Each Apify plan pays its own tier's price: FREE (the free plan) $0.000016 a job and $0.000019 with details, BRONZE (Starter) $0.000016 and $0.000018, SILVER (Scale) $0.000013 and $0.000015, GOLD (Business) and the enterprise tiers above it $0.000011 and $0.000013. The run start is a flat fee on every plan, $0.0068 per GB of memory ($0.0068 at the default 512 MB), and the header never shows it.

| Run (free plan price, default memory) | Cost |
|---|---|
| 100 newest jobs | $0.0084 |
| 100 jobs with full details | $0.0087 |
| 1,000 jobs | $0.0228 |
| Every job on Hirist, 28,358 delivered on 2026-11-08 | $0.4605 |

Number of jobs (`maxJobs`) and the run start set the most a run can cost, and a run stops at its spending limit with a message saying so. Why a run start: a search whose words are rare reads all of Hirist's jobs, 240 calls and about 70 seconds at the default memory, whatever it finds; the run start pays for that read, so each job costs little.

## How does the price compare with other Hirist scrapers?

Every actor on the Apify Store that names Hirist in its title or slug and had 3 or more users in the last 30 days, found by searching the Store for 9 Hirist and iimjobs terms on 2026-11-08 (37 Hirist actors read), ordered by users. Free-plan prices from each actor's current pricing.

| Actor | Users, 30 days | Per job | Start fee | Input |
|---|---|---|---|---|
| themineworks/hirist-jobs-scraper | 105 | $0.005 | $0.005 per GB | Keyword or one of 12 categories, up to 1,000 jobs |
| data_daemon/hirist-jobs-scraper | 23 | $0.002 | $0.001 | Keywords, or the whole board |
| rt-solutions/india-tech-jobs-scraper | 6 | $0.0015 | none | Instahyre, Hirist and Cutshort in one format |
| crawloop/hirist-jobs-scraper | 5 | $0.00249 | $0.00005 | Keyword, category, city or Hirist links |
| logiover/hirist-tech-scraper | 4 | $0.003 | none | Keywords, cities, experience band |
| memo23/hirist-jobs-scraper | 3 | $0.002 | $0.0001 | Keyword, city and experience |
| This actor | new | $0.000016, $0.000019 with details | $0.0068 per GB | One keyword or none, every job on Hirist |

Where others are cheaper: runs that save only a few jobs, because this actor's run start is $0.0068 and theirs is $0.001 or less. Depending on the plan, crawloop, logiover and memo23 can cost less for a run under 4 jobs, data_daemon under 5 and rt-solutions under 7; from 7 jobs a run this actor costs less than every actor in the table on every plan: 100 jobs on the free plan cost $0.0084 here, $0.505 on themineworks, the most used, and $0.15 to $0.30 on the others. The most used Hirist actor, themineworks, costs $0.005 a job on the free plan, $0.0042 on Starter, $0.00355 on Scale and $0.003 on Business, plus a $0.005 run start; this actor costs less on every plan for any run that saves a job. Where others do more: themineworks and crawloop browse Hirist's 12 categories, and themineworks, data_daemon and crawloop can deliver only jobs new since your last run.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word: frontend also finds Front-End. A pasted Hirist search link works too |
| Where the job is (`location`) | A city, state or country: Bangalore, Bengaluru, Pune, Delhi NCR, Karnataka, India. Remote alone asks for remote jobs; next to other places it narrows nothing |
| Experience (`experienceYears`) | Your years: a number such as 5, a range such as 3-6, 10+ for 10 or more, or fresher for 0. A job matches when the years it asks for overlap yours |
| Remote or onsite (`workType`) | remote is what Hirist marks work from home or lists as Remote; onsite is every other job |
| Posted in the last (`postedWithin`) | 24 hours, 3 days, 7 days, 30 days, any time, or your own period such as 48 hours |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description as text and HTML, the number of applicants, the recruiter's own apply link when given, and the city, state and country |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or lead |
| Match skills too (`searchDescriptions`) | Finds your words in Hirist's skill tags too, not only the title |
| Only these companies (`companies`) | A company name (Unisys) or a Hirist company page link. Empty searches everyone |
| Job links to check (`jobUrls`) | Paste job links to check whether they are still open, instead of searching |

Example input:

```json
{
  "searchTerms": ["python developer"],
  "location": ["Bangalore", "Pune"],
  "experienceYears": "5",
  "postedWithin": "7 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. These rows are from a run of the example input (python developer) on 2026-11-08: 5,998 of Hirist's newest jobs read, at least 112 matching at 86 companies, the 100 newest saved in 5 s.

| Job title (`title`) | Company name (`company`) | Main location (`location`) | Experience from (`experienceMin`) | Experience up to (`experienceMax`) | Pay summary (`salary`) | Posted on (`postedAt`) |
|---|---|---|---|---|---|---|
| Backend Developer - Python/FastAPI | HiringBlaze | Hyderabad | 2 | 4 | INR 12 - 15 lakh a year | 2026-11-06 |
| Senior Java Full Stack Developer - React.js/Python | Appizion Consulting & Solutions | Hyderabad | 5 | 8 |  | 2026-11-06 |
| Full Stack Developer - Python/React.js - AI Applications | Hyrhub | Bangalore | 5 | 10 |  | 2026-11-06 |
| Python Developer - Django/Azure | Patch Infotech | Remote | 4 | 6 |  | 2026-11-06 |
| Lead AI Developer - Generative AI/Python | Sunovaa Tech | Bangalore | 7 | 10 |  | 2026-11-06 |

One row as JSON:

```json
{
  "title": "Backend Developer - Python/FastAPI",
  "company": "HiringBlaze",
  "location": "Hyderabad",
  "otherLocations": [],
  "workType": "onsite",
  "salary": "INR 12 - 15 lakh a year",
  "postedAt": "2026-11-06T20:30:47Z",
  "jobUrl": "https://www.hirist.tech/j/backend-developer-pythonfastapi-1682753",
  "applyUrl": "https://www.hirist.tech/j/backend-developer-pythonfastapi-1682753",
  "status": "open",
  "platform": "hirist",
  "jobId": "1682753",
  "checkedAt": "2026-11-08T01:27:44+00:00",
  "salaryMin": 1200000,
  "salaryMax": 1500000,
  "salaryCurrency": "INR",
  "salaryPeriod": "year",
  "experienceMin": 2,
  "experienceMax": 4,
  "skills": ["Backend Architecture", "Python", "RESTful API", "FastAPI", "Redis", "RDBMS", "PostgreSQL", "MySQL"],
  "mandatorySkills": ["Backend Architecture", "Python", "FastAPI", "Redis", "RDBMS"],
  "companyRating": null,
  "companyReviews": null,
  "applicants": null
}
```

Full details add `description`, `descriptionHtml`, `applicants`, `city`, `region`, `country` and `countryCode`, and give the recruiter's own apply link in `applyUrl` when Hirist has one. A checked link that is closed or not found comes back with its `status`, company and link, and the other fields empty. A run also writes an `OUTPUT` record: how many jobs were read, matched and saved, the checked links, any notes on how your input was read, and the settings used.

## How fast is it?

A few seconds for most searches. On Apify on 2026-11-08 at the default 512 MB, the empty form took 5 s and the example input 10 s with 6 calls, about the same at 1 GB and 2 GB; a search for a city, a period or years of experience asks Hirist to filter, so it reads fewer jobs. A search whose words are rare reads every job on Hirist, 240 calls, in 70 s (46 s at 1 GB), and every job, 28,358 rows, took 94 s with a 254 MB memory peak. Full details read each saved job once more: 100 devops engineer jobs with details took 10 s and 105 calls.

## Common questions

### Which posting date does it use?

Hirist Jobs Scraper uses the day Hirist shows on its job cards and in its job markup, for the posting date, the newest-first order and the Posted in the last filter. Hirist also records the moment a job went live, which falls on that day for 95% of jobs: the row then gives that moment in UTC, and for the other 5% the day alone (YYYY-MM-DD). Hirist keeps a job up for 150 days after that day.

### Why does it find more jobs than Hirist's own search?

Hirist's search box matches words loosely and ranks by relevance, so a search mixes in jobs that do not have your words in the title, and leaves out many that do. Hirist Jobs Scraper reads every job and keeps those whose title has every word you typed: on 2026-11-08, 880 jobs with React in the title against 40 from Hirist's search for react. Tick Match skills too (`searchDescriptions`) to also match Hirist's skill tags: 2,131 jobs list React as a skill.

### How does years of experience work?

Every Hirist job asks for a range of years, such as 4 to 8. Type your years in Experience (`experienceYears`), such as 5, and Hirist Jobs Scraper keeps the jobs whose range includes 5, the same rule as Hirist's own filter. A range such as 3-6 keeps the jobs whose range overlaps it, 10+ (10 or more) keeps the jobs open to someone with 10 years or more, and fresher (0) keeps those that start at 0. Every Hirist job states its range, so the filter leaves out no job for lack of one, and every row carries the range in `experienceMin` and `experienceMax`.

### What does remote mean on Hirist?

Hirist marks a job as work from home or not, and some jobs list Remote as a place; Hirist Jobs Scraper calls those remote and every other job onsite. On 2026-11-08 that was 10.7% of jobs. Hirist has no hybrid mark, and its work-from-home jobs include hybrid ones: of 20 such descriptions read, 7 describe a hybrid setup. So hybrid in Remote or onsite (`workType`) reads as remote. Remote typed alone in Where the job is (`location`) asks for remote jobs too; typed next to a city it narrows nothing, because the city's remote jobs are already among its jobs: Bangalore with Remote finds the same 246 python developer jobs as Bangalore alone.

### What if a search finds nothing?

Hirist Jobs Scraper says why in the run's message and in its `OUTPUT` record, and charges only the run start. When your place, period and years of experience go to Hirist's own search and it has no job there, the message says Hirist has no job with your words inside your other filters. When jobs with your words were left out by a filter checked in the run, it names the filter that left them out and how to loosen it: on 2026-11-08, python developer in Pune, remote, in the last 3 days found 3 jobs with those words, and the work type alone left out 2 of them. The message also shows how your input was read.

### Does it need a login or an API key?

Hirist Jobs Scraper needs no Hirist login and no API key, because it reads the public API that hirist.tech's own job pages call, which serves what any visitor sees. You need only an Apify account.

### Does it work on Apify's free plan?

Hirist Jobs Scraper works on Apify's free plan, which pays the FREE price: $0.000016 a job plus the $0.0068 run start at the default 512 MB. The free $5 monthly credit pays for about 60,000 jobs in runs of 100, at $0.0084 a run.

### How often should I run it?

Running Hirist Jobs Scraper once a day keeps a job feed fresh: set Posted in the last (`postedWithin`) to 24 hours and Number of jobs (`maxJobs`) to 0 to get every job posted that day, about 200 on a weekday and fewer at weekends. Set the run up under Schedules in Apify Console, and match rows on `jobId` to skip jobs you already have.

### How do I get every job of one company?

To get every open job of one company with Hirist Jobs Scraper, type the company's name in Only these companies (`companies`), such as Unisys, or paste its Hirist company page link, and set Number of jobs (`maxJobs`) to 0. A company with a Hirist company page is read from that page in seconds: Unisys had 28 open jobs on 2026-11-08. Any other name is matched against the company of every job on Hirist, which takes about 30 seconds.

### How do I check a list of job links?

Hirist Jobs Scraper checks whether Hirist job links are still open when you paste them into Job links to check (`jobUrls`), one per line, instead of searching. Links on hirist.tech and hirist.com work, old .html links too. Each link comes back as one row, open with the job's fields, closed, or not found, so 10 links come to $0.00696 with the run start.

### Is iimjobs included?

Hirist Jobs Scraper reads hirist.tech only. iimjobs.com, Hirist's sister site for management, finance and sales jobs, keeps its own jobs, so its jobs are not in these rows.

### How do I call it from the API, Python, JavaScript, n8n or an AI agent?

Hirist Jobs Scraper runs from the Apify API, Python, JavaScript, n8n, Make or an AI agent over MCP. Each way uses your Apify token (Apify Console, Settings, API & Integrations) and takes the input as JSON keyed by the field names, such as `searchTerms` and `maxJobs`.

**API.** One call runs the actor and returns its rows. Apify stops that wait after 300 seconds, which covers any search; a client below waits as long as a run takes.

```bash
curl -X POST "https://api.apify.com/v2/acts/anshumanatrey~hirist-jobs-search/run-sync-get-dataset-items" \
  -H "Authorization: Bearer <YOUR_APIFY_TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"searchTerms": ["python developer"]}'
```

**Python** (`pip install apify-client`):

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/hirist-jobs-search").call(run_input={"searchTerms": ["python developer"]})
for row in client.dataset(run.default_dataset_id).iterate_items():  # apify-client 3+; on 2.x use run["defaultDatasetId"]
    print(row["title"], row["company"], row["location"], row["experienceMin"], row["salary"], row["jobUrl"])
```

**JavaScript** (`npm install apify-client`):

```js
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: '<YOUR_APIFY_TOKEN>' });
const run = await client.actor('anshumanatrey/hirist-jobs-search').call({ searchTerms: ['python developer'] });
const { items } = await client.dataset(run.defaultDatasetId).listItems();
for (const row of items) console.log(row.title, row.company, row.location, row.experienceMin, row.salary, row.jobUrl);
```

**n8n and Make.** In n8n, add the Apify node, pick Run an Actor and get dataset, choose this actor and paste the input JSON: the rows come out as n8n items. In Make, the Apify app's Run an Actor and Get Dataset Items modules do the same.

**AI agents (MCP).** Add `https://mcp.apify.com?tools=anshumanatrey/hirist-jobs-search` to your MCP client and sign in with Apify, or send `Authorization: Bearer <YOUR_APIFY_TOKEN>`. The agent gets this actor as a tool and sees every input field by its JSON key.

### Am I charged for closed jobs?

Hirist Jobs Scraper charges for a closed job only when you paste its link to check. A search returns open jobs only, and a pasted link that turns out closed or not found is one Job row, because it was checked and answered.

### Is it legal to use?

Hirist Jobs Scraper reads public job postings. You are responsible for how you use the data, including Hirist's terms and the privacy laws that apply to you.

## Limitations

- Pay is shown on 7% of jobs (on 2026-11-08); recruiters hide it on the rest.
- The company rating comes from AmbitionBox through Hirist, on 57% of jobs.
- Remote and onsite are Hirist's work-from-home mark; Hirist has no hybrid mark and states no job type (full-time, contract).
- The number of applicants comes with full details and for jobs read from a company page; Hirist hides view counts from visitors.
- Titles and companies are as Hirist shows them: most titles start with the company, and a confidential job's company reads Verified Company.
- A job a company posts twice with the same title at the same place is delivered once (412 such copies on 2026-11-08).
- A search with rare words, and a company with no Hirist company page, read every job on Hirist, about 70 seconds at the default memory.
- Hirist's category pages (/c/) are not read as a filter: type the job titles or skills instead.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | What it searches |
|---|---|
| [Greenhouse Jobs Scraper](https://apify.com/anshumanatrey/greenhouse-jobs-search) | Jobs from every company on Greenhouse, searched live |
| [Lever Jobs Scraper](https://apify.com/anshumanatrey/lever-jobs-search) | Jobs from 2,300+ companies on Lever (jobs.lever.co), searched live |
| [Workday Jobs Scraper](https://apify.com/anshumanatrey/workday-job-search) | Jobs from every company on Workday (myworkdayjobs.com), searched live |
| [SmartRecruiters Jobs Scraper](https://apify.com/anshumanatrey/smartrecruiters-jobs-search) | Jobs from 2,900+ companies on SmartRecruiters, searched live |
| [Workable Jobs Scraper](https://apify.com/anshumanatrey/workable-job-search) | Jobs from every company on Workable, in one search |
| [Ashby Jobs Scraper](https://apify.com/anshumanatrey/ashby-jobs-search) | Jobs from every company on Ashby (jobs.ashbyhq.com), searched live |
| [Cornerstone Jobs Scraper](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Jobs from every company on Cornerstone (csod.com), searched live |
| [Deel Jobs Scraper](https://apify.com/anshumanatrey/deel-jobs-search) | Jobs from every company on Deel ATS (jobs.deel.com), with pay |

For the people behind a company: [LinkedIn Profile Finder](https://apify.com/anshumanatrey/linkedin-harvester) turns an email into a public LinkedIn profile.

## Documentation

- Apify Store: https://apify.com/anshumanatrey/hirist-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/hirist-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-11-08 (version 1.0)

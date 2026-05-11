# Proposal: Scaling Research to 1000 "Federer" Companies

## 1. Objective
To develop a scalable, automated, and high-accuracy workflow to identify and profile 1000 specialty manufacturing companies across India that fit the "Federer" profile (Rs. 50Cr – 500Cr revenue, technocrat-led, high-growth).

## 2. Strategic Sourcing (The Funnel)
To reach 1000 qualified companies, we will expand the geographical focus beyond Ahmedabad-Vadodara to other industrial hubs:
- **Maharashtra:** Thane-Belapur, Roha, Patalganga (Chemicals & Pharma).
- **Telangana:** Pashamylaram, Jeedimetla (Bulk Drugs & APIs).
- **Tamil Nadu:** Ambattur, Gummidipoondi (Specialty Chemicals & Engineering).
- **Karnataka:** Peenya, Bommasandra (Biotech & Precision Manufacturing).

### Sourcing Channels:
- **SME Listings:** NSE Emerge and BSE SME platforms for recently listed high-growth companies.
- **Pollution Control Board Records:** State PCB (Gujarat, Maharashtra, etc.) lists of "Orange" and "Red" category manufacturers (primary source for identifying new plants).
- **Patent Filings:** Scraping Indian Patent Office data to find companies with recent "Technical Moats."
- **Export-Import Data:** Identifying companies with niche export portfolios via Zauba/ImportGenius.

## 3. Automated Qualification Workflow
We will implement a 3-layer automated funnel to filter 10,000+ raw leads down to 1,000 qualified "Federers."

### Layer 1: The Scraper (Data Ingestion)
- **Tooling:** Python (BeautifulSoup/Selenium) or Clay/Phantombuster.
- **Action:** Scrape GIDC/MIDC/TSIIC directories and Google Maps for company names and addresses.
- **Output:** Raw Lead List (10,000+).

### Layer 2: The Classifier (AI Filtering)
- **Tooling:** LLM-based web-search agents (Perplexity API or Custom GPTs).
- **Action:** For each raw lead, the agent fetches:
    - Founder/MD background from LinkedIn/Corporate pages.
    - Latest estimated revenue from public news or SME directories.
    - Product categorization (Manufacturer vs Trader).
- **Logic:** Filter leads where `Manufacturer == True` AND `Revenue >= 50Cr` AND `Revenue <= 500Cr`.

### Layer 3: The Scorer (C1-C6 Scoring)
- **Action:** Automated scoring based on search results. Companies scoring 5 or 6 are promoted to the final list.

## 4. Quality Control & Hallucination Guardrails
To maintain 95%+ accuracy, we will implement:
- **Triangulation:** Revenue data must be verified from at least two independent sources (e.g., Tofler + News report).
- **Human-in-the-Loop (HITL):** A dedicated Business Analyst (BA) reviews every company with a score of 5 or 6 to verify the "Technical Moat" (C3) and "Technical DM" (C4) manually.
- **Negative Prompting:** When using AI for profiling, we will use negative prompts: *"Do not include software companies, traders, or companies with private equity control unless explicitly mentioned as promoter-led."*

## 5. Execution Timeline (4 Weeks)

| Week | Phase | Deliverable |
| :--- | :--- | :--- |
| **Week 1** | **Hub Mapping & Scraping** | Raw list of 5,000+ manufacturers from 10 industrial hubs. |
| **Week 2** | **AI Qualification & Filtering** | Filtered list of 2,000 candidates with estimated revenue and DM profiles. |
| **Week 3** | **C1-C6 Scoring & Validation** | Initial list of 1,200 companies with full scoring. |
| **Week 4** | **Human QC & Finalization** | Final verified CSV of 1,000 "Federer" companies. |

## 6. Resource Requirements
- **1 Data Engineer:** For scraping and API integrations.
- **1 Business Analyst (Lead):** For quality control and manual verification.
- **Tooling Stack:** Python, OpenAI/Perplexity API, Tofler API subscription, LinkedIn Sales Navigator.

---

### **Note for Recruiter:**
A **hand-drawn diagram** illustrating this sourcing funnel, the integration of AI tools, and the quality control checkpoints is provided as a separate image submission per the assignment guidelines.

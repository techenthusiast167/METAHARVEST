# METAHARVEST

This is an advanced Python-based Metadata Web Scraper designed to extract rich, structured metadata from any given list of websites. It taps into web page contents to retrieve various types of information relevant to OSINT (Open Source Intelligence) and cybersecurity investigations.



---

# What This Tool Does

**Core Capabilities**


- **Title Extraction**: Captures the page title to identify the main topic or branding.

- **Meta Tags**: Gathers metadata such as description, keywords, and other HTML meta information useful for SEO and content summary.

- **Emails Extraction**: Uses regular expressions to detect and collect email addresses visible within the page content.

- **Named Entities**: Utilizes natural language processing (via spaCy) to identify and extract persons, organizations, and geographic locations, enabling better entity recognition for intelligence purposes.

- **Hyperlinks**: Extracts all links from the page, including relative URLs resolved to full URLs.

- **Social Media Links**: Filters extracted links to identify known social media platforms such as Facebook, Twitter, LinkedIn, GitHub, etc.
  
- **Security Headers**: Checks HTTP response headers related to site security best practices (e.g., Content Security Policy, Strict Transport Security, X-Frame-Options).

- **IP Address Resolution**: Converts the target hostname into its corresponding IP address.

- **Language Detection**: Reads the HTML lang attribute or meta tags to determine the page’s language.

- **Last Modified Date**: Attempts to find the last modification timestamp from HTTP headers, meta tags, or page text.

- **Timestamping**: Records the scrape time in a timezone-aware UTC ISO8601 format for logging and audit.



**Output Formats**

- Saves the detailed metadata per URL in JSON for structured data handling.

- Creates a CSV summary file for tabular data analysis and easy review across many URLs.


---

# Importance in OSINT and Cybersecurity

**OSINT (Open Source Intelligence)**


- **Information Gathering**: Automatically collects contact points (emails), key personnel or organizations, web infrastructure data (IPs), and social presence linked to a domain, all critical for intelligence operations.

- **Entity Identification**: Extracted names and locations help build profiles for targets or connected entities to aid investigations.

- **Automation**: Enables analysts to process large URL lists efficiently and systematically, saving significant manual effort.

- **Structured Data Output**: JSON and CSV formats allow integration with broader OSINT toolchains, databases, or visualization platforms.



**Cybersecurity Relevance**

- **Security Posture Analysis**: Capturing security headers exposes potential misconfigurations or weaknesses in web defenses.

- **Attack Surface Mapping**: Identifying social media links and contact emails aids penetration testers and red teams in finding attack vectors or social engineering targets.

- **Monitoring and Alerting**: Scheduled scraping can track changes over time in metadata or header settings, highlighting suspicious alterations that could indicate compromises.

- **Reconnaissance**: Ethical hackers and defenders use tools like this for reconnaissance phases, building a thorough understanding of target assets.


---


# Requirements and Dependencies

- **Firstly, create your virtual environment**:

  

# METAHARVEST

This is an advanced Python-based Metadata Web Scraper designed to extract rich, structured metadata from any given list of websites. It taps into web page contents to retrieve various types of information relevant to OSINT (Open Source Intelligence) and cybersecurity investigations.



---

# What This Tool Does

 ### Core Capabilities


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



— **Output Formats**

- Saves the detailed metadata per URL in JSON for structured data handling.

- Creates a CSV summary file for tabular data analysis and easy review across many URLs.


---

# Importance in OSINT and Cybersecurity

— **OSINT (Open Source Intelligence)**


- **Information Gathering**: Automatically collects contact points (emails), key personnel or organizations, web infrastructure data (IPs), and social presence linked to a domain, all critical for intelligence operations.

- **Entity Identification**: Extracted names and locations help build profiles for targets or connected entities to aid investigations.

- **Automation**: Enables analysts to process large URL lists efficiently and systematically, saving significant manual effort.

- **Structured Data Output**: JSON and CSV formats allow integration with broader OSINT toolchains, databases, or visualization platforms.



— **Cybersecurity Relevance**

- **Security Posture Analysis**: Capturing security headers exposes potential misconfigurations or weaknesses in web defenses.

- **Attack Surface Mapping**: Identifying social media links and contact emails aids penetration testers and red teams in finding attack vectors or social engineering targets.

- **Monitoring and Alerting**: Scheduled scraping can track changes over time in metadata or header settings, highlighting suspicious alterations that could indicate compromises.

- **Reconnaissance**: Ethical hackers and defenders use tools like this for reconnaissance phases, building a thorough understanding of target assets.


---


# Requirements and Dependencies

- **Create your virtual environment**:

      python3 -m virtualenv my_temp_venv
      source my_temp_venv/bin/activate 
  

- **Ensure you have Python 3.7 or later installed**

- **Install required packages using pip**:

      pip install requests beautifulsoup4 spacy colorama
      python -m spacy download en_core_web_sm


- - - 

# Usage

— **Please copy the script from the link below and save it locally**:
  
https://gist.github.com/techenthusiast167/1489e2711921aa2741d154a8f10960f4

**Example**:

- Open **nano metaharvest**
- Copy and paste in the script and press
**Ctrl + 0, Enter, Ctrl + X** to exit

- Create a `urls.txt` file containing one URL per line using nano. You can include as many URLs as needed

      https://example.com
      https://another-site.org

— **Run the scraper script**:

      python metaharvest.py


— **View Outputs**:
  
   - `metadata_output.json` — detailed metadata per URL.
     
   - `metadata_output.csv` — summarized tabular data for easy analysis.
 

- - - 

## Disclaimer

This tool is provided for educational, lawful, and ethical cybersecurity and OSINT purposes only. I make no warranties regarding the tool’s suitability or legality in any particular jurisdiction. Users are solely responsible for ensuring their use complies with all applicable laws, regulations, and website terms of service. The developers disclaim any liability arising from unauthorized or malicious use of this software.


- - - 


## Ethical Considerations

Use the tool responsibly by respecting website policies and privacy laws, minimizing server impact, being transparent and honest, protecting collected data, and applying it solely for lawful and ethical purposes.


- - - 

If you need any additional assistance—on resolving errors, adding features, or polishing documentation - just let me know. I’m here to help!

**Creator: Tech Enthusiast** 

**LinkedIn: http://linkedin.com/in/tech-enthusiast-669279263**

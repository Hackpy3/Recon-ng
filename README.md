# Recon-ng
Recon-ng is a powerful open-source web reconnaissance framework written in Python. It is designed for conducting web-based reconnaissance and information gathering. Recon-ng is modular, meaning it has a variety of modules that can be used to perform specific tasks such as domain enumeration, subdomain discovery, port scanning, and more.

### Uses of Recon-ng:
1. **Domain Enumeration**: Discover subdomains and related domains.
2. **Port Scanning**: Identify open ports on target systems.
3. **Whois Lookup**: Retrieve domain registration information.
4. **DNS Enumeration**: Gather DNS records and information.
5. **Social Media Profiling**: Collect information from social media platforms.
6. **Email Harvesting**: Gather email addresses associated with a domain.
7. **Vulnerability Scanning**: Identify potential vulnerabilities in web applications.
8. **Data Mining**: Extract and analyze data from various sources.

### Example Outline of Using Recon-ng:

1. **Installation**:
   - Ensure Python is installed.
   - Clone the Recon-ng repository from GitHub:
     ```bash
     git clone https://github.com/lanmaster53/recon-ng.git
     ```
   - Navigate to the Recon-ng directory and install dependencies:
     ```bash
     cd recon-ng
     pip install -r REQUIREMENTS
     ```

2. **Launching Recon-ng**:
   - Start Recon-ng:
     ```bash
     ./recon-ng
     ```

3. **Setting Up a Workspace**:
   - Create a new workspace for your project:
     ```bash
     workspaces create example_workspace
     ```
   - Switch to the new workspace:
     ```bash
     workspaces load example_workspace
     ```

4. **Adding a Domain**:
   - Add a target domain to the workspace:
     ```bash
     add domains example.com
     ```

5. **Using Modules**:
   - List available modules:
     ```bash
     marketplace search
     ```
   - Load a module, for example, the `whois_pocs` module:
     ```bash
     modules load recon/domains-contacts/whois_pocs
     ```
   - Set the target domain:
     ```bash
     options set SOURCE example.com
     ```
   - Run the module:
     ```bash
     run
     ```

6. **Viewing Results**:
   - View the results of the module execution:
     ```bash
     show hosts
     show contacts
     ```

7. **Exporting Data**:
   - Export the collected data to a file:
     ```bash
     reporting export
     ```

8. **Advanced Reconnaissance**:
   - Use additional modules for further reconnaissance, such as `google_site_web` for searching Google for site-specific information or `shodan_host` for querying Shodan for host information.

### Example Commands:
- **Search for subdomains**:
  ```bash
  modules load recon/domains-hosts/brute_hosts
  options set SOURCE example.com
  run
  ```
- **Harvest emails**:
  ```bash
  modules load recon/domains-contacts/harvester
  options set SOURCE example.com
  run
  ```
- **Check for open ports**:
  ```bash
  modules load recon/hosts-ports/shodan
  options set SOURCE example.com
  run
  ```

Here are additional **example commands** for using **Recon-ng** to perform various reconnaissance tasks. These commands demonstrate the flexibility and power of Recon-ng for different types of information gathering:

---

### 1. **Whois Lookup**:
   Retrieve domain registration information for a target domain.
   ```bash
   modules load recon/domains-contacts/whois_pocs
   options set SOURCE example.com
   run
   ```

---

### 2. **Subdomain Enumeration**:
   Use brute-force to discover subdomains of a target domain.
   ```bash
   modules load recon/domains-hosts/brute_hosts
   options set SOURCE example.com
   run
   ```

---

### 3. **DNS Enumeration**:
   Gather DNS records (A, MX, NS, etc.) for a domain.
   ```bash
   modules load recon/domains-hosts/dnsdumpster
   options set SOURCE example.com
   run
   ```

---

### 4. **Email Harvesting**:
   Collect email addresses associated with a domain using the Harvester module.
   ```bash
   modules load recon/domains-contacts/harvester
   options set SOURCE example.com
   run
   ```

---

### 5. **Google Search for Site-Specific Information**:
   Use Google to search for site-specific information (e.g., `site:example.com`).
   ```bash
   modules load recon/domains-hosts/google_site_web
   options set SOURCE example.com
   run
   ```

---

### 6. **Shodan Host Lookup**:
   Query Shodan for information about a specific host or IP address.
   ```bash
   modules load recon/hosts-ports/shodan
   options set SOURCE 192.168.1.1
   run
   ```

---

### 7. **Port Scanning**:
   Perform a port scan on a target host using the `bing_ip` module.
   ```bash
   modules load recon/hosts-ports/bing_ip
   options set SOURCE 192.168.1.1
   run
   ```

---

### 8. **Social Media Profiling**:
   Search for profiles associated with a domain on social media platforms.
   ```bash
   modules load recon/profiles-profiles/profiler
   options set SOURCE example.com
   run
   ```

---

### 9. **LinkedIn Employee Search**:
   Search for employees associated with a company on LinkedIn.
   ```bash
   modules load recon/companies-contacts/linkedin_auth
   options set SOURCE example.com
   run
   ```

---

### 10. **Vulnerability Scanning**:
   Use the `xssed` module to check for known XSS vulnerabilities.
   ```bash
   modules load recon/vulnerabilities/xssed
   options set SOURCE example.com
   run
   ```

---

### 11. **Data Mining from Pastebin**:
   Search Pastebin for leaked data related to a domain.
   ```bash
   modules load recon/domains-contacts/pastebin
   options set SOURCE example.com
   run
   ```

---

### 12. **IP Geolocation**:
   Retrieve geolocation information for an IP address.
   ```bash
   modules load recon/hosts-hosts/ipinfodb
   options set SOURCE 192.168.1.1
   run
   ```

---

### 13. **SSL Certificate Analysis**:
   Analyze SSL certificates for a domain.
   ```bash
   modules load recon/domains-hosts/ssl_san
   options set SOURCE example.com
   run
   ```

---

### 14. **Netcraft Hosting History**:
   Retrieve hosting history for a domain using Netcraft.
   ```bash
   modules load recon/domains-hosts/netcraft
   options set SOURCE example.com
   run
   ```

---

### 15. **Bing IP Search**:
   Search Bing for IP addresses associated with a domain.
   ```bash
   modules load recon/hosts-hosts/bing_ip
   options set SOURCE example.com
   run
   ```

---

### 16. **Threat Intelligence Lookup**:
   Check if a domain or IP is listed in threat intelligence databases.
   ```bash
   modules load recon/hosts-hosts/threatcrowd
   options set SOURCE example.com
   run
   ```

---

### 17. **Data Export**:
   Export collected data to a CSV file for further analysis.
   ```bash
   reporting export
   ```

---

### 18. **Module Information**:
   Get detailed information about a specific module.
   ```bash
   modules info recon/domains-hosts/brute_hosts
   ```

---

### 19It seems your message got cut off. If you were asking for more examples or additional details, let me know! Otherwise, here's one more example to round out the list:

---

### 19. **Reverse IP Lookup**:
   Find all domains hosted on the same IP address.
   ```bash
   modules load recon/hosts-hosts/reverse_resolve
   options set SOURCE 192.168.1.1
   run
   ```

---

Let me know if you'd like further clarification or additional examples!

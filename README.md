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

### Conclusion:
Recon-ng is a versatile tool for web reconnaissance, offering a wide range of modules to gather information about a target. By following the outlined steps, you can effectively use Recon-ng to perform comprehensive reconnaissance and gather valuable intelligence for your penetration testing or security assessment tasks.

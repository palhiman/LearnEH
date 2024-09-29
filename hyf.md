
# Target-domain: hack-yourself-first.com

## Information Gathering

	> 1. DNS Enumeration 

		>> dnsenum hack-yourself-first.com
		>> dig hack-yourself-first.com
		>> nslookup hack-yourself-first.com
		>> dnsrecon hack-yourself-first.com

	> 2. Port Scanning
	
		>> nmap -sS -sV -T4 hack-yourself-first.com

		>> masscan hack-yourself-first.com -p1-65535 --rate=1000
	
	> 3. Web Application Scanning

		>> nikto -h http://hack-yourself-first.com
		>> whatweb hack-yourself-first.com

		
	> 4. Directory and File Enumeration (Discovering hidden files and directories)

		>> dirb http://hack-yourself-first.com
		>> gobuster dir -u http://hack-yourself-first.com -w /usr/share/wordlists/dirb/common.txt

	> 5. SSL Information
		
		>> sslscan hack-yourself-first.com

		>> testssl hack-yourself-first.com

	> 6. Banner Grabbing

		>> nc hack-yourself-first.com 80

			>>> After connecting type:
				
				HEAD / HTTP/1.0

	> 7. Understanding website structure

		>> wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://hack-yourself-first.com
		
	> 8. Check for HTTP headers and Security Headers

		>> curl -I http://hack-yourself-first.com
		

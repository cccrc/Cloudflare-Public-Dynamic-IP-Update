# Cloudflare Public Dynamic IP Update
Updating public dynamic IP address to existing cloudflare DNS record (Only work for updating single DNS Zone)

This fork is for:
- the use of env variables instead of config file
- logging to system log instead of console

## Requirement
Using [curl](https://en.wikipedia.org/wiki/CURL), [jq](https://stedolan.github.io/jq/) (Need to install **epel-release** prior to install jq in CentOS), and [dig](https://en.wikipedia.org/wiki/Dig_(command)) command. <br/>
Check whether jq is installed on your system or not before use this script

Need to customize cloudflare_config file before using this script.
- **Auth-Key**<br>
Authorization key for cloudflare API. Able to find it at **My Profile** page. Substitute **[Your_CloudFlare_API_Auth_Key]** with your API key.<br>
*Follow this [Instruction](https://support.cloudflare.com/hc/en-us/articles/200167836-Where-do-I-find-my-Cloudflare-API-key-)*
- **Auth-Email**<br>
Your Cloudflare account login email. Substitute **[Your_CloudFlare_Account_Email]** with yours.
- **Zone-ID**<br>
You can find zone ID of your DNS Zone on the right sidebar of cloudflare DNS overview page, under API tab. Substitute **[DNS_Zone_ID_of_Your_Domain]** with yours.
- **Update-Target**<br>
Meaning list of domain address that you want to update linking ip address via this script. List must be separated by single comma(,). Substitute **[List_Of_Domain_Address_You_Want_To_Update]** with your list.<br>
*e.g. "google.com,www.google.com"*

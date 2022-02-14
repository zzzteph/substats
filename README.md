## The idea

The idea was to collect all subdomains from all public bugbounty scope, find with **amass** all subdomains, make some analysis and generate a few wordlist on the results that may be helpful.

So I collected more than a **million subdomains** for near **3000** domains from bugbounty scopes. Among them were google, paypal, apple, and many others. 
I used this resource https://github.com/arkadiyt/bounty-targets-data to gather all required data for further analysis.

What will you find in this repository?

- Some statistics with conclusions - top subdomains, masks, length statistics, etc.
- Lists with different tops of subdomains - 100,1000, 10000 for different levels.
- The whole collected list of resources.

# Abstaract 

During information gathering about the particular scope, no matter this is bugbounty or private assessments, it's always needed to find as much information. There are many examples of when some companies were hacked through high critical vulnerabilities found on their servers found through subdomain enumeration. Here you can find some statistics about subdomains in bugbounty scopes. 

Great things in subdomains that most of them have some meaning or legend that are hidden in the name, like:
- dev.services
- api
- staging
- ds1-eu-central.portal
- us-vpn-poc
- blo01-01m01-sw01 - even this nasty one(!)

So if there was a way to find how these names are generated, they might be easier to find. 
For example, you can generate a massive wordlist with all possible combinations for **us-vpn-poc**. But, how big a wordlist will it be? So, there will be at least **26^8** or **208827064576** of different combinations...Do you need to iterate all of these combinations? I'm not sure, and it will probably take near a year, even with 10000 subdomains per second.
And for **ds1-eu-central** - **milleniums of millenium**. 

To make subdomain finding easier, There are a lot of different wordlists that contain popular subdomains names that allow researchers to find targets quickly, like:
- https://wordlists.assetnote.io/
- https://github.com/theMiddleBlue/DNSenum/tree/master/wordlist
- https://gist.github.com/jhaddix/86a06c5dc309d08580a018c66354a056

And to enumerate the subdomains, you can also find many awesome tools like (each tool has also built-in wordlist):
- https://github.com/infosec-au/altdns
- https://github.com/OWASP/Amass
- https://github.com/TheRook/subbrute
- https://github.com/projectdiscovery/subfinder
- https://github.com/aboul3la/Sublist3r

So the idea was to collect all subdomains from all public bugbounty scope, find with **amass** all subdomains, make some analysis and generate a few wordlist on the results that may be helpful.


## Statistics

Everyone like it, but I will try to make it short. In futher analysis I will refer to subdomain of first 0 domains like - **analytics.google.com**.
Eights level - **analytics.1.2.3.4.5.6.7.google.com**


### TOP 10 subdomains by their levels

I replaced **www** with next popular subdomain in 0 column.  

|1|2|3|4|5|6|
|---|---|---|---|---|---|
|**api**|**mail**|ns|matching|c|**aws**| 
|m|cust|**mail**|**tms**|**aws**|c|
|dev|spider|r|isp|**tms**|net|
|**mail**|insight|ctr|**my**|paas|**tms**|
|staging|search|**stage**|internal|k8s|on|
|test|storage|ll|**aws**|s0|   |
|autodiscover|**fr**|np|dmz|us|   |
|**stage**|**us**|staff|cloud|internal|   |
|app|m| compute|community|   |   |
|blog|fwd|c|**us**|   |   |
|support|**my**|dev|**api**|   |   |

So in general - most popular subdomains have speaking name - api, mail, aws,search and etc, that fully refers to its purpose. It's important to say, that some of them appears of different of subdomain levels.
Some of them refers to the origin country - **us,fr**.

### Length statistics

So the interesting thing here, that 




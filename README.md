<p align="center">
  <img src="https://github.com/zzzteph/substats/blob/main/logo.jpg?raw=true"  height="350">
</p>


The idea was to collect all subdomains from all public bugbounty scope, find with **amass** all subdomains, make some analysis and generate a few wordlists on the results that may be helpful.

So I collected more than **million subdomains** for near **3000** domains from bugbounty scopes. Among them were **google**, **paypal**, **apple**, and many others. 
I used this resource https://github.com/arkadiyt/bounty-targets-data to gather all required data for further analysis.

What will you find in this repository?

- Lists with subdomains for different levels.
- The whole collected list of resources.
- And, of course, very-little statistics and conclusions.

# Summary 

During information gathering about the particular scope, no matter this is bugbounty or private assessments, it's always needed to find as much information. There are many examples of incidents when some companies were hacked through high critical vulnerabilities on their servers found through subdomain enumeration.

Great things in subdomains that most of them have some meaning or legend that are hidden in the name, like:
- dev.services
- api
- staging
- ds1-eu-central.portal
- us-vpn-poc
- blo01-01m01-sw01 - even this nasty one(!)

So if there was a way to find how these names are generated, they might be easier to find. 
For example, you can generate a massive wordlist with all possible combinations for **us-vpn-poc**. But, how big a wordlist will it be? So, there will be at least **26^8** or **208827064576** of different combinations... Do you need to iterate all of these combinations? I'm not sure, and it will probably take near a year, even with 10000 subdomains per second.
And for **ds1-eu-central** - **milleniums of millenium**. 

To make subdomain finding easier, There are a lot of different wordlists that contain popular subdomains names that allow researchers to find targets quickly, like:
- https://wordlists.assetnote.io/
- https://github.com/theMiddleBlue/DNSenum/tree/master/wordlist
- https://gist.github.com/jhaddix/86a06c5dc309d08580a018c66354a056

And to enumerate the subdomains, you can also find many excellent tools like (each instrument has also built-in wordlist):
- https://github.com/infosec-au/altdns
- https://github.com/OWASP/Amass
- https://github.com/TheRook/subbrute
- https://github.com/projectdiscovery/subfinder
- https://github.com/aboul3la/Sublist3r

So the idea was to collect all subdomains from all public bugbounty scope, find with **amass** all subdomains, make some analysis and generate a few wordlists on the results that may be helpful.


**So, what are top 10 subdomains for each level?**

I replaced **www** with the following popular subdomain in the 0 column.  

|0|1|2|3|4|5|
|---|---|---|---|---|---|
|**api**|**mail**|ns|matching|**c**|**aws**| 
|m|cust|**mail**|**tms**|**aws**|**c**|
|dev|spider|r|isp|**tms**|net|
|**mail**|insight|ctr|**my**|paas|**tms**|
|staging|search|**stage**|internal|k8s|on|
|test|storage|ll|**aws**|s0|   |
|autodiscover|**fr**|np|dmz|us|   |
|**stage**|**us**|staff|cloud|internal|   |
|app|m| compute|community|   |   |
|blog|fwd|**c**|**us**|   |   |
|support|**my**|dev|**api**|   |   |

So, in general - the most popular subdomains have the speaking name - **api**, **mail**, **aws**, **search**, etc., that entirely refers to its purpose. In addition, all top masks contain only latin characters.

**What is the most common length of subdomains on each level?**

On most of the most common length is **3-4** symbols.


### So this is it!

You can download the full list by following links:
|Link|Words count|Info|
|---|---|---|
|[all](https://github.com/zzzteph/substats/blob/main/wordlists/all)|401668| All valid collected subdomains with removed root domain.|
|[all_unchecked](https://github.com/zzzteph/substats/blob/main/wordlists/all_unchecked)|997285|All collected subdomains with removed root domain|
|[complex](https://github.com/zzzteph/substats/blob/main/wordlists/complex)|67265| List of words that used in complex subdomain names like **mon01-dev-test**. So the list contains words like: **mon01**,**dev**,**test**|


In the [wordlists](https://github.com/zzzteph/substats/blob/main/wordlists) folder you can find lists for each subdomain levels, from 1 to even 9*.

_*Numbering begins from 0_




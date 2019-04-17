# Project 9 - Honeypot

Time spent: **14** hours spent in total

> Objective: Set up a honeypot and intercept some attempted attacks in the wild.  


## Which Honeypot(s) you deployed

These are the honeypots I deployed:  

1. **Dionaea**: Dionaea is a honeypot which traps malware exploiting vulnerabilities exposed by services offered to a network with the ultimate goal of gaining a copy of the malware [[1](https://github.com/threatstream/mhn/wiki/Dionaea-Sensor)]. 

- [x] GIF Walkthrough:<img src="https://imgur.com/GlP8dNM.gif" width="800">

- [x] Attack Stats:<img src="https://imgur.com/9wJ1J3N.gif" width="800">

2. **Amun**:Amun is a "python-based low-interaction honeypot, following the concepts of Nepenthes but extending it with more sophisticated emulation and easier maintenance." [[2](https://github.com/threatstream/mhn/wiki/Amun-Sensor)].

- [x] GIF Walkthrough:<img src="https://imgur.com/cOHI1ft.gif" width="800">

3. **Snort**:Snort is an "open source intrusion prevention system capable of real-time traffic analysis and packet logging."[[3](https://github.com/threatstream/mhn/wiki/Snort-Sensor)]. 

- [x] GIF Walkthrough:<img src="https://imgur.com/h7FtNWt.gif" width="800">


## Any issues you encountered

The issues I encountered were mostly related to setting up of the the Virtual Machines. Since this assignment was somewhat abstract, I faced a lot of issues, such as nginx page showing (MHN homepage not loaded), no traffic on the Attack page, unable to download files, issues setting up, etc. 
I had to manually install a package `$ sudo pip install hpfeeds-threatstream==1.1` while SSH'd into the admin VM. Also I had to reset the VM multiple time and add additional firewall rules. After multiple attempts and installing mhn 2-3 times I was able to solve the issues eventually and run it successfully.

## Data Collected 

The following tables showcase statistics provided by MHN in the admin page.

#### FOR DIONAEA (I configured this separately from amun and snort)

* Attacks in last 24 hours: 1278


*Table 1 - Top 5 attacker IPs*

| No. | IP | Location | Attacks |
|:---:|:--:|:--------:|:-------:|
| 1 | 182.253.72.44 | Indonesia | 442 |
| 2 | 34.66.209.165 | U.S | 414 |
| 3 | 216.155.123.164 | U.S | 14 |
| 4 | 185.176.26.100 | Russia | 13 |
| 5 | 185.176.27.110 | Russia| 11 |


*Table 2 - Top 5 attacked ports*

| No. | Port | Attacks |
|:---:|:----:|:-------:|
| 1 | 80| 446 |
| 2 | 23 | 35 |
| 3 | 445 | 30 |
| 4 | 81 | 17 |
| 5 | 3000 | 15 |

#### FOR AMUN AND SNORT (I configured these 2 separately from Dionaea)

* Attacks in last 24 hours: 11

*Table 1 - Top 5 attacker IPs*

| No. | IP | Location | Attacks |
|:---:|:--:|:--------:|:-------:|
| 1 | 89.248.168.51 | Seychelles | 1 |
| 2 | 223.87.241.20 | China |1 |
| 3 | 81.22.45.231 | Unknown Network | 1 |
| 4 | 80.44.65.196 | U.K | 1 |
| 5 | 217.58.65.187 | Italy| 1 |


*Table 2 - Top 5 attacked ports*

| No. | Port | Attacks |
|:---:|:----:|:-------:|
| 1 | 23 | 4 |
| 2 | 8010 | 1 |
| 3 | 10025 | 1 |
| 4 | 3389 | 1 |
| 5 | 7547 | 1 |

* Top 5 Honey Pots: 
1. amun (9 attacks)
2. snort (2 attacks)

#### Lastly, file [session1.json](./session1.json) contains all the data collected by Dionaea. And file [session2.json](./session2.json) contains all the data collected by amun and snort.

## Any unresolved questions raised by the data collected

No such unresolved issue or question raised by the data collected so far. If more wait time was given/possible more number of attacks could have been observed for `amun` and `snort`.

## Resources

* [Google Cloud Platform documentation](https://cloud.google.com/docs/)
* [MHN, list of supported sensors](https://github.com/threatstream/mhn/wiki/List-of-Supported-Sensors)



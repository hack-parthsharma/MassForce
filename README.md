# Sub-Domains Enumeration Tools

### This repo has two parts:
1. The BruteForce Techniques.
2. The Reverse Lookup Techniques.

## BruteForce Techniques.

There was a lot of tools that do the brute-force techniques, but a few of them that were producing high performance with this techniques like massDNS but the rate of the false positive was very high in my experience, so i decided to build my own tool, after a lot of research i found a library called adns that was capable of sending a lot of dns queries asynchronously.

The tool is capable of performing brute force of 30,000 subdomains in one minute with a very high success rate.

I used the best wordlist commonspeak.txt .

```
pip install adns-python
sed -e 's/$/.example.com/' commonspeak.txt > company_profile.txt
python MassForce.py company_profile.txt
```

## Reverse Lookup Techniques.

With the same previous situation and mindset, i tried to build a reverse lookup dns asynchronous tool.

The tool is also capable of performing brute force of 30,000 IPs in one minute with a very high success rate.

```
pip install adns-python
python MassForceRev.py 8.8.0.0 8.8.64.255
```

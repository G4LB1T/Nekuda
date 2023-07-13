# Nekuda - IDN-Squatting Detector
## Domain Lookalikes
A domain lookalike is a domain name that is similar to a legitimate domain name, but with slight differences. These differences can be in the spelling of the domain name, the top-level domain (TLD), or the extension. Domain lookalikes are often used in phishing attacks, where attackers attempt to trick users into entering their personal information on a fake website.
For example, one may try and fool users with the domain `micros0ft.com`, trying to mimic `microsoft.com`.
## Internationalized Domain Name and IDN TLDs
An internationalized domain name (IDN) is an Internet domain name that contains at least one label displayed in software applications, in whole or in part, in non-Latin script or alphabet or in the Latin alphabet-based characters with diacritics or ligatures. These writing systems are encoded by computers in multibyte Unicode. Internationalized domain names are stored in the Domain Name System (DNS) as ASCII strings using Punycode transcription.
Here are a few examples of IDNs:
- `スターバックスコ리아.com` (Korean)
- `漢語.com` (Chinese)
- `भारत.com` (Hindi)
- `العربية.com` (Arabic)

In order to be compatible with components expecting ASCII input, these characters must be encoded in Punycode. It is an ASCII-compatible encoding of Unicode characters that allows internationalized domain names (IDNs) to be used across the entire internet. 
Out of the 1470 available top-level domain names (e.g. `.com`) there are currently 152 IDN TLDs - reflecting other non-country specific TLDs as `.com` or `.net` in native tongues alongside localized ones as `.한국` (Korea), `.укр` (Ukraine) and others.
## IDN-Squatting
This is a new disruptive concept devised by the authors of this tool - instead of integrating non-ASCII characters as part of the domain - register the entire domain in the target's native tongue. For example, instead of `microsoft.com` register any of the following domains:
- `微软.公司` (Chinese)
- `마이크로소프트.닷컴` (Korean)
- `Ма́йкрософт.ком` (Russian)
- `ไมโครซอฟท์.คอม` (Thai)
- `माइक्रोसॉफ्ट.कॉम` (Hindi)
- `مايكروسوفت.كوم` (Arabic)
- `מיקרוסופט.קום` (Hebrew)

## Nekuda
### What is Nekuda?
Nekuda is a Python notebook that given an input keyword will yield potential IDN-Squat-able domains. Its goal is to educate about this potential new technique for creating phishing pages alongside assisting defenders in tracking down these domains in the near future.
## Using Nekuda
First, to make sure you have all of the required Python dependencies, run:
```
> pip install requirements.txt
```
In order to run the tool you will need a GCP account and enable [Cloud Translation API](https://cloud.google.com/translate/docs/reference/libraries/v2/python). Setting it is beyond the scope of this guide, as well as creating a JSON with Google's application credentials but there are plenty of [adequate guides by Google](https://cloud.google.com/docs/authentication/application-default-credentials#GAC) for this topic.

Once you've fulfilled both Python and GCP requirements all that is left is to change the variable `idn_squatting_target` to the brand you wish to protect then run the entire notebook. If this is your first time with Python Notebook we recommend either [this guide](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html) from Jupyter or [this one](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) by VS Code's team.

## Creators
- Adi Pick [Linkedin](https://www.linkedin.com/in/adi-pick-52b97916a/)
- Gal Bitensky [LinkedIn](https://www.linkedin.com/in/gal-bitensky/) [Twitter](https://twitter.com/gal_b1t)

This tool was first released as part of [BlackHat USA 2023 Arsenal](https://www.blackhat.com/us-23/arsenal/schedule/#nekuda-idn-squatting-detector-33540)

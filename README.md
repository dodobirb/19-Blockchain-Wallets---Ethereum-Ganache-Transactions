# Module_19_Challenge
FinTech Boot Camp Module 19 Challenge: Blockchain Wallets

Our new platform *Fintech Finder* is an application that customers can use to find fintech professionals from among a list of candidates, hire them, and pay them. The Ethereum blockchain network has been integrated into the application in order to enable customers to instantly pay the fintech professionals whom they hire with cryptocurrency.

To develop the code and test it out, the perspective of a Fintech Finder customer has been assumed: they are using the application to find a fintech professional and pay them for their work.

The first file is *fintech_finder.py*. It contains the code associated with the web interface of the application. The code included in this file is compatible with the Streamlit library.

The second file is *crypto_wallet.py*. This file contains the Ethereum transaction functions needed to execute *fintech_finder.py* through the use of 'import' statements. Integrating these two files allows task automation associated with generating a digital wallet, accessing Ethereum account balances, and signing and sending transactions via a personal Ethereum blockchain (Ganache).

---

## Ganache & Interface View

Ganache address balance & history:

![Ganache address balance & history](./my_address_balance_history_ganache.png)

Ganache transaction details:

![Ganache transaction details](./transaction_details_ganache.png)

Interface - Validated transaction hash (bottom left):

![Interface - Validated transaction hash](./validated_trans_hash_bottomleft.png)

---

## Technologies

This application was written in Python 3.9.4 on a Windows 10 machine. 

[Ganache](https://trufflesuite.com/docs/ganache/index.html) is a personal blockchain for rapid Ethereum and Corda distributed application development. You can use Ganache across the entire development cycle; enabling you to develop, deploy, and test your dApps in a safe and deterministic environment. In this case, it was used to generate Ethereum-connected mock accounts with which to mimic transactions. All versions of Ganache are available for Windows, Mac, and Linux.

[Streamlit](https://docs.streamlit.io/library/get-started) is an open-source Python library that makes it easy to create and share custom web apps for machine learning and data science. The library imported for this program includes a 'Get Started' guide, API reference, and more advanced features of the core library including caching, theming, and Streamlit Components. Cloud deployment services are offered as well.

---

## Installation Guide

Ensure through your local terminal that your development environment supports the following imports and dependencies:

### fintech_finder.py
```
import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3
w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545')) 
# Developer's Ganache tester accounts. Please indicate your own HTTP Provider.
```

### crypto_wallet.py
```
import os
import requests
from dotenv import load_dotenv
from bip44 import Wallet
from web3 import Account
from web3 import middleware
from web3.gas_strategies.time_based import medium_gas_price_strategy
```

If it does not, reference your terminal installation guide to download the missing software.

---

## Contributors

Brought to you by lead developer Erin Kenny at FintechFinder.

[Email](ekenny3@uncc.edu)

[LinkedIn](www.linkedin.com/in/e-kenny)

---

## License

MIT

License file included in repository.

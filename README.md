# 🚀 GM Free Proxy Rotator

A secure, auto-rotating free proxy generator for Python developers. Get fresh HTTP/HTTPS proxies on every request automatically!

---

## 🛠️ Installation

You can install this module directly from GitHub using `pip`:

```bash
pip install git+https://github.com/malik498-r/gm-free-proxy.git
```

## 🔑 How to Get Your Access Key

To use this library, you need a monthly activation key.
Go to this link to generate your temporary key: Get Key Here
Follow the short instructions on the page to copy the code.

## 🚀 Usage Guide

Here is a simple example of how to configure the key and fetch rotating proxies in your python scripts:

```python
import gm_free_proxy
import requests

# 1. Set your monthly access key (Only needs to be run once)
gm_free_proxy.set_key("YOUR_COPIED_KEY_HERE")

# 2. Fetch a fresh, unique proxy automatically
proxy = gm_free_proxy.get_proxy()
print("Current Proxy Assigned:", proxy)

# 3. Use it directly with the requests library
try:
    response = requests.get("https://httpbin.org/ip", proxies=proxy, timeout=5)
    print("Your Masked IP:", response.json())
except Exception as e:
    print("Proxy connection timed out, trying next request...")
```

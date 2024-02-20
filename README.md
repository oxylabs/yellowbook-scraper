# Yellowbook Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Yellowbook Scraper](https://oxylabs.io/products/scraper-api/web/yellowbook?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Yellowbook website effortlessly. This brief guide showcases how Yellowbook Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Yellowbook results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Yellowbook page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.yellowbook.com/lp/fa74ac/1/loading?fn=&ln=&city=united+states&state=all#.'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/yellowbook-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html>\n\n<head>\n<meta name=\"robots\" content=\"noindex, nofollow\">      <script src=\"ht ... </html>",
      "created_at": "2024-02-20 12:35:28",
      "updated_at": "2024-02-20 12:35:32",
      "page": 1,
      "url": "https://www.yellowbook.com/lp/fa74ac/1/loading?fn=&ln=&city=united+states&state=all#.",
      "job_id": "7165685389053677569",
      "status_code": 200
    }
  ]
}
```
With our Yellowbook Scraper, you can easily gather public data from Yellowbook’s business listings. Gather essential data like business name, contact details, hours of operation, and location to enhance your research and stay ahead in your industry. If you need further assistance, our support team is ready to help you via live chat, or you can email us at hello@oxylabs.io.
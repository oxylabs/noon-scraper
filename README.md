# Noon Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Noon Scraper](https://oxylabs.io/products/scraper-api/ecommerce/noon?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Noon website effortlessly. This brief guide showcases how Noon Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Noon results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Noon page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.noon.com/uae-en/telco-sale/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/noon-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-AE\" dir=\"ltr\" data-version=\"v3.9.98\" data-commit=\"a7663\"><head><meta c ... </html>",
      "created_at": "2024-02-20 12:44:54",
      "updated_at": "2024-02-20 12:44:55",
      "page": 1,
      "url": "https://www.noon.com/uae-en/telco-sale/",
      "job_id": "7165687761259750401",
      "status_code": 200
    }
  ]
}
```
With our Noon Scraper, you can seamlessly gather public data from every Noon web page. Gather vital product details, such as price, customer ratings, and detailed descriptions, to gain insights into the market and outperform your business rivals. If you require any assistance, reach out to our support team via live chat or email us at hello@oxylabs.io.
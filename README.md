# Contact-Details Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Contact-Details Scraper](https://oxylabs.io/products/scraper-api/web/contact-details-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Contact-Details website effortlessly. This brief guide explains how an Contact-Details Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Contact-Details results by providing your own URLs to our service. We can return the HTML for any Contact-Details page you like.

#### Python code example

The example below illustrates how you can get HTML of Contact-Details page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://oxylabs.io/about-us'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/contact-details-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta name=\"viewport\" content=\"width=de ... </html>",
      "created_at": "2023-12-18 11:38:26",
      "updated_at": "2023-12-18 11:38:28",
      "page": 1,
      "url": "https://oxylabs.io/about-us",
      "job_id": "7142478211106999297",
      "status_code": 200
    }
  ]
}
```
With our Contact-Details Scraper, you can easily retrieve public information from any Contact-Details webpage. Gather essential information such as phone numbers, email addresses, or mailing addresses to better understand your target audience and stay ahead of your competitors. If you need any additional support, our team is always ready to help! Feel free to reach out through our live chat or send an email to hello@oxylabs.io.
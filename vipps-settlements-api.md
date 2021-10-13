# Vipps eCommerce API

The Vipps Settlements API is used by
[Vipps på nett](https://vipps.no/produkter-og-tjenester/bedrift/ta-betalt-paa-nett/ta-betalt-paa-nett/),
[Vipps Checkout](https://vipps.no/produkter-og-tjenester/bedrift/ta-betalt-paa-nett/vipps-checkout/),
[Vipps i kassa (POS)](https://vipps.no/produkter-og-tjenester/bedrift/ta-betalt-i-butikk/vipps-i-kassa/),
native apps and other solutions.

These Swagger/OpenAPI representations may be useful to get a quick overview:
* [Swagger](https://vippsas.github.io/vipps-settlements-api/)
* [ReDoc](https://vippsas.github.io/vipps-settlements-api/redoc.html)

See: Vipps Settlements API [GitHub repository](https://github.com/vippsas/vipps-settlements-api).

API version: 0.0.1.

Document version 0.0.1.

## Table of contents

- [Authentication](#authentication)
- [Example usage](#example-usage)
  * [Request](#request)
  * [Response](#response)
- [Questions?](#questions-)

# Authentication

Please see:
[Quick overview of how to make an API call](https://github.com/vippsas/vipps-developers/blob/master/vipps-getting-started.md#quick-overview-of-how-to-make-an-api-call)
in the
[Getting started guide](https://github.com/vippsas/vipps-developers/blob/master/vipps-getting-started.md).

# Example usage

## Request

This will retrieve transactions for MSN 123456
from (and including) January 1 2021
to (and including) December 31 2021:

[`GET:/experimental/salesunits/123456/transactions?firstdate=2021-01-01&lastdate=2021-12-31`](https://vippsas.github.io/vipps-settlements-api/#/Settlements/get-transactions-date-range)

Headers:

```
Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1Ni <snip>
Ocp-Apim-Subscription-Key: 0f14ebcab0ec4b29ae0cb90d91b4a84a
Merchant-Serial-Number: 123456
Vipps-System-Name: Acme Enterprises Ecommerce DeLuxe
Vipps-System-Version: 3.1.2
Vipps-System-Plugin-Name: Point Of Sale Excellence
Vipps-System-Plugin-Version: 4.5.6
Content-Type: application/json
```

## Response

Let's pretend there were two transactions:

```
[
  {
    "orderId": "acme-shop-123-order123abc-1",
    "transactionId": "54321",
    "transactionDate": "2018-11-14T15:22:46.680Z",
    "amount": 49900,
    "message": "One pair of Vipps socks"
  }
  {
    "orderId": "acme-shop-123-order123abc-2",
    "transactionId": "54321",
    "transactionDate": "2018-11-14T15:22:46.681Z",
    "amount": 99800,
    "message": "Two pair of Vipps socks"
  }
]
```

# Questions?

We're always happy to help with code or other questions you might have!
Please create an [issue](https://github.com/vippsas/vipps-settlements-api/issues),
a [pull request](https://github.com/vippsas/vipps-settlements-api/pulls),
or [contact us](https://github.com/vippsas/vipps-developers/blob/master/contact.md).

Sign up for our [Technical newsletter for developers](https://github.com/vippsas/vipps-developers/tree/master/newsletters).

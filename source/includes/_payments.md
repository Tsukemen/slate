# Payment Processing

## Introduction

The Blockchain Receive Payments API V2 is the quickest and easiest way to begin accepting automated bitcoin payments. Consisting of just a simple HTTP GET request, you can be up and running in minutes.

One of the difficulties involved with receiving bitcoin payments is the need to generate a unique address for each new user or invoice. These addresses need to monitored and stored securely. The blockchain receive payments API takes care of the generation and monitoring of addresses. We will notify your server using a simple callback whenever a payment is received.

## Requesting an API key

In order to use the Receive Payments API V2, please apply for an API key [here](https://api.blockchain.info/v2/apikey/request/). This API key is only for our Receive Payments API. You cannot use the standard blockchain wallet API key for Receive Payments V2, and vice versa.

## Obtaining an Extended Public Key (xPub)

This API requires you to have a BIP 32 account xPub in order to receive payments. The easiest way to start receiving payments is to open a [Blockchain Wallet](https://blockchain.info/wallet/#/signup). You should create a new account inside your wallet exclusively for transactions facilitated by this API. When making API calls, use the xPub for this account (located in **Settings -> Addresses -> Manage -> More Options -> Show xPub**).




> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.


Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>


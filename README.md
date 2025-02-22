# graphcms-utils

## Install

```bash
npm i graphcms-utils
```

## Usage

### `verifyWebhookSignature`

```js
const { verifyWebhookSignature } = require("graphcms-utils");

const secret = "rCNwyiloY3oJYYkxgpBXaleIiUv5MYlx";

const body = {}; // Typically req.body

const signature = verifyWebhookSignature({ body, secret });
```

### `generateWebhookSignature`

This is useful for testing signed webhooks. You can generate a GraphCMS webhook signature, and then use it to test your webhook.

```js
const { generateWebhookSignature } = require("graphcms-utils");

const secret = "rCNwyiloY3oJYYkxgpBXaleIiUv5MYlx";

const body = {
  hello: "world",
};

const signature = generateWebhookSignature({ body, secret });
```

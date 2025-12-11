# AudioPod AI Developer Documentation

This is the developer documentation for AudioPod AI, built with [Mintlify](https://mintlify.com).

## Structure

```
docs/
├── index.mdx           # Landing page
├── quickstart.mdx      # Complete onboarding (CLI + dashboard)
├── account/
│   ├── api-keys.mdx    # API key management
│   └── api-wallet.mdx  # Pricing & billing
├── sdks/
│   ├── overview.mdx    # SDK comparison
│   ├── python.mdx      # Python SDK docs
│   └── nodejs.mdx      # Node.js SDK docs
└── api-reference/      # OpenAPI-generated API docs
```

## Local Development

```bash
npm i -g mintlify
mintlify dev
```

## Key Features

- **CLI-first onboarding**: Developers can register, verify, and create API keys entirely via cURL
- **Pay-as-you-go pricing**: No subscriptions required for API access
- **LLM integration**: Code blocks can be copied directly to ChatGPT, Claude, Cursor, etc.
- **Interactive API playground**: Test endpoints directly in the docs

## CLI Registration Flow

```bash
# 1. Register
curl -X POST "https://api.audiopod.ai/api/v1/auth/initiate-registration" \
  -H "Content-Type: application/json" \
  -d '{"email": "you@example.com", "password": "Pass123", "full_name": "Name"}'

# 2. Verify (use code from email)
curl -X POST "https://api.audiopod.ai/api/v1/auth/verify-registration" \
  -H "Content-Type: application/json" \
  -d '{"email": "you@example.com", "verification_code": "123456"}'
# → Returns access_token

# 3. Create API key
curl -X POST "https://api.audiopod.ai/api/v1/auth/api-keys" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -d '{"name": "my-key", "scopes": ["*"]}'
# → Returns api_key

# 4. Add funds
curl -X POST "https://api.audiopod.ai/api/v1/api-wallet/topup/checkout" \
  -H "X-API-Key: $AUDIOPOD_API_KEY" \
  -d '{"amount_cents": 500}'
# → Returns Stripe checkout URL

# 5. Use the API
curl -X POST "https://api.audiopod.ai/api/v1/stem-extraction/api/extract" \
  -H "X-API-Key: $AUDIOPOD_API_KEY" \
  -F "url=https://youtube.com/watch?v=..." \
  -F "mode=six"
```

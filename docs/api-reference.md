# API Reference

The Cumulus Platform exposes a REST API for integrating workflows and agents
into your own systems.

## Base URL

```
https://<your-tenant>.api.naviant.io
```

The Naviant team can provide the exact base URL for your tenant. Request it
through [Naviant Customer Support](https://naviant.com/customer-support/).

## Authentication

All API requests must be authenticated. The platform uses token-based
authentication; include your token in the `Authorization` header:

```http
Authorization: Bearer <your-token>
```

!!! warning
Treat API tokens as secrets. Do not commit them to source control or share
them. Rotate tokens if you suspect they have been exposed.

## Example request

```bash
curl -H "Authorization: Bearer $TOKEN" \
  https://<your-tenant>.api.naviant.io/health
```

## Responses

The API returns JSON. Standard HTTP status codes indicate success or failure:

| Code  | Meaning                                 |
| ----- | --------------------------------------- |
| `200` | Success                                 |
| `401` | Authentication failed                   |
| `403` | Not authorized for this resource        |
| `404` | Resource not found                      |
| `5xx` | Server error — retry or contact support |

!!! info
Detailed, endpoint-level API documentation is available to integrators on
request through
[Naviant Customer Support](https://naviant.com/customer-support/).

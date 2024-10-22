# github-extension-dify
github extension call dify api build personal QA System
github-extension-dify is a basic example of a GitHub Copilot Extension.It call dify API to build personal QA System. This repository should serve as an example of the building blocks of a Copilot Extension. See index.js for the main logic.

## Dify API Integration

This project integrates with the Dify API to answer questions. The Dify API is used to generate responses to user messages. The integration details are as follows:

### API Endpoint

The Dify API endpoint used is:
```
http://135.224.232.86/v1/chat-messages
```

### Request Headers

The following headers are used in the request:
```
Authorization: Bearer {api_key}
Content-Type: application/json
```

### Request Payload

The request payload is formatted as follows:
```json
{
    "inputs": {},
    "query": "What are the specs of the iPhone 13 Pro Max?",
    "response_mode": "streaming",
    "conversation_id": "",
    "user": "abc-123",
    "files": [
        {
            "type": "image",
            "transfer_method": "remote_url",
            "url": "https://cloud.dify.ai/logo/logo-site.png"
        }
    ]
}
```

### Response

The response from the Dify API is streamed back to the user.

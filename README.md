# ChatGPT-to-API
Create a fake API using ChatGPT's website

**API endpoint: http://127.0.0.1:8080/v1/chat/completions.**

## Setup
    
### Authentication
  
Access token retrieval has been automated by [OpenAIAuth](https://github.com/acheong08/OpenAIAuth/) with account email & password.

`accounts.txt` - A list of accounts separated by new line 

Format:
```
email:password
...
```

All authenticated access tokens will store in `access_tokens.json`

Caution! please use unblocked ip for authentication, first login to `https://chat.openai.com/` to check ip availability if you can.

## Getting set up
```  
git clone https://github.com/xqdoo00o/ChatGPT-to-API
cd ChatGPT-to-API
go build
./freechatgpt
```

### Environment variables
  - `PUID` - A cookie found on chat.openai.com for Plus users. This gets around Cloudflare rate limits
  - `SERVER_HOST` - Set to 127.0.0.1 by default
  - `SERVER_PORT` - Set to 8080 by default

### Files (Optional)
  - `proxies.txt` - A list of proxies separated by new line

    ```
    http://127.0.0.1:8888
    ...
    ```
  - `access_tokens.json` - A JSON array of access tokens for cycling (Alternatively, send a PATCH request to the [correct endpoint](https://github.com/acheong08/ChatGPT-to-API/blob/master/docs/admin.md))
    ```
    ["access_token1", "access_token2"...]
    ```

## Admin API docs
https://github.com/acheong08/ChatGPT-to-API/blob/master/docs/admin.md

## API usage docs
https://platform.openai.com/docs/api-reference/chat

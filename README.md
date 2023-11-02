# chatnio-blob-service
File Service for Chat Nio

## Supported File Types
- Text
- Image
- Audio (_require Azure Speech to Text Service_)
- Docx
- Pdf
- Pptx
- Xlsx


## Run
```shell
pip install -r requirements.txt
uvicorn main:app --reload
```
Then the service will be running on `http://localhost:8000`

## Deploy
```shell
uvicorn main:app --host
```

## API
`POST` `/upload` Upload a file
```json
{
    "file": "file"
}
```

Response

```json
{
  "status": true,
  "content": "...",
  "error": ""
}
```

Environment Variables
```shell

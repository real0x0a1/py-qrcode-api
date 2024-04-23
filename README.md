Certainly! Here's the updated README.md:

---

# QR Code Generator API

## Overview

The QR Code Generator API is a simple web service that allows you to generate QR codes from text data. This API is perfect for integrating QR code generation functionality into your applications, websites, or services.

## Usage

To use the QR Code Generator API, send a POST request to the provided API endpoint with JSON data containing the text you want to encode.

API Base URL: `https://api-qrcode-hlsl.onrender.com`

Endpoint: `POST /generate_qr`

Example request using cURL:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"data": "TEXT"}' https://api-qrcode-hlsl.onrender.com/generate_qr --output OUTPUT.png
```

Replace `TEXT` with the data you want to encode, and `OUTPUT.png` with the desired filename for the generated QR code image.

## Example

Here's an example of how you can use the API to generate a QR code:

```python
import requests

data = {
    "data": "Hello, World!"
}

response = requests.post("https://api-qrcode-hlsl.onrender.com/generate_qr", json=data)

with open("output.png", "wb") as f:
    f.write(response.content)
```

This will generate a QR code with the text "Hello, World!" and save it as `output.png` in the current directory.

## Author

This project was created by [real0x0a1](https://github.com/real0x0a1).

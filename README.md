# TinyPesa Bulk STK Push Bot (Fixed)

A Flask web application for sending bulk M-Pesa STK Push notifications via the TinyPesa API.

## ⚠️ Important Fix

This version uses the **correct TinyPesa API format**:
- `Content-Type: application/x-www-form-urlencoded`
- `ApiKey` header for authentication
- `msisdn` field for phone numbers

## Quick Start

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Copy `.env.example` to `.env` and add your **TinyPesa API Key**
4. Run: `python app.py`

## Getting Your API Key

1. Sign up at [tinypesa.com](https://tinypesa.com)
2. Go to Dashboard → Developer/API
3. Copy your **API Key** (not username)

## Deployment

### Render
1. Push to GitHub
2. Connect repository on Render
3. Add environment variable: `TINYPESA_API_KEY`
4. Deploy!

## Troubleshooting No STK Prompt

If you're not receiving prompts:

1. **Check API Key** - Ensure it's copied correctly from dashboard
2. **Phone Format** - Use 2547XXXXXXXX format (auto-converted in app)
3. **Network** - Ensure your phone has good Safaricom signal
4. **SIM Card** - Update your SIM by dialing *234*1*6#
5. **iPhone Users** - e-SIM can block STK prompts; use physical SIM
6. **Check Response** - Look at the app results for error messages

## Usage

1. Enter amount per recipient
2. Paste phone numbers (one per line)
3. Click "Send STK Push to All"
4. Recipients receive M-Pesa PIN prompt on their phones

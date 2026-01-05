# 🧀 Amul Stock Checker with Voice Notifications

An intelligent automation workflow that monitors Amul product availability and calls your phone when items are back in stock. No more manual refreshing or missed restocks!

## 🎯 What It Does

This n8n workflow automates the entire stock checking process for Amul protein products:

1. **Captures your preferences** - Pincode and phone number via a web form
2. **Reverse engineers authentication** - Extracts and maintains Amul's session cookies
3. **Monitors stock availability** - Continuously checks product availability for your location
4. **Calls you instantly** - Uses ElevenLabs AI agent to make a real phone call when your selected products are in stock
5. **Smart retry logic** - Automatically retries every few minutes (editable) if products are out of stock

## ✨ Key Features

- 🔐 **Session Management** - Automatically handles Amul's cookie-based authentication
- 📍 **Location-aware** - Checks stock based on your pincode and substore
- ☑️ **Product Selection** - Choose which specific protein products to monitor
- 📞 **Voice Notifications** - Real AI-powered phone calls (not texts or emails you'll ignore)
- 🔄 **Intelligent Retry** - Configurable wait time between checks (default: 3 minutes)
- ✅ **Availability Filtering** - Only notifies when YOUR selected items are in stock


## 🛠️ Technical Stack

- **n8n** - Workflow automation platform
- **ElevenLabs API** - AI voice agent for phone calls
- **Amul Shop API** - Product and inventory data
- **Custom JavaScript** - Cookie handling and data processing

 ## 📋 Prerequisites

Before you begin, ensure you have:

- n8n instance (self-hosted or cloud)
- ElevenLabs account with:     
  - API credentials
  - Configured AI agent
  - Twilio phone number integration
  - [Youtube video here for this setup](https://www.youtube.com/watch?v=1_ebl-acp6M)
- Basic understanding of n8n workflows

## 🚀 Installation

### Step 1: Import the Workflow

1. Copy the contents of `Amul Protien.json`
2. In n8n, go to **Workflows** → **Import from File** or **Import from URL**
3. Paste the JSON content
4. Click **Import**

### Step 2: Configure ElevenLabs Credentials

1. In n8n, go to **Credentials** → **Add Credential**
2. Select **ElevenLabs API**
3. Enter your API key
4. Save with the name: `ElevenLabs account`

### Step 3: Update ElevenLabs Configuration

In the **"Call Agent"** node, update these values:

```javascript
{
  "agent_id": "YOUR_AGENT_ID",
  "agent_phone_number_id": "YOUR_PHONE_NUMBER_ID",
  // ... rest of config
}
```

### Step 4: Activate the Workflow

1. Click **Active** toggle in the top-right
2. The form trigger will generate a webhook URL


## 📄 License

This project is provided as-is for educational and personal use. Please respect Amul's terms of service and use responsibly.

## 🙏 Acknowledgments

- **Amul** - For their e-commerce platform
- **ElevenLabs** - For AI voice technology
- **n8n** - For the incredible workflow automation platform

---

**Made with ❤️ and a lot of reverse engineering**

*Stop refreshing. Start automating.* 🚀

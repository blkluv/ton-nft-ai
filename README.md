# 🤖 TON AI NFT Generator

**`imageai.py`** automatically creates NFTs with AI-generated images based on **transactions in the TON blockchain**, using the **GetGems API**.  
📘 [GetGems API Documentation](https://api.getgems.io/public-api/docs)

---

## 🎮 How It Works

This project allows anyone to mint AI-generated NFTs simply by sending a TON transaction with a text prompt.

When a transaction >0.02 TON is detected, the script:
1. Parses your comment (prompt)
2. Generates an image using AI
3. Uploads the image to file hosting
4. Automatically mints an NFT on **GetGems**

---

## 🚀 Quick Start

### 1️⃣ Run the Script

```bash
python imageai.py
🚀 AI NFT Generator launched!
👛 Wallet address: EQCP3m3nG7T6atRKXx53pDPhsbks--KvVNlrHqayKhMjKeCY (customizable)
💡 Send >0.02 TON with a comment as your prompt
🤖 The AI will generate an image and mint it as an NFT
============================================================
2️⃣ Send a Transaction

Network: TON Testnet

Address: EQCP3m3nG7T6atRKXx53pDPhsbks--KvVNlrHqayKhMjKeCY

Minimum Amount: 0.02 TON (for NFT minting)

Comment: Your AI image prompt

3️⃣ Watch the Magic ✨

The script automatically:

Detects your transaction

Generates an AI image

Uploads it to file hosting

Mints an NFT and sends it to your wallet

graph TD
    A[Transaction >0.02 TON] --> B[Parse prompt]
    B --> C[AI generates image]
    C --> D[Upload to hosting]
    D --> E[Mint NFT]
    E --> F[NFT delivered to sender’s address]

⚙️ Step-by-Step Breakdown
🕵️ 1. Transaction Monitoring

Checks new transactions every 5 seconds

Skips transactions <0.02 TON

Uses TON Center API + GetGems API

🎨 2. AI Image Generation

API: NeuroImg.art

Model: AniFlux-v4.1

Resolution: 1024x1024 px

Steps: 25

Format: PNG

📤 3. Image Uploading

Uses upload.py to upload AI-generated files

Stores images on file hosting

Returns a permanent image link (AI’s raw link may not be valid for minting)

🪙 4. NFT Minting

Platform: GetGems (testnet/mainnet)

Collection: Configurable in settings

Attributes: Includes prompt + generator type

Owner: Transaction sender

📥 Found new transactions: 1
🎯 Processing transaction: 0.03 TON, prompt: 'spaceship'
🎨 Generating image for prompt: 'spaceship'
🕒 Queue: 2/8
🎨 Generating image...
✅ Image ready!
📥 Downloading image: https://ai-api.test/i/12345678.png
✅ Uploaded: http://mysite.com/loads/abc123.png
📦 Minting NFT...
✅ NFT created successfully!
🔗 View: https://testnet.getgems.io/collection/.../NFT_ADDRESS

<img width="1809" height="1011" alt="Screenshot 2026-06-06 112824" src="https://github.com/user-attachments/assets/19214eac-5977-4d28-8c39-82928418b5a8" /># WooCommerce Telegram Order Notifier

Instant Telegram notifications for every new WooCommerce order.

A lightweight and easy-to-use WordPress plugin that sends real-time WooCommerce order alerts directly to your Telegram account or group using the Telegram Bot API.

---<img width="709" height="1600" alt="epImage " src="https://github.com/user-attachments/assets/6f2f69cb-7208-4955-a556-0b82f620ea4e" />



# Features

* Instant Telegram notifications for new WooCommerce orders
* Simple Telegram Bot integration
* Supports private chats and Telegram groups
* Includes:

  * Customer name
  * Email
  * Phone number
  * Ordered products
  * Payment method
  * Order total
  * Order status
  * Billing address
  * Admin order link
* Test notification button
* Lightweight and fast
* WooCommerce HPOS compatible
* Secure settings handling
* No third-party services required

---
#
# Requirements

* WordPress 5.8+
* PHP 7.4+
* WooCommerce 5.0+
* Telegram account
* Telegram Bot Token
* Telegram Chat ID

---

# Installation

## Method 1 — Upload ZIP

1. Download the plugin ZIP file
2. Go to WordPress Admin → Plugins → Add New
3. Click **Upload Plugin**
4. Upload the ZIP file
5. Activate the plugin

---

## Method 2 — Manual Installation

1. Extract the plugin files
2. Upload the plugin folder to:

```text
/wp-content/plugins/
```

3. Activate the plugin from the WordPress Plugins page

---

# Setup Guide

After activation:

1. Go to:

```text
WooCommerce → Telegram Orders
```

2. Enter:

   * Telegram Bot Token
   * Telegram Chat ID

3. Save settings

4. Click:

```text
Send Test Notification
```

to verify the connection.

---

# Create a Telegram Bot

1. Open Telegram
2. Search for:

```text
@BotFather
```

3. Start the chat
4. Send:

```text
/newbot
```

5. Follow the instructions
6. Copy the generated bot token

---

# Get Telegram Chat ID

## Personal Chat

1. Open your bot chat
2. Press **Start**
3. Send any message to the bot

Now open:

```text
https://api.telegram.org/botYOUR_BOT_TOKEN/getUpdates
```

Replace:

```text
YOUR_BOT_TOKEN
```

with your actual bot token.

Find:

```json
"chat": {
  "id": 123456789
}
```

Copy the `id` value and use it as your Chat ID.

---

## Telegram Group

1. Add the bot to your Telegram group
2. Send a message in the group
3. Run `getUpdates` again
4. Copy the group chat ID

Group IDs usually look like:

```text
-1001234567890
```

---

# Notification Example

```text
🛒 New WooCommerce Order

Order #1024
Customer: John Doe
Phone: +1 555-1234
Email: john@example.com

Products:
• Product A × 2
• Product B × 1

Payment: Cash on Delivery
Total: $149.00
Status: Processing
```

---

# Security

* Uses WordPress Settings API
* Uses nonces for secure form submissions
* Sanitized and escaped data
* Uses WordPress HTTP API
* Only WooCommerce managers/admins can access settings

---

# Troubleshooting

## Bot not sending messages

Make sure:

* The bot token is correct
* You started the bot chat
* The chat ID is correct
* Your hosting allows outgoing requests to:

```text
api.telegram.org
```

---

## Error: `chat not found`

Usually means:

* Wrong chat ID
* Bot not started
* Bot not added to group

---

## Error: `Unauthorized`

Usually means:

* Invalid bot token

---

# Compatibility

* WooCommerce HPOS compatible
* Tested with WooCommerce 9+
* Compatible with most WordPress themes

---

# Plugin Structure

```text
woocommerce-telegram-order-notifier/
│
├── woocommerce-telegram-order-notifier.php
├── uninstall.php
└── README.md
```

---

# Future Improvements

* Multiple chat support
* Custom message templates
* Order status notifications
* Inline Telegram buttons
* Product image support

---

# License

GPL v2 or later

---

# Author

Store Tools

Built for WooCommerce store owners who want instant order alerts directly in Telegram.

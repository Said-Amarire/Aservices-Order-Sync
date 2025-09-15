# Aservices Order Sync

![Aservices Order Sync](https://via.placeholder.com/800x200.png?text=Aservices+Order+Sync)

**A powerful WooCommerce plugin to sync orders in real-time with Google Sheets, track customer device info, payment details, and AffiliateWP data, with a fully responsive dashboard.**

---

## 🌟 Features

- **Ultra-Fast Order Sync:** Instantly sends WooCommerce order data to Google Sheets after checkout.  
- **Device Detection:** Detects browser, operating system, and device type with accuracy.  
- **Customer Tracking:** Logs IP address, country, and browser languages.  
- **AffiliateWP Integration:** Captures affiliate ID, name, email, referral ID, and status.  
- **Order Details:** Saves product names, quantities, variations, fees, totals, and payment method.  
- **Non-Blocking Requests:** Optimized for ultra-fast checkout performance.  
- **Failed Queue Retry:** Automatically retries failed webhooks.  
- **REST API Endpoint:** Pull WooCommerce orders programmatically.  
- **Responsive Loader:** Fullscreen overlay with animated spinner during checkout.  
- **Customizable Dashboard:** Configure all settings from WordPress/WooCommerce admin.  

---

## 🛠 Installation

1. Download the plugin `.zip` file.  
2. Go to **WordPress Admin > Plugins > Add New > Upload Plugin**.  
3. Upload the file and click **Install Now**.  
4. Activate the plugin.  
5. Open **WooCommerce > Aservices Order Sync Settings** to configure your **Google Sheets Webhook URL**, **API Key**, and **API Secret**.  

---

## ⚙️ Configuration

- **Google Sheets Webhook URL:** Your Google Apps Script endpoint for order syncing.  
- **API Key & Secret:** Used to authenticate REST API requests.  
- **Retry Interval:** Automatic retry for failed webhooks (every 5 minutes).  
- **Device & UA Tracking:** Enabled by default for precise device/browser detection.  

---

## 🚀 Usage

- Orders are automatically pushed to Google Sheets after checkout or order status updates.  
- Failed webhooks are queued and retried automatically.  
- You can fetch order data through the REST API endpoint:

GET /wp-json/wc-gs/v1/orders
Headers:
X-WC-GS-KEY: your_api_key


## The plugin captures customer details, order items, fees, payment method, affiliate data, and device information.

🎨 Responsive Loader

Fullscreen overlay during checkout.

Modern animated spinner.

Works seamlessly across desktop, tablet, and mobile.

📄 Example Payload

{
  "orderId": 1234,
  "orderDate": "2025-09-15 12:00:00",
  "orderStatus": "processing",
  "customerName": "John Doe",
  "customerEmail": "john@example.com",
  "ipAddress": "123.456.78.9",
  "country": "Morocco",
  "browser": "Chrome",
  "platform": "Windows 10",
  "device": "Desktop",
  "language": "en-US",
  "product1_name": "Subscription Plan",
  "product1_variations": "1 Month",
  "product1_qty": 1,
  "paymentMethod": "Credit Card",
  "fee1_total": "0 USD",
  "productTotal": "25 USD",
  "orderTotal": "25 USD",
  "affiliateId": 1,
  "affiliateName": "Affiliate Example",
  "affiliateEmail": "affiliate@example.com",
  "referralId": 101,
  "referralStatus": "paid"
}

## 💡 Notes

Requires WooCommerce installed and active.

Supports AffiliateWP integration.

Caches geolocation data to reduce API calls.

Uses non-blocking HTTP requests for minimal checkout impact.

📝 Changelog

1.0.0 – Initial release with:

Google Sheets integration

Device detection

REST API endpoint

Responsive checkout loader

AffiliateWP support

Failed queue retry

⚖️ License

MIT License © 2025 Aservices

## 📞 Support

For help, bug reports, or feature requests:
Amarire Dev — mailto:contact@amarire.dev

# iRCTC_TheTechnicalServer Assistant

A local Manifest V3 Chrome extension that acts as a guided booking assistant for IRCTC, keeping all sensitive steps under strict manual control.

## Safety Boundary (Strict)
This extension **never** bypasses or automatically completes login, CAPTCHA, OTP, payment, or final booking submission. It acts as a state-driven assistant that prepares forms to save you time.
- Login, CAPTCHA solving, and OTP entry remain **entirely manual**.
- The extension **will not** automatically click "Continue", "Pay & Book", or "Confirm".
- Payment completion is **strictly manual**. The extension will only select your preferred payment method on the payment options page, and you must proceed manually.
- No personal passenger data, passwords, CAPTCHAs, OTPs, or payment information is ever transmitted off your machine. Data is stored safely in `chrome.storage.local`.

## Features
- **Guided Workflow**: Understands the page state (Search, Train Selection, Passenger Entry, Review, Payment) and prepares the necessary UI fields based on your configuration.
- **Journey Search Autofill**: Configure your From Station, To Station, Date, Travel Class, and preferred Train Number. The extension will automatically populate the IRCTC search fields and results page.
- **Passenger Autofill**: Locally store up to 6 general passengers (or 4 Tatkal passengers). The extension will instantly fill the passenger form when ready.
- **Payment Preparation**: Preselects BHIM/UPI/USSD and your specific provider on the final Payment Options page.
- **State Dashboard**: A collapsible, floating panel displaying the current booking stage, journey details, remaining passenger slots, and manual action required prompts.

## Install
1. Open `chrome://extensions` in Chrome or Edge.
2. Enable **Developer mode**.
3. Select **Load unpacked**.
4. Choose this extension folder.

## Configure and Use
1. Click the extension icon to open Settings.
2. Fill out your Journey Search parameters (Origin, Destination, Date, Train Number, Class).
3. Choose your Booking Type (General or Tatkal) and add your passenger details.
4. Open `irctc.co.in`.
5. Login manually. The extension will prepare your search form on the homepage. Click Search manually.
6. On the results page, the extension will locate your train and class. Click Book Now manually.
7. On the passenger details page, the extension will fill in the form. Click Continue manually.
8. Complete CAPTCHAs and OTPs manually as they appear. The extension will pause whenever they are present.
9. Verify the Review Journey page, then proceed manually.
10. On the Payment page, verify the prepared provider and complete your payment explicitly.

## Troubleshooting
- If a form does not fill properly or IRCTC changes a page, you can use the **Start**, **Pause**, or **Reset Session** controls in the floating panel.
- Use the **Settings** gear icon in the floating panel to quickly adjust passenger or payment settings mid-booking.

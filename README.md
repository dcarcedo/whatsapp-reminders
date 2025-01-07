# Appointment Automation System

A streamlined appointment management system built using **Google Sheets**, **Apps Script**, and **Twilio**. This project automates appointment scheduling, reminder messages, and confirmations via WhatsApp.

## Features

- Synchronizes available time slots with Google Calendar.
- Allows manual appointment creation via URL/Webapp.
- Sends automated WhatsApp reminders to clients.
- Supports appointment confirmation via a custom HTML-based bridge.

## How It Works

1. **Google Sheets**:
   - Manage patient data and available time slots.
   - Use dropdown menus for quick appointment creation.

2. **Google Apps Script**:
   - Automates calendar synchronization and appointment reminders.
   - Integrates with Twilio for WhatsApp messaging.
   - Edits Google Calendar event to reflect user confirmation

3. **Twilio**:
   - Sends personalized reminder messages to clients.
   - Example message:  
     ```
     Hola [Name], te envío recordatorio de la cita de mañana a las [Time] en [Location]. Por favor, confirma haciendo clic aquí: [confirmLink]
     ```

4. **HTML Bridge**:
   - Enables appointment confirmations via a secure link.
   

## Setup

### Prerequisites

- A Google account with access to Google Sheets and Calendar.
- A Twilio account with WhatsApp API enabled.
- Basic knowledge of Google Apps Script.

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/appointment-automation-system.git
   cd appointment-automation-system
2.    Set up Google Apps Script:
    Open Google Sheets.
    Navigate to Extensions → Apps Script and paste the code from src/appsscript/.

3. Configure Twilio:
    Add your Twilio credentials to the sendWhatsAppMessage function in src/twilio/twilio.js.

4. [Optional] Deploy the HTML Bridge:

    Host src/html-template.html on your WordPress site or any static hosting.

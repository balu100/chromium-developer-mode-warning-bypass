# Chromium-based Developer Mode Notification Bypass

This project provides a simple method to bypass the developer mode notification in Chromium-based browsers, specifically Microsoft Edge.

## How It Works

By editing the Preferences file of your Edge browser, you can prevent the developer mode notification from appearing.

## Instructions

1. **Locate the Preferences File:**
   
   Open the file located at:
   `C:\Users\Your_User\AppData\Local\Microsoft\Edge\User Data\Default\Preferences`

2. **Edit the Preferences File:**

   - Search for the following JSON entry:
     ```json
     {"allow_chrome_webstore": true}
     ```
   - If this entry is not present, add the following line:
     ```json
     "dev_mode_warning_snooze_end_time": "XXXXXXXXXXXXXXXXX",
     ```

3. **Set the Timestamp:**

   Replace `XXXXXXXXXXXXXXXXX` with a timestamp value. For example:
   ```json
   {"allow_chrome_webstore": true, "dev_mode_warning_snooze_end_time": "99999999999000000", "developer_mode": true}

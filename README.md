# 📌 Client Sign-In & Vendor Submission Automation Flow (n8n)

---

## 🟢 Node 1: Client Sign-In & Link Distribution
**Expected Output**
```json
{
  "client_username": "fintech_client_123",
  "form_link": "https://forms.gle/abc123?client=fintech_client_123"
}
```
## 🟢 Node 2: Vendor Submission (Google Form Trigger)
**Expected Output**
```json
{
  "client_username": "fintech_client_123",
  "vendor_name": "XYZ Traders",
  "form_responses": {
    "field1": "value",
    "field2": "value",
    "uploaded_files": [
      "file_id_1",
      "file_id_2"
    ]
  },
  "submission_timestamp": "2025-09-23T10:15:00Z"
}
```
## 🟢 Node 3: Google Sheets (Append Row)
**Expected Output**
```json
{
  "status": "success",
  "row_added": {
    "client_username": "fintech_client_123",
    "vendor_name": "XYZ Traders",
    "field1": "value",
    "field2": "value",
    "submission_timestamp": "2025-09-23T10:15:00Z"
  }
}
```
## 🟢 Node 4: Google Drive (File Upload)
**Expected Output**

## 🟢 Node 5: Email Notification
**Expected Output**
```json
{
  "status": "sent",
  "recipient": "client@email.com",
  "subject": "New Vendor Submission: XYZ Traders",
  "body": "A new vendor submission has been received and stored."
}
```

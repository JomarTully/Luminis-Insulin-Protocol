# Luminis Health insulin infusion calculator — clinical review draft

Open `index.html` in a browser. On GitHub Pages, upload all three files (`index.html`, `logic.js`, `app.js`) together into a dedicated `luminis-insulin/` folder. Link from a home page with `<a href="luminis-insulin/">Luminis Health insulin calculator</a>`. Do not replace the separate Johns Hopkins calculator.

Source: supplied PDF “Hyperglycemic Emergencies – Insulin Infusion Titration,” LH MED16.2.02 – Continuous Infusion of Regular Insulin Attachment 1 (PDF modified December 2024). The app covers initiation by actual weight and potassium, Table 1 and Table 2 adjustment by BG and one-hour trend, hold/restart instructions, high-rate notifications, and maximum 30 units/hr. It also offers a separately saved hourly event log and reports for the last 12, 24, or 48 hours, downloadable CSV, and print/PDF.

Review needed before bedside use: the printed headings overlap at exactly 60 kg and 100 kg (app chooses ≤60 and ≥100 respectively and flags them); text and table conflict at an exactly 150 mg/dL hourly drop (app flags it); Table 2 provides no rounding increment for the 0.05 units/kg/hr redose (app displays exact calculation to three decimals); and for a negative computed rate, the protocol instructs a hold then Table 2 reassessment but does not give a fixed restart rate (app does not invent one). The app requires a 60-minute interval to automate titration. Results must be checked against current institutional policy and orders. A calculated recommendation does not confirm an administered rate.

Events save only on explicit action in the current browser using local storage; no patient names or IDs should be entered. Export before clearing browser data, switching devices, or starting a new patient. This log is not an EHR record and has no access controls on shared devices.

Run pure-logic edge checks with `node test.js`.

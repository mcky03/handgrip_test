# handgrip_test
Handgrip strength_testing
Handgrip Strength Calculator (Web App)
A simple, browser‑based handgrip strength calculator built with HTML, CSS, and JavaScript.

Users can enter:

Date of test

Gender

Age range

Left handgrip strength (kg)

Right handgrip strength (kg)

The app compares the entered values with example reference ranges and shows whether each hand is below, within, or above the typical range for the selected gender and age group.

Note: The reference ranges in this demo are illustrative only and can be updated in the JavaScript code to match local or published reference values.

Features
Runs entirely in the browser (static HTML + CSS + JavaScript).

Mobile‑friendly layout suitable for quick use in clinical or workshop settings.

Displays:

Reference range for the selected gender and age range.

Status for each hand: below / within / above range.

A brief text summary.

Optional Print / Save as PDF button to allow users to keep a copy of their result.

Logs user submissions to an external form (e.g. Google Forms) for attendance and record‑keeping.

Data Logging and Privacy
This tool can be configured to send user inputs (e.g. date, gender, age range, left/right handgrip strength) to an external form service such as Google Forms for:

Attendance tracking

Simple usage statistics

Basic quality improvement analytics

A typical setup:

A hidden HTML form posts data to a Google Form in the background (e.g. via a hidden iframe).

The user stays on the calculator page and sees their results, while the submission is logged in the form’s response sheet.

Privacy note (generic):

No patient identifiers (e.g. name, ID number, phone, email) should be captured or transmitted by this tool.

Data should be used in an aggregated, non‑identifiable way for monitoring, audit, and service improvement.

Local teams are responsible for ensuring that use of this tool complies with applicable institutional and data protection policies.

Usage Instructions
Open the calculator in a web browser.

Enter:

Date of test

Gender

Age range

Left and right handgrip strength (in kg)

Click “Save my result & show results”:

Your entry is logged for attendance/record‑keeping (if configured).

The app calculates and displays:

Example reference range for your gender and age range

Whether each hand is below / within / above that range

A short textual summary

(Optional) Click Print / Save as PDF to keep a copy of the result.

Updating Reference Ranges
The handgrip reference ranges are defined in the JavaScript as a simple object, for example:

js
const referenceRanges = {
  Male: {
    "18-29": { min: 36, max: 56 },
    "30-39": { min: 34, max: 54 },
    // ...
  },
  Female: {
    "18-29": { min: 22, max: 36 },
    // ...
  }
};
To update:

Open index.html in a text editor.

Locate the referenceRanges object in the <script> section.

Replace the min and max values with your chosen reference data (e.g. from local guidelines or published normative studies).

Commit and push the changes to GitHub; the GitHub Pages site will update automatically.

Viewing the Project (GitHub Pages)
This project is intended to be hosted as a static site via GitHub Pages.

Typical setup:

Place the calculator code in index.html at the root of the repository.

In the repository settings, enable GitHub Pages:

Source: Deploy from a branch

Branch: main (or master)

Folder: / (root)

After deployment, access the app using:

text
https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/
Share this URL (or a QR code pointing to it) with clinical units or workshop participants for easy access.

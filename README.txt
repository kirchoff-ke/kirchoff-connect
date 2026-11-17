KIRCHHOFF CONNECT — OFFLINE CBE SCHOOL ANALYTICS
School: Kalokol Mixed Junior School
Platform: Windows + Android (installable web application / PWA)

WHAT IS INCLUDED IN THIS BUILD
- Dashboard
- Learner registration, editing, search and deletion
- Grades 7, 8 and 9
- Assessment entry for all nine learning areas
- Formative and summative assessment records
- Editable eight-level CBE rubric configuration
- Individual term report generation and A4 printing
- Grade-level analytics
- JSON backup and restore
- IndexedDB local browser database
- Service-worker offline caching and install manifest

IMPORTANT GRADING NOTE
The school-approved boundaries requested for ALL Grades 7, 8 and 9 are preconfigured:
EE1 90–100; EE2 75–89; ME1 58–74; ME2 41–57; AE1 31–40;
AE2 21–30; BE1 11–20; BE2 0–10.
The achievement point values are EE1=8, EE2=7, ME1=6, ME2=5,
AE1=4, AE2=3, BE1=2 and BE2=1. These ranges are based on the
user-supplied grading image with the requested changes to EE1 and BE2.
Confirm that this is the school's adopted rubric before operational use.

HOW TO RUN ON WINDOWS
1. Extract this ZIP file.
2. Install Visual Studio Code (or use another local web server).
3. Open the extracted folder in VS Code.
4. Install the Live Server extension.
5. Right-click index.html and choose "Open with Live Server".
6. In Chrome or Edge, use the install icon in the address bar / browser menu to install.
   Service workers and PWA installation require localhost or HTTPS; do not open file://.

HOW TO USE ON ANDROID
1. Put the project on a local or secure HTTPS web server, or serve it from a computer
   on the same Wi-Fi network for initial testing.
2. Open the app URL in Chrome on Android.
3. Choose browser menu > Add to Home screen / Install app.
4. Load it once while connected to the server so the offline cache is populated.
5. It can then open offline from its home-screen icon.

DATA AND MULTI-DEVICE LIMITATION
Records are stored locally in each browser/device using IndexedDB. Windows and Android do
not automatically share a database. Use Export backup on one device and Import backup on
the other to transfer a snapshot. Avoid editing both copies independently and importing
over newer data. A later controlled synchronization feature can be added if required.

PRIVACY
Use device passwords and keep backup files secure. This starter has no user login or
role-based permissions yet. Add authentication and access controls before sharing devices
or storing sensitive learner information in a production environment.

REPORT CARD UPDATE (v2)
-----------------------
The report card is now designed for A4 portrait printing with navy blue and green styling.
In School & Grading settings you can edit the school name, email, phone, postal address,
term opening and closing dates, class teacher name, head teacher name, and upload the
school logo, official stamp, and both signatures. Images are stored in this browser's
local IndexedDB settings and are included in JSON backups.

In Learner Reports, select a grade and learner to preview one report, or select a grade
and use Preview all reports in grade. Review the preview before choosing the print button.
For the best print result, choose A4 paper, Portrait orientation, and enable background
graphics in the browser print dialog. The app hides its navigation and controls when printing.

UPDATING AN EXISTING GITHUB PAGES INSTALLATION
----------------------------------------------
1. On the existing laptop/browser, use Backup to export a JSON backup before updating.
2. Extract this ZIP on the computer.
3. Upload/replace the files inside the KIRCHHOFF_CONNECT folder in the SAME GitHub repository
   and SAME published folder (usually the repository root). Keep the existing Pages URL.
4. Wait for GitHub Pages to finish deploying. Close old app tabs/windows, reopen the website,
   and refresh. The service worker cache has been upgraded to v2.
5. Existing learner and assessment records remain in that browser's local database because
   the database name and structure are unchanged. Still keep the JSON backup safely.
6. Settings and uploaded images are local to each device/browser. Configure them on each
   device or transfer them using Export Backup / Import Backup.

Privacy: do not place learner records, marks, signatures, school stamp images, or other
private data in the public GitHub repository. Upload only the application source files.

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
No score boundaries have been assumed. On the School & grading page, enter the official
school-approved minimum percentages for EE1, EE2, ME1, ME2, AE1, AE2, AE1, BE2 as provided
by your approved rubric. The app validates descending thresholds and requires BE2 to start
at 0%. If the school's approved rubric defines score bands differently, update the mapping
logic before operational use. Confirm the exact official boundaries with your school/MoE
guidance before entering real marks.

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

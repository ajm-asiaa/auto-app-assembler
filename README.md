# auto-app-assembler
These are the files required to run the Auto App Assembler (formally Electron Express) service for CARTA developers.

It can automatically create a Linux AppImage or a fully signed & notarized macOS Electron version (Intel or Apple Silicon) from any carta-frontend and carta-backend combination with the press of a button. 
This is useful for CARTA developers and the Science team to easily test new feature branches or bug fixes etc.

Originally it queried Github to get the list of all current carta-frontend and carta-backend branches. It could also sort by date, but in order to get timestamp information, 
many additional API requests need to be made. However, Github imposes a limit of 60 API requests per hour. 
Instead, we now use Github Webhooks to store any commits in a local list as soon as they are made.

Some additional files are required on the machines that build and package the carta-backend. They have not been uploaded yet.
If using NGINX and reverse proxy, it requires configuration blocks to be added to your NGINX configuration file.

To run:
```
npm install
npm start
```

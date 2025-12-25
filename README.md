# RemoteVNCBooking_Web

A web project for **Remote VNC machine booking and connection control**.  
It provides user sign-up/login, a machine list (with grouping and favorites), weekly time-slot booking and cancellation, and a protection mechanism that requires a **Connect Password** when connecting during a time slot booked by someone else.

## Feature Overview

- **Account System**
  - Sign Up (Name / WWID / Password / Connect Password)
  - Login (WWID / Password)
  - Remember me (auto-fill login info)
- **Machine List**
  - Grouped by SN prefix (e.g., `A_*` / `B_*` / `C_*`)
  - Shows machine state and whether it is currently busy / currently in use by the logged-in user
  - Favorites can pin machines for quick access
- **Booking System**
  - Weekly view (Sunday–Saturday)
  - AM / PM toggle (0–11 / 12–23)
  - Supports selecting multiple slots and clicking **Booking**, or selecting slots booked by the current user and clicking **Cancel**

- **Connection Protection**
  - The Connect action first checks whether the current time slot is booked
  - If the slot is booked by another user: a dialog is shown and **Connect Password** verification is required before connecting
  - If the slot is booked by the current user or unbooked: connect directly via the `vnc://` scheme

- **First-time Download**
  - The Sign Up dialog provides a download link to `AutoCreateVNC.zip`

## Tech Stack

- Frontend: HTML / CSS / Vanilla JavaScript  
- Backend: Node.js (Express)  
- Database: MySQL
- Password Hash: bcrypt

**Login page**
![Login](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p1.png)
**Sign up page**
![SignUp](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p2.png)
**Main page**
![Main](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p3.png)
**Select machine**
![Select_machine](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p4.png)
**Select machine (I already booking *Time_yellow*)**
![Select_machine](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p5.png)
**Select machine (Other user booking *Time_red*)**
![Select_machine](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p6.png)
**Other user booking by I want to connect**
![Select_machine](https://github.com/Blacktea945/RemoteVNCBooking_Web/blob/master/screenshots_p/pic_p7.png)



# Dark Souls Twitch Overlay

A Dark Souls–style Twitch overlay that displays cinematic **“YOU DIED”** messages on stream, triggered directly from Twitch chat.

The overlay connects anonymously to a Twitch channel using **tmi.js**, listens for the `!ds` command from authorized users, and shows a full-width animated banner with sound and visual effects.

---

## ✨ Features

- Dark Souls / Elden Ring inspired “YOU DIED” banner  
- Full-width cinematic black bar with blurred edges  
- Fade-in and fade-out animation  
- Plays custom `died.mp3` sound  
- Triggered from Twitch chat with `!ds <text>`  eg. !ds Skill issue
- Only **Sub, VIP, Moderator or Broadcaster** can trigger  
- 5-minute global cooldown  
- Works as an OBS Browser Source  
- Anonymous Twitch connection (no login required)

---

## 📥 Installation

### 1. Download the repository
Click **Code → Download ZIP** on GitHub  
Extract the files into any folder on your computer.
---

### 2. Set your Twitch channel
Open `index.html` in **Notepad** or any text editor.
Find this line:

```
const CHANNEL = "YA TWITCH HERE";
```
Change it to your Twitch channel name.
Save the file.

### 3. Add the overlay to OBS
Open OBS Studio
Click + → Browser Source
Enable Local File
Click Browse and select index.html
Enable:
Allow OBS to control audio
Refresh browser when scene becomes active
Click OK

--------------------------------------

Only the following roles can use the command:
Broadcaster
Moderator
VIP
Subscriber
The overlay will appear in the center of the screen and disappear automatically.

Cooldown
The command can be used once every 5 minutes globally to prevent spam.

### 🎨 Customization

In index.html you can edit:
Colors
Font size
Fade time
Cooldown
Sound file

Cooldown line:
```
const COOLDOWN = 5 * 60 * 1000;
```
### ⚔ Credits
Inspired by the Dark Souls UI by FromSoftware.
Powered by tmi.js.


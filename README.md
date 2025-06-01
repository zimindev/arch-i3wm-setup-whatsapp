# 💬 Install WhatsApp on Arch Linux

This guide shows how to install **WhatsApp** on Arch Linux using different methods, including a native wrapper and AUR packages. Works perfectly with tiling window managers like **i3wm**.

---

## ✅ Method 1: `whatsapp-for-linux` (Unofficial AUR Client)

This is a native-like WhatsApp Web wrapper with tray support.

### 🔧 Install with an AUR helper:

```bash
yay -S whatsapp-for-linux
````

Then launch with:

```bash
whatsapp-for-linux
```

---

## 🧰 Method 2: Create a Nativefier App (Custom Desktop Client)

Use `nativefier` to wrap WhatsApp Web in a native desktop app.

### 1. Install dependencies

```bash
sudo pacman -S npm
sudo npm install -g nativefier
```

### 2. Generate the app

```bash
nativefier -p linux -n "WhatsApp" "https://web.whatsapp.com/"
```

This creates a `WhatsApp-linux-x64` folder.

### 3. Move the app to `/opt`

```bash
sudo mv WhatsApp-linux-x64 /opt/whatsapp
```

### 4. Create a launcher symlink

```bash
sudo ln -s /opt/whatsapp/WhatsApp /usr/local/bin/whatsapp
```

Now you can launch it with:

```bash
whatsapp
```

---

## 🌐 Method 3: Use Web Version (Simple and Effective)

Just open in your browser:

```
https://web.whatsapp.com
```

You’ll need to scan the QR code using your phone.

---

## 🎛️ Optional: i3 Keybinding

Add this to your i3 config (`~/.config/i3/config`) for a shortcut:

```bash
bindsym $mod+w exec whatsapp
```

Reload i3 with:

```bash
Mod + Shift + R
```

---

## 🟢 Done!

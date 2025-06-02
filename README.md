# Mac-n-Cheese-SS (No Yahtzee's — just a screenshot utility for Macs/Unix-like systems)

A tasty macOS snipping tool that saves your screenshots, flavors your clipboard, and serves 'em hot. 🔪🧀📸

---

## ✨ Features

* 🖼️ Interactive screenshots (`screencapture -i`)
* 📋 Clipboard auto-copy
* 💾 Auto-save to your own cheese drawer (default: `~/Desktop/Screencaps/images`)
* 🔧 Headless background execution via LaunchAgent
* ⌨️ Global keyboard shortcuts:

  * `⌃S` (Control + S): Full-screen screenshot → clipboard + saved
  * `⌃⇧S` (Control + Shift + S): Interactive snip tool → clipboard + saved

---

## ⚙️ Install

### 🔄 One-liner setup:

```bash
curl -L -o install_ss_screenshot.sh https://raw.githubusercontent.com/YOUR_USERNAME/mac-n-cheese-ss/main/install_ss_screenshot.sh
chmod +x install_ss_screenshot.sh
./install_ss_screenshot.sh
```

---

## 🧠 What the install script does:

* Asks where to save your cheesy captures (default: `~/Desktop/Screencaps/images`)
* Lets you choose a filename style (timestamp, epoch, increment, or custom string)
* Sets up:

  * `~/bin/ss_clip_and_save.sh` — main snip script
  * `~/.ssconf/` — persistent config storage
  * `~/Library/LaunchAgents/com.gnotree.sscreenshot.plist` — background service
* **Creates Automator Quick Actions bound to:**

  * `⌃S`: Instant clipboard + save snip
  * `⌃⇧S`: Selection-based snip like `Win + Shift + S`

> You'll be cheesing your screen to the clipboard so fast, you'll forget what Print Screen ever was. It's like you're back on Windows 7 — but smoother, sharper, and full of Mac flavor.

> `⌃⇧S` is your new `Win + Shift + S`. Say cheese and snip with style. 😎🧀

---

## 🚀 Usage

After install, just hit your keys:

* `⌃S`: Screenshot entire screen to clipboard + file
* `⌃⇧S`: Select region to screenshot → clipboard + file

Or trigger manually anytime:

```bash
launchctl start com.gnotree.sscreenshot
```

Screenshots are saved and served hot into your specified cheese vault.

---

## 📁 File Layout

* `install_ss_screenshot.sh`: Setup & onboarding script
* `~/bin/ss_clip_and_save.sh`: Main script that does the work
* `~/.ssconf/`: Where config lives (directory + naming prefs)
* `~/Library/LaunchAgents/com.gnotree.sscreenshot.plist`: Headless background service

---

## 🧾 License

MIT License — snack freely, remix openly.

---

## 🧀 Author

Crafted with cheddar by [GT/gnotree/Hobie Brown/SpydersP(l)unk](https://github.com/gnotree)

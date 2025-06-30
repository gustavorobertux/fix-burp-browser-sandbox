# Fix Burp Browser Sandbox

This is a simple shell script to fix permission issues with the Burp Suite embedded Chromium-based browser on Linux systems.

If you see errors related to the browser not launching or crashing immediately, this script might help. It ensures the `chrome-sandbox` binary has the correct permissions (`setuid root`), which is required for the Chromium sandbox to work properly on Linux.

---

## 🔧 What it does

- Locates the `chrome-sandbox` binary under your home directory.
- Verifies if it has the correct `owner` (`root:root`) and permissions (`4755`).
- Applies the necessary changes only if required.
- Warns you to restart Burp Suite if it's already running.

---

## 📜 Usage

```bash
git clone https://github.com/gustavorobertux/fix-burp-browser-sandbox.git
cd fix-burp-browser-sandbox
chmod +x fix_burp_browser.sh
./fix_burp_browser.sh

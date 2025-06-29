# Dev Tip: Avoid Unnecessary CPU Usage

Developers sometimes face an issue where their laptop heats up or makes noise even after they have stopped active development. While it is normal for your machine to use high CPU during local development with servers (Next.js, React, Django, Express, etc.), if your laptop continues to heat up and make noise while idle, one common reason may be that you forgot to stop your local servers. Even if your laptop has good specs and you don’t notice, it may still be unnecessarily consuming CPU resources in the background.

### This can also happen if:
1️⃣ Your IDE (VS Code, IntelliJ, etc.) reopens previous projects and automatically restarts the dev server you had running before reboot.

2️⃣ You have startup scripts, daemons, or auto-start apps (e.g., Docker, background Node/Python services) that automatically launch on boot.

3️⃣ You have a misconfigured system service or a cron job triggering a heavy process on startup.

---

## To close processes that are consuming resources unnecessarily:

### For macOS Users:
✅ Open **Activity Monitor** (`Cmd + Space`, type “Activity Monitor”).  
✅ Go to the **CPU** tab and sort by **% CPU** to find heavy processes.  
✅ Select the process (e.g., `node`, `python`) → click ❌ → **Force Quit**.

---

### For Windows Users:
✅ Open **Task Manager** (`Ctrl + Shift + Esc`).  
✅ Go to the **Processes** tab and sort by **CPU**.  
✅ Right-click the high-CPU process (e.g., `node.exe`, `python.exe`) → **End Task**.

---

## Best Practice Reminder

✅ Always stop local servers with `Ctrl + C` when done.  
✅ Check your IDE settings to prevent auto-start of dev servers on reboot.

# [FIX] Kingdom Come: Deliverance II Controller Support (Linux Handhelds)

This guide fixes the non-responsive controller issue for handhelds like the **MSI Claw 8AI+**, **ROG Ally**, or **Legion Go** running Linux (Nobara/SteamOS).

### 1. Steam & System Settings
* **Steam Input:** Set to **"Disable Steam Input"** (Right-click game > Properties > Controller).
* **Launch Options:** Add `SteamDeck=1 %command%` (Properties > General).
* **Proton:** Use **"Proton Experimental"**.
* **Driver:** **Handheld Daemon (HHD)** highly recommended.

### 2. Manual Configuration Fix
1. Locate your game's profile folder. **Note:** Paths vary depending on your Steam library location and username. It usually looks like this:
   `.../Steam/steamapps/compatdata/1771300/pfx/drive_c/users/steamuser/Saved Games/kingdomcome2/profiles/default/`
2. Open **`attributes.xml`** (Must be lowercase).
3. Replace the entire content of that file with the code from the `attributes.xml` provided in this repository.

### 3. Optional: Write Protection (Terminal)
If the game keeps resetting your settings, you can manually lock the file. Replace `[YOUR_PATH_TO_FILE]` with the actual path found in Step 2:

* **To LOCK (Activate protection):**
  `chmod 444 "/[YOUR_PATH_TO_FILE]/attributes.xml"`
* **To UNLOCK (To change graphics settings):**
  `chmod 644 "/[YOUR_PATH_TO_FILE]/attributes.xml"`

---
*Jesus Christ be praised!*

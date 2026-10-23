# Rake Risk Format Generator

Windows desktop tool that turns eT-RR PDFs into the Rake Risk Excel workbook (with its linked Summary sheet) for **Paradip (TSLJ @ KICT)** and **Dhamra (All Plants)**.

This repository is the **official download and update channel**. It contains release files only, no source code.

> A paid subscription is required to use the program. Downloading it does not activate it. You sign in with the email and password supplied to you.

---

## Download and install

1. Open the [**Releases**](../../releases/latest) page and download `RakeRisk_Update_vX.Y.zip` from **Assets**.
2. Right-click the ZIP and choose **Extract All…**. Extract it to a folder you can write to, for example `Documents\RakeRisk` or `Desktop\RakeRisk`.
   Do not use `C:\Program Files`, because the program cannot update itself there.
3. Open the extracted folder and double-click **RakeRiskGenerator.exe**.
4. Sign in with your account.
5. On the first run on a computer, choose where the generated Excel files should be saved. The suggested folder is inside the program folder.

The `Templates` folder must stay next to the EXE.

### Windows says "Windows protected your PC"

The program is not code-signed, so Windows SmartScreen shows this on the first run. Click **More info**, then **Run anyway**.

---

## Using the program

1. Choose the **location** (Paradip or Dhamra).
2. Click **Add PDFs…** and pick your eT-RR files. The counter shows how many PDFs are loaded. Large batches are shown in columns, and you can maximise the window to see more at once.
3. Check the output folder, then click **Convert**.

The bar at the top of the window shows who is signed in, when the subscription ends, and the **Sign out** button.

---

## Updates

You do not need to come back to this page to update. When a new version is published, the program offers it the next time you open it:

- **Update available**: you can install it now or later.
- **Update required**: the update installs straight away and the program will not open without it.

The update downloads with a progress bar, closes the program, replaces the program files and templates, and starts the new version by itself. Your settings and output folder are kept. Updates are checked against a security checksum before they are installed.

---

## Subscription and sign-in

- The program checks your subscription each time it opens, and again every few hours while it stays open.
- It keeps working for up to **3 days without internet**. After that, connect once to verify.
- Each account is tied to **one PC**. To move to another computer, ask for the PC to be reset.

| Message you see | What to do |
|---|---|
| Wrong email or password | Re-enter it. Use the password reset email if you forgot it. |
| Your subscription ended | Contact the administrator to renew. |
| Registered to a different PC | Ask the administrator to reset your PC. |
| An internet connection is needed | Connect to the internet and open the program again. |
| This account has been blocked / No subscription is set up | Contact the administrator. |
| Update failed: checksum mismatch | Do not install it. Tell the administrator. |

---

## For the administrator: publishing a release

1. Build the program, then run `make_update_package.bat`. It creates `RakeRisk_Update_vX.Y.zip` and prints a **SHA-256** checksum.
2. Create a new release here with the tag `vX.Y`, and attach that ZIP.
3. In the Admin panel, open **Updates** and enter the version, the ZIP's download link, the checksum and the release notes, then publish.

Never rename or delete a published ZIP while any customer might still be on the old version. Changing a file after publishing also changes its checksum, so update the checksum in the Admin panel as well.

---

## Support

Contact the administrator who issued your account.

© All rights reserved. This software is provided to subscribed users only and may not be redistributed.

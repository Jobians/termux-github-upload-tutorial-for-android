## How to Upload a Folder to Your GitHub Repository on Android Using Termux

### Recommended Apps to Download:

* [**Termux**](https://f-droid.org/en/packages/com.termux/)
* [**Material Files**](https://play.google.com/store/apps/details?id=me.zhanghai.android.files) (for easy access to copy file paths)

---

### Step-by-Step Instructions:

1. **Grant Storage Access to Termux**

   Before anything else, run the following command in Termux to allow it to access your device’s storage:

   ```
   termux-setup-storage
   ```

   Confirm the storage permission prompt.

---

2. **Install Git and GitHub CLI**

   ```
   pkg install git gh
   ```

---

3. **Log in to GitHub**

   ```
   gh auth login
   ```

   Follow the on-screen prompts. If you have 2FA enabled, enter your verification code when asked.

---

4. **Navigate to Your Folder**

   Use the `cd` command to move into the folder you want to upload:

   ```
   cd /path/to/folder
   ```

   *(Tip: Use Material Files to get the exact folder path.)*

---

5. **Initialize a Git Repository**

   ```
   git init
   ```

---

6. **Add Files to the Repository**

   ```
   git add .
   ```

---

7. **Commit the Changes**

   ```
   git commit -m "Initial commit"
   ```

   *(You can replace `"Initial commit"` with any custom message.)*

---

8. **Create or Use a GitHub Repository**

   Go to GitHub and create a new repository, or use an existing one.

---

9. **Set the Remote Repository**

   Copy the **HTTPS** or **SSH** URL of your GitHub repo, then run:

   ```
   git remote add origin <YOUR-REPO-URL>
   ```

   Replace `<YOUR-REPO-URL>` with your actual repo URL.

---

10. **Push Your Files to GitHub**

```
git push -u origin main
```

**If you get this error:**

```
error: src refspec main does not match any
```

Run this command first:

```
git checkout -b main
```

Then push again.

---

### You're Done!

Your folder and its contents should now be uploaded to your GitHub repository. Check GitHub via your browser to confirm.

---

**If this tutorial helped you, check out the [video tutorial](https://youtu.be/TvoCGz1MWdQ) for a step-by-step walkthrough.**
And consider subscribing to my [YouTube channel](https://youtube.com/@jobianstechie) — I post helpful tech content regularly. Thanks for your support!

## Support

If you find my work helpful, you can support me by donating:

[![Donate](https://img.shields.io/badge/Donate-Crypto-0070BA.svg)](https://cwallet.com/t/TE6A6KMV)

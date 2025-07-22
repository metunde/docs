---
title: "The Easiest Way to Reset a Forgotten Windows Password (No Third-Party Tools Needed)"
datePublished: Tue Jul 22 2025 15:04:52 GMT+0000 (Coordinated Universal Time)
cuid: cmdeo1lt2000s02jy8vr7hw5h
slug: the-easiest-way-to-reset-a-forgotten-windows-password-no-third-party-tools-needed
tags: windows-password-reset-windows-tips-pc-troubleshooting

---

---

I recently started at a new workplace and was handed a company PC. I met two user accounts on it:

* One account **had no password**.
    
* The second account was **password-protected**, but the staff who previously used it does not remember the password.
    

At first, I considered **reinstalling the operating system** to start fresh, but that meant backing up all company data, saving credentials, and then restoring everything afterward, but that would take more time than I wanted.

Another idea was to **delete the locked account**, but I had no way of knowing if it contained important files. Deleting valuable data was a risk I wasn’t willing to take.

So, I decided to **reset the password** of the locked account. After a few minutes of Googling and *ChatGPTing*, I found a quick solution that worked perfectly. Here’s how I did it:

---

**Steps to Reset the Password**

**Step 1:**

1. Press **Windows + R**,
    
2. Type “**control userpasswords2**” and press **Enter**.
    

---

**Step 2:**

A **User Accounts** window will appear.  
Select the locked account.

---

**Step 3 (Important Note):**

After step 1, check the group bar in front of the current user; it must belong to the **Administrator** group for the guaranteed success of this method.

---

**Step 4:**

Click **Reset Password**, enter a **new password** (or leave it blank for no password), and click **OK**.

Now, you can log into the previously locked account using the new password.

---

**If You Want to Delete the Locked Account Instead**

If you’re sure the account has no important files, you can delete it in just four steps:

1. Go to **Settings &gt; Accounts &gt; Family & other users**.
    
2. Under **Other users**, find the account you want to remove.
    
3. Click it, then choose **Remove**.
    
4. Confirm deletion (this will **delete all files associated** with that account).
    

---

The locked account turned out to have **zero data**, and the entire process took me less than **10 minutes**. It was an easy task, and I have another handy Windows trick in my bag.

Watch out for my next article cos I am definitely trying the scenario where I can’t access any account, using a VM.  
If you forgot the password to your Linux machine, I already published an article about that [here](https://hashnode.com/post/cmbjqav35000b09kq8yf4940t).
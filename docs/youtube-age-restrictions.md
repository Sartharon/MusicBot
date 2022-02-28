---
title: Youtube age restriction
description: "Instructions for how to allow the playback of age restricted Youtube videos"
---
The following steps is optional and works in Chrome and Microsoft Edge:
1. Navigate to [Youtube](https://youtube.com) and log in with your account.

2. Open the developer console and switch to the network tab by pressing `CTRL + Shift + I`.  
![Developer console - Network Tab](/assets/images/dev-Net.png)

3. Play an age restricted Youtube video (like [this](https://www.youtube.com/watch?v=B3eAMGXFw1o)) while the network tab is open. You will see the network tab will fill with entries.  
![Network Tab - filling with entries](/assets/images/age-restriction/dev-Net-filling.png)

4. Scroll down in the list, search for and select one of the following entries:
* *player?*
* *next?*
* *browse?*
* *log_event?*
![Network Tab - correct entry](/assets/images/age-restriction/dev-Entry.png)

5. On the right side scroll down to **Request Header** and search for **cookie:**. Select a different entry shown in step 4 if **cookie:** is not present. Right click on cookie and copy it and paste it in a text editor of your choice.
![Entry - Request Header](/assets/images/age-restriction/dev-Entry.png)
![Entry - Request Cookie](/assets/images/age-restriction/dev-Cookie.png)

6. Search for **__Secure-3PAPISID=** in the text and copy the token to the **PAPISID =** setting in your bots *config.txt*.
![PAPISID](/assets/images/age-restriction/PAPISID.png)

7. Search for **__Secure-3PSID=** in the text and copy the token to the **PSID =** setting in your bots *config.txt*.
![PSID](/assets/images/age-restriction/PSID.png)

8. Restart your bot after adding those keys to your bots' config.txt



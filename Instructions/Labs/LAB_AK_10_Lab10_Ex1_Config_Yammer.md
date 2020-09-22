# Module 10 - Lab 10 - Exercise 1 - Configuring Yammer Enterprise

Because Yammer Enterprise brings the rich social experiences of Yammer to Microsoft Teams, SharePoint Online, and other Microsoft 365 apps, Holly Dickson is interested in implementing Microsoft Yammer in Adatum's Microsoft 365 pilot project. This will enable Adatum users to share, create, and edit files directly from Yammer conversations with Office for the web.

In this exercise Holly will configure the Yammer organizational settings for Adatum. She will also configure Yammer to enforce Microsoft 365 identity, which enables single sign-on (SSO) capabilities in Yammer. Holly will complete her Yammer preparation by configuring the Yammer user experience. 

### Task 1 - Configure a Yammer organization setting

1. On **LON-CL1**, you should still be logged in as the **Administrator** with a password of **Pa55w.rd**.

2. At the end of the prior lab, you were instructed to sign out of Microsoft 365 as Holly Dickson and close your Microsoft Edge browsing session. If you did not do it, then please do so now. This will enable you to start with a fresh browsing session. <br/>

	With Edge closed, select the **Edge** icon on the taskbar to open a new session. 

3. In Edge, enter the following URL in the address bar: **https://portal.office.com**.

4. In the **Pick an account** window, select Holly Dickson's account (**Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant ID provided by your lab hosting provider)). In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

5. On the **Stay signed in?** window, select **Don't show this again** and then select **Yes**.

6. On the **Microsoft Office Home** page, select **Yammer**.

7. On the **Yammer** home page, on the right-side of the title bar at the top of the page, select the **gear (Settings)** icon.

8. In the **Settings** pane that appears, under the **Yammer** section, select **Edit network admin settings**. This opens the **Yammer admin center**.

9. In the **Yammer admin center**, in the left-hand navigation pane, under the **Network** group, select **Usage Policy**.

10. In the **Usage Policy** window, update the following settings: <br/>

	- Select the **Require users to accept policy during sign up and after any changes are made to the policy** check box.
	- Select the **Display policy reminder in sidebar** check box.
	- In the **Custom Policy Title** field, enter**M365x Acceptable Use Policy**.
	- In the **Enter your policy in the textbox below** field, copy and paste in the following text: **Welcome to Yammer! Our goal is to provide a collaborative environment to connect with colleagues and bridge various departments and geographic locations to share meaningful information.**

11. Select **Save**.

12. In the **M365x Acceptable Use Policy** window that appears, select **I Accept**. 

13. In the **Welcome to the new Yammer!** window, select the X in the upper right corner to close it.

14. On the **Yammer** home page, on the right-side of the title bar at the top of the page, select the **gear (Settings)** icon.

15. In the **Settings** pane that appears, under the **Yammer** section, select **Edit network admin settings**. This opens the **Yammer admin center**.

16. In the **Yammer admin center**, in the left-hand navigation pane, under the **Network** group, select **Configuration**.

17. On the **Configuration** page, in the **Email Settings** section, select the **Require all users in your network to confirm their messages posted via email before posting** check box.

18. In the **Enabled Features** section, remove the check mark from **3rd Party Applications** to disable this feature.

19. Select **Save**.

20. In the **Yammer admin center**, in the left-hand navigation pane, under the **Content and Security** group, select **Data Retention**.

21. In the **Data Retention Policy** page, read the description of available options and select **Archive** (if it's not already selected) and then Select **Save**.

22. In the **Yammer admin center**, in the left-hand navigation pane, under the **Content and Security** group, select **Monitor Keywords**.

23. In the **Monitor Keywords** page, enter **admin@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant ID provided by your lab hosting provider) in the **Email Address** field.

24. In the text box below the **Email Address**  field, enter the following words, one in each line: **gambling**, **erotic**, **warez**.

25. Select **Save**. 

26. In the **Yammer admin center**, in the left-hand navigation pane, under the **Content and Security** section, select **Security Settings**.

27. Under the **Office 365 Identity Enforcement** section, select the **Enforce Microsoft 365  identity** check box and then select **Save**.

28. In your Edge browser, close the **Yammer admin center** tab and proceed to the next task.


### Task 2 - Configure the Yammer user experience

1. On **LON-CL1**, you should still be logged in as the **Administrator** with a password of **Pa55w.rd**.

2. At the end of the prior task, you were instructed to close the **Yammer admin center** tab. If you did not do it, then please do so now. 

3. In your Edge browser, on the **Microsoft Office Home** page, select **Yammer**.

4. On the **Yammer** home page, on the right-side of the title bar at the top of the page, select the **gear (Settings)** icon.

5. In the **Settings** pane that appears, under the **Yammer** section, select **Edit settings**. This opens the **Account Settings** page.

6. the **Account Settings** page, select the **Notifications** tab at the top of the page.

7. In the list of notifications, select only the following options in the **Email me when...** section (unselect all the rest):

- **I receive a message in my inbox**

- **I log in from somewhere new**

- **I post a message via email (This will send a confirmation email)**

8. Select **Save**.

9. Leave your Edge browsing session open, but close the **Yammer: Notifications** tab and proceed to the next task.


### Task 3 - Using Yammer

1. Switch to **LON-CL2**. The last time you used LON-CL2, you were logged into Outlook on the web as the MOD Administrator. You were then instructed to log out of Outlook and close your Edge browsing session at the end of the lab. If your Edge browser is still open, then close it now. 

2. Select the **Microsoft Edge** icon on the taskbar to open a new Edge browsing session, and then enter the following URL in the address bar: **https://portal.office.com**.

2. In the **Pick an account** window, if  Holly Dickson's **Holly@M365xZZZZZZ.onmicrosoft.com** account appears in the list, then select it now; otherwise, select **Use another account** and then sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant ID provided by your lab hosting provider) with a password of **Pa55w.rd**.

3. On the **Microsoft Office Home** page, select **Yammer**.

4. At the **WHO DO YOU WORK WITH** prompt, type **Christie** in the first text box, and then Select **DONE** and close the window.

5. Select **I Accept** at the **M365x Acceptable Use Policy** prompt.

6. Find the post from MOD Administrator in the post list.

7. Select **Like**, and then Select **SHARE**.

8. In the **Share This Conversation** dialog box, select **Post in a Group**, type **All Company** in the drop-down box, and then in the text box, type **Welcome from me too**.

9. Select **Share**.

10. Select **All Company** and in the **What are you working on** text box, type “**free gambling here”**, and then Select **Post**.

11. Log out of Microsoft 365 as Holly, close all browser tabs other than the **Sign out** tab, and then close Microsoft Edge.

12. Open Microsoft Edge and browse to **https://portal.office.com**. This time, log in as the MOD Administrator account (**Admin@M365xZZZZZZ.onmicrosoft.com**, where ZZZZZZ in the tenant ID provided by your lab hosting provider)

14. In the **Microsoft Office Home** page, select **Outlook**.

15. Verify the MOD Administrator received a message from Yammer with a report about a monitored keyword appearance in Beth’s post.

16. On the **Microsoft Office Home** page, select the user icon (the circle with MOD Administrator's **MA** initials) in the upper right-hand corner, and in the **My account** window that appears, select **Sign out**. Once you are signed out, close all other tabs, and then close Microsoft Edge.  



**Results**: After completing this exercise, you should have enabled Yammer Enterprise for A. Datum Corporation.

# Proceed to Lab 10 - Exercise 2
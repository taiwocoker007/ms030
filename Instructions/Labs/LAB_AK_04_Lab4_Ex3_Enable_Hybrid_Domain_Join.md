# Module 4 - Lab 4 - Exercise 3 - Enable Hybrid Domain Join

In this exercise, you will run Azure AD Connect to configure Hybrid Azure AD join. Hybrid Azure AD join enables automatic account configuration and Signle-Sign-On to cloud services for devices joined to Adatum's on-premises Active Directory. You will verify the device sync and verify the Hybrid Azure AD Join on LON-CL1 by using dsregcmd and the Windows 10 Mail app.

### Task 1 - Configure Hybrid Azure AD join

In this task, you will run the Azure AD Connect setup wizard to enable Hybrid Azure AD join of devices joined to Adatum’s on-premises Active Directory. 

‎1. You should still be logged into **LON-DC1** as the **Administrator** from the prior task.

2. Start **Azure AD Connect** by double-clicking the icon on the Desktop.

3. In **Microsoft Azure Active Directory Connect**, click **Configure**.

4. In **Additional tasks**, select **Configure device options**, and then select **Next**.

5. In **Overview**, select **Next**.

6. In **Connect to Azure AD** window, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where zzzzzz is the tenant ID provided by your lab hosting provider) in the **USERNAME** field, enter **Pa55w.rd** in the **PASSWORD** field, and then select **Next**. 

7. In **Device options**, select **Configure Hybrid Azure AD join**, and then select **Next**.

8. In **Device operating systems**, select **Windows 10 or later domain-joined devices**, and then select **Next**.

9. In SCP configuration, select **Adatum.com**, under **Authentication Service** select **Azure Active Directory**, and select **Add**.

10. In the **Enterprise Admin Credentials** window, enter **adatum\Administrator** in the **USERNAME** field, enter **Pa55w.rd** in the **PASSWORD** field, and then select **OK**. 

11. Back in **SCP configuration**, select **Next**.

12. **In Ready to configure**, select **Configure**.

13. In **Configuration complete**, select **Exit**.

14. Switch to **LON-CL1**.

15. On the log-in screen, you log in as **Beth@xxxUPNxxx.xxxCustomDomainxxx.xxx** (where xxxUPNxxx was the unique UPN name assigned to your tenant, and xxxCustomDomainxxx.xxx was the name your lab hosting provider assigned to the custom domain) account with a password of **Pa55w.rd**.

### Task 2 - Assign licenses

In this task, you assign product licenses to a synced user.

‎1. Switch to **LON-DC1** and log in as **Administrator** with a password of **Pa55w.rd**.

2. After finishing the previous lab exercise, you should still be logged into Microsoft 365 in your Edge browser as Holly Dickson.  

3. In your **Edge** browser, select the **Microsoft 365 admin center** tab, and then in the left-hand navigation pane, select **Users**, and then select **Active Users**. <br/>

4. In **Active users**, in **Search** enter **holly** and press Enter.

5. Select **Holly Dickson**.

6. In the menu bar above the list of users, select **Manage product licenses**. If you do not see this button, select the **ellipsis** icon (**More actions**). In the drop-down menu that appears, select **Manage product liceneses**.

7. In the **Licenses and apps** pane that appears for Holly Dickson, clear the checkbox next to **Office 365 E5**, and click **Save changes**.

8. In **Search** enter **beth** and press Enter.

9. Select **Beth Burke**.

10. In the menu bar above the list of users, select **Manage product licenses**. If you do not see this button, select the **ellipsis** icon (**More actions**). In the drop-down menu that appears, select **Manage product liceneses**.

11. In the **Licenses and apps** pane that appears for Beth Burke, select **Office 365 E5** and **Enterprise Mobility + Security E5**, and click **Save changes**.


### Task 3 - Verify device sync

In this task, you will start another sync cycle and verify, that computer accounts from Adatum's on-premises Active Directory are synced as devices to Azure Active Directory.

1. You should still be logged into **LON-DC1** as the **Administrator** from the prior task.

2. After finishing the previous exercise, you should still be logged into Microsoft 365 in your Edge browser as Holly Dickson.

5. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **...Show all** to display all the navigation menu options.

6. In the left-hand navigation pane, under **Admin centers**, select **Azure Active Directory**.

7. In the **Azure Active Directory admin center**, in the left-hand navigation pane, select **Azure Active Directory**.

8. In the **Azure Active Directory** blade for Adatum Corporation, under **Manage**, select **Devices**.

9. In the **Devices | All devices** blade, look for **LON-CL1**. If you do not see the device, wait a few minutes, and above the list of devices, click **Refresh** until you see **LON-CL1**.



### Task 4 - Verify the Hybrid Azure AD Join

In this task, you will verify the Hybrid Azure AD Join by running the dsregcmd command. Moreover, you will verify Single-Sign-On and automatic account configuration in the Windows 10 Mail app.

1. Switch to **LON-CL1**.

2. On the log-in screen, you log in as **Beth@xxxUPNxxx.xxxCustomDomainxxx.xxx** (where xxxUPNxxx was the unique UPN name assigned to your tenant, and xxxCustomDomainxxx.xxx was the name your lab hosting provider assigned to the custom domain) account with a password of **Pa55w.rd**.

3. Sign out as Beth.

4. On the log-in screen, you log in as **Beth@xxxUPNxxx.xxxCustomDomainxxx.xxx** (where xxxUPNxxx was the unique UPN name assigned to your tenant, and xxxCustomDomainxxx.xxx was the name your lab hosting provider assigned to the custom domain) account with a password of **Pa55w.rd**.


5. Right-click the **Windows (Start) icon** in the lower left corner of the taskbar, and select **Command Prompt**.

6. Type
   ```
   dsregcmd /status
   ```
   and press Enter.

7. In the output, beside **AzureADJoined** you should see **YES**. If not, wait a few moments and try again.

8. Close **Command Prompt**.

9. Select the **Windows (Start)** icon in the lower left corner of the taskbar, and select **Settings**.

10. In **Windows Settings**, select **Accounts**.

11. Select **Email & app accounts**. You should see Beth's Work or school account.

12. Close **Settings**.

13. Select the **Windows (Start)** icon in the lower left corner of the taskbar, and select **Mail**.

14. In **Mail**, click **Get started**.

15. In **Accounts**, click **Add account**.

16. Beth's work or school account should be offered at the top of the list. Select it.

17. The account should be configured automatically without any intervention. When the **All done!** message appears, click **Done**.

18. Back in **Accounts**, click **Ready to go**.

	**Note:** Syncing might not work yet, because the mailbox was not created. If Beth receives the first mail, syncing should work.

19. Select the **Windows (Start)** icon in the lower left corner of the taskbar, select **Administrator**, and select **Sign out**.

# End of Lab 4
 
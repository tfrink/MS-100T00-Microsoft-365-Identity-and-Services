# Module 4 - Lab 3 - Exercise 1 - Review Key Features of Exchange Online

Holly Dickson is Adatum’s Enterprise Administrator. She has recently deployed Microsoft 365 in a virtualized lab environment. Now that she has a tenant account set up and has been assigned to the Global Administrator role, she has been asked to review the key administrative functions within Exchange Online, SharePoint Online, and Teams so that she becomes familiar with their functionality and can offer guidance to her IT team on how they can be used throughout Adatum.

With regard to Microsoft Exchange, Adatum’s CTO has requested that Holly review some of the basic administrative functions in Exchange Online related to mail flow and recipient management. Since the Global Administrator role includes the Exchange Administrator role, Holly can perform all Exchange-related tasks.

### Task 1 – Manage Recipients

As you continue in your role as Holly Dickson, you are ready to review the steps involved in creating and managing mail flow recipients.

1. At the end of the previous lab, you were on LON-CL1, where you took on the role of Laura Atkins and installed Microsoft 365 Apps for enterprise. For this lab exercise, you must switch back to LON-DC1, where you will resume your pilot project in the role of Holly Dickson. <br/>

	Switch to **LON-DC1**, where you should still be logged in as the **Administrator** with a password of **Pa55w.rd**; if not, then do so now.

2. You should still have an Edge browser session and the Microsoft 365 admin center open from the prior lab. If so, proceed to the next step; otherwise, open Microsoft Edge, navigate to **https://portal.office.com/**, log in as **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider) and **Pa55w.rd**, and then in the **Microsoft Office Home** page, select **Admin** to open the Microsoft 365 admin center.

3. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Show all** (if necessary), then scroll down to **Admin centers** and select **Exchange**. This will open the **Exchange admin center** in a new tab. This is the Exchange admin center for Microsoft Exchange Online. 

4. In the **Exchange admin center**, select **Recipients** in the left-hand navigation pane to expand the Recipients group.

5. In the **Recipients** group in the left-hand navigation pane, select **Mailboxes**. The mailboxes that appear in this view include all the user accounts that were pre-created in your tenant by the lab hosting provider, along with the mailboxes for Holly Dickson and Laura Atkins that were created when you added their Microsoft 365 user accounts in the prior lab. <br/>

	Select the mailbox for **Joni Sherman** by clicking on her **DISPLAY NAME.** This will open the **User Mailbox** window with Joni’s data prefilled. By default, the window displays the **Mailbox** tab (the tabs appear at the top under Joni's name).

6.  At the bottom of the **Mailbox** tab, Under more **More options** select **Custom attributes**.

7. This opens the **Custom attributes** window for Joni. You can enter up to 15 attributes. You will not be entering any attributes in this lab exercise, but it’s important that you know this feature is available. Select **Cancel**.   <br/>

	‎**Note:** Custom attributes are properties your company can use for specific mailbox identification, such as a cost center number for the mailbox or other information such as an HR personnel number.

8. In addition to the **Mailbox** tab, there is the **Account** tab which combined includes several other sections that enable you to enter additional information pertaining to this specific mailbox. While you will not enter any of this optional information for the purposes of this lab, take a few minutes now and select the following tabs to see what additional information can be captured: 

	- **contact information.** This tab enables you to add personal information such as Street, City or Mobile number for the user.

	- **organization.** This tab enables you to add company-specific information such as Title or Department for the user.

9. Select the **Mailbox** tab again, then select **Manage mailbox delegation.** This enables the admin to assign a user to this mailbox’s Send As, Send on Behalf permissions, or Read and manage. This option is commonly used if you want another user to be able to send messages from this mailbox.

10. While in the **Manage mailbox delegation** window and select **Edit** to the right of **Read and manage** 

11. In the **Manage Mailbox deligation** window, select **+ Add permissions**. 

12. In the search bar, type in **Holly Dickson**.  In the list of user accounts that appears, select **Holly Dickson** and then select the **Save** button. Select **Close** and then select **cancel** twice.  <br/>

	‎**Note:** It may take about an hour for permission changes to propagate through the Microsoft 365 tenant. At that time, Holly Dickson will be able to access Joni’s mailbox without needing a password.

13. On Joni Sherman's **Mailbox** window, select the **X** in the top right-hand corner of the pane to close it.

14. Leave your browser and all the tabs open for the next task.

 
### Task 2 – Manage Groups 

In this task you will create two types of groups within Exchange Online: 

- The first group will be a distribution list of email recipients within the Sales department. Distribution lists are used to create a one-stop email list for contacting users simultaneously rather than having to email each recipient individually. Holly Dickson and Alex Wilber will be owners of the group, and you will assign Allan Deyoung, Diego Siciliani, and Lynne Robbins as group members.

- The second type of group that you will create is a dynamic distribution list. This group will contain the members of Adatum's new Dynamics CRM project team. Holly Dickson will be the group owner, and Nestor Wilke will be assigned as a group member.

1. Your browser should still be open to the **Exchange admin center** from the prior task, and it should still be displaying the expanded **Recipients** group in the left-hand navigation pane. In the prior task, you worked with user accounts using the **Mailboxes** option under the Recipients group. In this task, you will be creating groups, so select the **Groups** option in the **Recipients** group.  <br/>

	**Note:** You should already see the **Inside Sales** group that you created in Lab 2. This is a Microsoft 365 group whose email address is associated with the custom, on-premises domain (@xxxUPNxxx.xxxCustomDomainxxx.xxx). In the following steps, you will create a Distribution list group and a Microsoft 365 group whose email addresses will be in Microsoft 365 (@xxxxxZZZZZZ.onmicrosoft.com). 

2. You will begin by adding a distribution list of email recipients within the Sales department. Select the **Add a  group** button under the Microsoft 365 tab.

3. In the **Choose a group type** window that appears, select **Distribution** and then select **Next**.

4. In the **Set up the Basics** tab, add the group name of **Sales Department** next to **Name**, leave the description blank, and then select **Next**.

5. In the **Edit settings** tab, enter the following information and then select **Next**:	

	- Email Address: Type in  **SalesDept**. In the domain field to the right of it, select the drop-down arrow and select **xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider).

	- Joining the Group: Select **Owner Approval** This option allows the owner to control who can join the group.
	
	- Leaving the Group: Select **Closed**. This option enables the owner to control who can leave the group. Together with the prior **Joining the Group** option, you can control who joins or leaves your distribution group. </br></br>
**Tip:** In a real-world scenario, if your organization wants less administration, then leave the Joining and Leaving group options set to **Open**. 

6. In the next section, select **Create group** and then select **Close**.

7. Wait until you see your group name under the **Distribution list** tab. If you don't see it, refresh the tab every few minutes.

8. Once you see your new **Sales Department** group, select directly on the group name and then select the **Members** tab.

9. On the **Members** tab, select **View all and manage owners**. Since you are logged into the EAC using Holly Dickson, her account is displayed as the default Owner. However, Holly wants Alex Wilber to co-own the group, so select **+ Add owners** under the **Owners** section.

10. In the **Add Owners** window, select **Alex Wilber**, select the **Add (1)** button, and then select the back arrow. 

11. Select **View all and manage members**. Select **+ Add members** under the **Members** section. 

12. In the **Add Members** window, select **Allan Deyoung**, **Diego Siciliani**, and **Lynne Robbins**. Select the **Add (3)** button and then select the back arrow. 

13. Verify the changes were made and then select the **X** in the top right-hand corner of the pane to close it.

14. You will now add a dynamic distribution list that contains the members of Adatum's new Dynamics CRM project team. Begin by selecting the **Add a group** button. 

15. In the **Choose a group** window that appears, select **Dynamic distrabution**, select **Next**, and then enter the following information:

	- Group name: **Dynamics CRM Project Team**
	
	- Description: **Adatum users working on the Microsoft Dynamics CRM project** 

16. In the **Assign users** section, enter the following information and then select **Next**:

	- Owners: **Holly Dickson**
	
	- Members: Ensure **All recipient types** is selected

17. Under **Edit settings**, enter the following information then select **Next**:

	- Group email address: **DynCRM**

	- Group email address domain: In the domain field to the right of the **DynCRM** alias, select the drop-down arrow and select **xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider)

18. Select **Create Group** and then select **Close**. 

19. Go to the **Dynamic distribution list** and select directly on **Dynamic CRM Project Team**.

20. In the **Dynamics CRM Project Team** window, the **Members** tab is displayed. Under **Owners**, select **View all and manage owners**.

21. In the **Add Owners** window, select **Nestor Wilke**, select the **Add (1)** button, and then select the back arrow.

22. Ensure all changes were made and then close out of the **Dynamics CRM Project Team** window.

23. Leave your browser and all the tabs open for the next task.

### Task 3 - Upgrade Distribution Lists

Organizations have typically relied on distribution groups in Exchange to communicate and collaborate with groups of people both inside and outside the company. However, Microsoft 365 Groups offer a more powerful solution for collaboration, and Adatum’s CTO wants to take advantage of this feature. He has asked you to upgrade the company’s Sales Department distribution list to a Microsoft 365 group so that Adatum’s Sales staff can choose the people they want to collaborate with and easily set up a collection of resources for those people to share.

1. In the **Exchange admin center**, you should still be displaying the **Groups** option under the expanded **Recipients** group in the left-hand navigation pane. 

2. Select the circle to the left of the **Sales Department** distribution list. When a check mark appears, select the three horizontal ellipses icon and select **Upgrade distribution group**.
	
3. A **Ready to upgrade** pop up will appear. Select **Upgrade**. </br></br> 
	**Note:** It may take up to 5 minutes for the Sales Department group to show up under the **Microsoft 365** tab.

4. If the **Sales Department** group still displays as a **Distribution list**, then select the **Refresh** icon in the menu bar above the list. The Sales Department group should now display as a **Microsoft 365** group. 

5. Leave your browser and all the tabs open for the next task. 

### Task 4 - Configure a Group Naming Policy

A group naming policy enables organizations to standardize and manage the names of distribution groups created by its users. You can require that a specific prefix and suffix be added to the name for a distribution group at the time it's created, and you can also block specific words from being used. This helps organizations minimize the use of inappropriate words in group names. 

Adatum’s CTO wants Holly to implement a standard naming policy throughout the organization based on the following format: **{Department}{Group Name}{City}**

1. In the **Exchange admin center**, you should still be displaying the list of groups. In the menu bar that appears over the list of groups, select **Add naming policy.**

2. In the **Edit group naming policy** window that appears, you will add a prefix and a suffix. </br></br>
	In the **For the prefix, apply the following sequence:** field, select the drop-down arrow and select **Attribute**. To the right in the **select one** field, select **Department**.

3. Select **Add prefix**. 

4. Select the drop-down arrow in the box that has **Attribute** and then select **Text**. In the **Add text** field, enter **Group**.

5. Below the **AND  Select a suffix to add to the end of group names**, select the drop-down arrow and then select **Attribute**. Select the drop-down arrow and then select **City**.

6. Review the **Preview policy** example that is based on the parameters you selected. If any need to be fixed, select the correct values now. When everything looks correct, select the **Save** button at the bottom of the window and close out of the pane.

7. Leave your browser and all the tabs open for the next task.

### Task 5 – Manage Resources

A room mailbox is a resource mailbox that is assigned to a physical location, such as a conference room, an auditorium, or a training room. Users can easily reserve these rooms by including room mailboxes in their meeting requests. Adatum’s CTO wants to test this feature using the company’s most popular conference room, and he has asked Holly to configure this resource.

1. In the **Exchange admin center**, you should still be displaying the expanded **Recipients** group in the left-hand navigation pane. Under this group, select **Resources.**

2. In the menu bar, select the **Add a resource** sign and then in the new window, select **Room**.  </br></br>
	‎**Note:** This selection is designed for administrators to set up a meeting location for booking purposes. When scheduling meetings, you will be able to select the room from the Global Address List (GAL).

3. In the **Fill in the basic info** window that appears, enter the following information:

	- Room name: **Conference Room 1**

	- Resource email: **Con1**

	- Email address domain: In the domain field to the right of the **Con1** alias, select the drop-down arrow and select **xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider)
	
	- Capacity: **15**

	- Location: The room is in Building 5, Room 2011, so enter **5/2011**

	- Phone: **425-555-2011**

4. Select **Next** and then select **Next** for the resource address section.

5. In the **Booking options** window, select the **Allow scheduling only during working hours** check box. 

6. Uncheck the **Auto-accepts meeting request** check box. In the **Booking delegates** field, enter **Holly Dickson** and **Nestor Wilke**. </br></br>
	**Note:** This option allows a user to filter booking requests.
	
7. Ensure the box next to **Automatically decline meetings outside of limits below** is selected. If this option is not selected, you won't be able to enter the information in the following steps.

8. In the **Booking window (days)** field, enter **60** days.  </br></br>
	**Note:** As a best practice, organizations should establish a company standard so that events do not over-book locations.

9. In the **Maximum duration (hours)** field, enter **120** hours (this is five days, or one work week). 

10. Select **Next** and then review the resource information. Select **Create** and wait for the resouce to be created. When it's finished, select the **Done** button that appears. You have now successfully created a new room mailbox.

11. Leave your browser and all the tabs open for the next task.

### Task 6 – Manage Contacts

One of the key features of Exchange Online is the ability to maintain different types of contacts in the Exchange Admin Center. In this task, you will be introduced to mail contacts and mail users.

1. In the **Exchange admin center**, you should still be displaying the expanded **Recipients** group in the left-hand navigation pane. Under this group, select **Contacts.**

2. In the menu bar that appears over the list of contacts, select **Add a contact**. and in the menu that appears, in the first drop down menu select **Mail contact.**  <br/>

	‎**Note:** This option enables external people from outside your organization to be added to your Exchange Online distribution lists.

3. In the **Add contact** window that appears, enter the following information.

	- First name: **Hai**

	- Last Name: **Chu**

	- Display Name: tab into the field and **Hai Chu** is automatically displayed

	- External Email Address: **Hai@fabrikam.com**

4. Select **Add** and then select **close** once the changes are successfully saved. Hai should now appear in the list of contacts as a **Mail contact**. If not, refresh your menu and in a minute or so you should see Hai Chu.

5. On the menu bar above the contacts list, select the **Add a contact** sign to add another contact. In the new window in the first drop-down menu, select **Mail user.** (should be selected by default) <br/>

	**Note:** This option is for individuals who need to use the company domain even though they are not a full-time employee (for example: contractors, advisors, and selective temporary staff). This option will forward email to the individual’s external email when mail is sent to the contact’s internal company account.  <br/>
	
	‎**WARNING**: A Mail User does not need a license to access SharePoint Online; the user simply needs to be given access to it.   
	
6. In the **new mail user** window that appears, enter the following information:

	- First name: **Bill**

	- Last Name: **Norman**

	- Display Name: tab into the field and **Bill Norman** is automatically displayed

	- External email address: **Bill@fabrikam.com**
	
	- Alias: Bill 

	- User ID: **Bill** (this is the user’s alias for his internal Adatum account)

	- User ID domain: in the domain field to the right of the User ID, select the drop-down arrow and select **xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider)

	- New password: **Pa55w.rd**

	- Confirm Password: **Pa55w.rd**

7. Select **Add** and then select **Close** once the changes are successfully saved. Bill Norman should now appear in the list of contacts as a **Mail user**. If not, refresh your menu and in a minute or so you should see Bill Norman.

8. Leave the Exchange admin center tab open and proceed to the next task.

### Task 7 – Configure Messaging Protection

Adatum has experienced a recent rash of malware infections. The company's CTO has asked Holly to investigate the various options that are available in Exchange Online to fortify Adatum’s messaging environment.

**Note:** In these next three tasks you will configure malware, connection, and spam filters, respectively. These filters were previously configured in the Exchange admin center; however, starting December 1, 2020, that functionality has been moved to the Security and Compliance Center, which is where you will go to create these filters.

**Permissions Warning:** A user must have appropriate permissions to create malware, connection, and spam filters. To create these objects, a user can be assigned the appropriate permissions in either of two ways:

- The user can be assigned either the Security Administrator or Organization Management role in the Security and Compliance Center.
- You can run a series of PowerShell commands that install the Exchange Online Management module and then enables the user to customize organization settings. 

Because the real-world approach is usually to assign the appropriate role through the Security and Compliance Center, this task will have you assign Holly Dickson to the Organization Management role. However, based on lab testing, it may take up to an hour for the role responsibilities to propagate completely through Adatum's Microsoft 365 tenant in your VM lab environment. As such, when you attempt to save the malware filter that you create in this task, you may receive a Client Error. This error is caused by the simple fact that the responsibilities assigned to the Organization Management role have not propagated completely through your tenant from the time you assigned the role to the time you saved the filter. If you receive this error, you will be given instructions to run the PowerShell commands that enable your ability to create these filters. You should then repeat the insructions in this task to create the malware filter. 

1.  In your **Edge** browser, you should still have a tab open for the **Microsoft 365 admin center**. If so, then select this tab and proceed to the next step; otherwise, navigate to the **Office 365 home** page, log in as your tenant admin account, navigate to the **Microsoft 365 admin center**, and then in the left-hand navigation pane, select **Show all**.

3.  In the **Microsoft 365 admin center**, in the left-hand navigation pane under **Admin centers**, select **Security**.

4.  In the **Office 365 Security & Compliance center**, select **Threat Management** in the left-hand navigation pane, and then in the expanded group select **Policy**.
    
6.  In the **Office 365 Security & Compliance center**, select **Threat Management** in the left-hand navigation pane, and then in the expanded group select **Permissions**.
    
7.  In the **Home \> permissions** page in the **search** field, type **Org** then select the search glass.

8.  On the **Home \> permissions** page list, select the **Organization Management** role.

9.  On the **Organization Management**page under the **members**section, select the **Edit** icon.

10. On the **editing choose members** page. Select **choose members**.

11. On the **choose members** page, Select the **add** icon.

12. On the **choose members** list. Select the **HOlly Dickson** account.Then select the **add** icon.

13. On the **choose members** page. Select the**done** icon.

14. On the **editing choose members** page, select the **save** icon.

     **Note**: the organization management role may take a minute or two to update the microsoft tenant. If the policy doesn't update within a few minutes proceed to the connection filter task. 
     
16.  In the **Home \> Policy** page, select the **Anti-Malware** tile under the
    **Policies** section.

17. In the **Home \> Policy \> Anti-malware** page, on the menu bar at the top
    of the window, select **+Create** to add a new malware filter. This
    initiates the **Create an anti-malware policy** wizard.

18. In the **Name your policy** page, enter **Malware Policy** in the **Name**
    field.
    
19. In the **Description** field, enter **This policy has been created to
    protect the messaging environment** and then select **Next**.   

19. In the **users and domains**section under domains, enter **onmicrosoft.com** and then select **Next**.

20. On the **protection settins** page, select the checkboxes for **enable the common attachements filter** and **enable zero-hour auto purge for malware (recommended)**.

21. On the **Notifications** section, since this filter will not generate any
    notifications, do not select any of the notification options, and instead
    select **Next**.

22. On the **reivew** section, confirm that all the information is correct, then select the submit icon.

23. Congratulations, the New ant-malware policy has been created. Select the done icon.

    **Note**: A **Security & Compliance** window will appear with a message that indicates your organization settings need to be updated. Select **Yes** to continue.
    
24.  It may take a minute or so for your organization settings to be updated. Once the update is complete and you are back on the **Home \> Policy \>
    Anti-malware** page, you can proceed to the next task. Do not close any of the browser tabs.

### Task 8 – Manage Connection Filters

Holly has been contacted by Adatum’s CTO. He is upset that he keeps finding email from friends and business associates in his junk email folder, and he’s even had email blocked entirely by a spam filter. He has asked Holly to address this problem by making sure that email sent from people who are trusted do not get blocked. 

Holly has investigated the situation and has found that in Microsoft 365, you can create a connection filter policy that defines a list of IP addresses that you trust. This is known as an Allow list, or Safe Sender list. You can also create a Blocked senders list, which is a list of IP addresses (typically from known spammers) that you never want to receive email messages from. 

1. In the **Office 365 Security & Compliance** center, you should still be displaying the **Home > Policy > Anti-malware** window. In this thread at the top of the page, select **Policy**. 

2. In the **Home > Policy** window, under the **Policies** section, select the **Anti-spam** tile. 

3. The **Home > Policy > Mail filtering** window displays a list of default **Anti-spam settings** that control how messages are handled by Microsoft 365 anti-spam policies. <br/>

	Select the drop-down arrow to the left of the **Connection filter policy (Default)** filter. This displays the current settings for this default connection filter. Select the **Edit connection filter policy** link.

4. In the **Connection filter policy** pane that appears, the **Connection filtering** section displays options regarding which IP Addresses will be allowed to send messages to your environment and what IP addresses will be blocked from sending messages. <br/>

	At this time, you will NOT be adding IP addresses to the allow or block lists. You can do this if you have a known IP address you would like to test against. It typically takes up to 1 hour to replicate the change within the system. For this lab, simply review the fact that you can create allowed and blocked lists of IP addresses.

5. At the bottom of the **Connection filtering** section, select the **Turn on safe list** check box. This is a best practice that enables for your tenant the most common third-party sources of trusted senders that Microsoft subscribes to. Selecting this check box skips spam filtering on messages sent from these senders, ensuring they are never mistakenly marked as spam.

6. Select **Save** to save this filter, and then select **OK** once the changes are successfully saved.

7. Leave your Edge browser open to the **Office 365 Security & Compliance** center for the next task.


### Task 9 – Manage Spam Filters

For Microsoft 365 customers whose mailboxes are hosted in Microsoft Exchange Online, their email messages are automatically protected against spam and malware. Microsoft 365 has built-in malware and spam filtering capabilities that help protect inbound and outbound messages from malicious software and help protect you from spam. 

As Adatum’s Global Admin, Holly doesn't need to set up or maintain the filtering technologies, which are enabled by default. However, she can make company-specific filtering customizations in the Security and Compliance center. She has decided to test this out by configuring a spam policy to grant or deny an email by focusing on the language of the email and the location of the email's origin.


1. In the **Office 365 Security & Compliance** center, you should still be displaying the **Home > Policy > Mail filtering** window after having completed the prior task. <br/>

	Select the **Anti-spam inbound policy (Default)** filter. This displays the current settings for this default spam filter. Take a moment and review the policy settings that are available in this filter, and then select the **Edit actions** link. 

2. Make the below changes then select **Save**.	‎**Note:** In this section you will be presented a variety of options on how you would like spam to be handled and what rating will be triggered depending on the severity of the spam.

3. In the **spam and bulk actions** section, make the following selections:

	- Spam: **Move message to Junk Email folder**

	- High confidence spam: **Prepend subject line with text**

	- Phishing email: **Quarantine message**

	- High confidence phishing email: **Quarantine message**

	- Bulk: **Move message to Junk Email folder**

	- Select the threshold: **5**

	- Quarantine (retain spam for days): **10** 

	- Prepend subject line with this text: enter **WARNING: This message contains potential spam!**
	
	- Enable end-user spam notifications check box, and then change the **Send end-user spam notifications every (days)** value to **5**.


4. Select the drop-down arrow to the right of the **International spam** section.  <br/>

	‎**Note:** This section allows you to automatically tag messages as spam when they originate from countries/regions that are to be avoided or distrusted, as well as messages written in specific languages.

5. Select the **Edit spam threshold and properties** link.

6. In the **Mark as spam** section, select the **Contains specific languages** drop down, and select **On**. 

7. You should already know the languages that you want to filter. In the **Languages** field, enter the first letter of a language that you want to filter. This will display all languages that start with that letter (as well as any languages that contain that letter within the name of the language). <br/>

	Enter a letter and then select a language with that letter in it that you want to filter. Repeat this step for a couple of languages. 

9.  In the **Mark as spam** section, select the **From these countries** drop down, and select **On**.
=======
1.  You should still be logged into LON-CL1 as the **Administrator** with a
    password of **Pa55w.rd**; however, if the log-in page appears, then log in
    now.

2.  In your **Edge** browser, you should still be in the **Office 365 Security &
    Compliance center** (SCC). If so, then proceed to the next step; otherwise,
    perform the steps from the prior task to navigate to the SCC now.

3.  In the **Office 365 Security & Compliance center**, you should still be on
    the **Anti-spam settings** page after completing the prior task. If so, then
    proceed to the next step; otherwise, in the left-hand navigation pane,
    select **Threat Management**, select **Policy,** and then select the
    **Anti-spam** tile under the **Policies** section.

4.  In the **Anti-spam policies** windows in the list of policies, select the
    **Anti-spam inbound policy(defualt)**.


5.  In the **Anti-spam inbound policy (default)** pane, you will be
    presented a variety of options on how you would like spam to be handled and
    what rating will be triggered depending on the severity of the spam. The
    following steps will guide you through these settings so that you can update
    them per Adatum's requirements.

6.  Select the **edit spam threshhold and properties** link, under the **bulk email threashold & spam properties** section. Update the
    following settings:


13. Select the drop-down arrow to the right of the **Spam properties** section.  <br/>

    -   set the threshold: **5** 
   
    -   **mark as spam** 
    -   empty messages: **Off**
    -   Embedded tags in HTML: **On**
    -   JavaScript or VBScript in HTML :**On**
    -   SPF record hard fail: **On**
    -   Sender ID filtering hard fail: **On**
    -   from these counties:

           -   Type the letters **"ab"** in the **from theses countries** field to display
                the list of countries starting with the letters “ab” or that
                include an “ab”. You can enter any letter or letters that you
                wish.


           -   Select any country/region you want to restrict.

14. Under the **Spam properties** section, turn **On** the following options:

           -   If you want to restrict an additional country, repeat the
                prior two steps.
                
                
7.  Once you have selected all the countries/regions that you want to restrict. Select **save**.             

8.  Select the **edit actions** icon under the **actions** section to update the following
    settings:

    **Note:** This section determines what happens to emails that have been tagged as spam.


15. Under the **Mark as spam** section, turn **On** the following options:

    -   Select the **spam** drop-down arrow and select the **Move message to junk email folder**.


    -   Select the **phishing** drop-down arrow and select **quarrantine message**.


	- **Sender ID filtering: hard fail**

     -  change **retain spam in quarantine for this many days** to **10** days.

9.  Select **Save**.


17. In your Edge browser, close the **Security & Compliance** center tab, but leave all other tabs open. 

10.  In the list of spam filters, select the drop-down arrow to the left of the
    **Default spam filter policy (always ON)** filter that you just edited. In
    the middle column of settings for this filter, note how **End-user spam
    notifications** are disabled (it status is **Off**). <br/><br/>
    Below this option, select **Configure end-user spam notifications**.

11.  In the **Default** window that appears, select the **Enable end-user spam
    notifications** check box, and then change the **Send end-user spam
    notifications every (days)** value to **5**.

12.  Select **Save**.

13. In your Edge browser, close the **Security & Compliance** center tab, but leave all other tabs open. 


### Task 10 – Manage Mail Flow Rules 

After Holly reviewed the messaging environment at Adatum Corporation, she realized that she could provide a more efficient and secure environment if she created a set of mail flow rules that identify and take action on messages that are in-transit through her Exchange Online organization, as opposed to simply waiting until the messages are delivered to mailboxes before being acted upon by Inbox rules in Outlook and Outlook on the web. 

Holly has discovered that mail flow rules contain a richer set of conditions, exceptions, and actions, all of which will provide her with the flexibility to implement many types of messaging policies for Adatum. She is eager to put this to the test regarding a significant issue currently affecting Adatum’s messaging environment - users who send extremely large email messages. She has decided that her first task will be to create a mail flow rule that restricts email size.

1. On LON-DC1, select the **Exchange admin center** tab in your Edge browser, and then in the left-hand navigation pane select **mail flow**.

2. Under **Mail flow**, select **rules**. <br/>

	**Note:** In this section you will be presented with a variety of options to protect against emails being sent from Adatum that have sensitive information, as well as creating custom rules to prevent or track messaging-related issues from recipients in your environment. For the purposes of this lab, you will only update the email size restriction rule.

3. In the menu bar that appears over the list of mail flow rules, select the **plus (+)** sign, and in the menu that appears, select **Filter messages by size.**

4. In the **new rule** window that appears, enter the following information:

	- Name: **Email size restriction**

	- Apply this rule if: select **The message size is greater than or equal to...** 

		- To the right of this drop-down field, select **Enter text**.

		- In the **specify size (KB)** window that appears, enter **1024** and then select **OK**. 

	- Do the following: hover your mouse over **Block the message...**, and then in the drop-down menu that appears, select **Reject the message and include an explanation**. 

			
		- In the **specify rejection reason** window, enter the following text: **Your message exceeds the size limit. Please adjust the message size or compress the email content and send it as a zipped file.**

		- Select **OK.**

	- Under **Choose a mode for this rule**, select **Enforce.**

5. Select **Save**.

6. Leave your Edge browser open as well as all the tabs.


### Task 11 – Validate Accepted Domains

A domain that’s added to an organization's on-premises environment is called an accepted, or custom domain. You can create mailboxes with accepted domains to receive and send email. In Lab 1, you created a domain for Adatum Corporation based on the unique UPN name assigned to your tenant and the custom domain name provided by your lab hosting provider (in this case, xxxUPNxxx.xxxCustomDomainxxx.xxx, where xxxUPNxxx is your unique UPN Name and xxxCustomDomainxxx.xxx is the domain created by your lab hosting provider). 

In this task, you will use the Exchange Admin Center to view the accepted domain that you previously created and configure its domain type. Each domain can be changed to either authoritative (which accepts all inbound or outbound mail) or internal relay (which only accepts internal email). By default, all domains should be set to authoritative. You want to ensure that your custom domain’s type is set to authoritative.

1. In the **Exchange admin center**, you should still be displaying **mail flow** from the left-hand navigation pane. Under the mail flow section, select **accepted domains.**

2. In the list of accepted domains, you should see Adatum’s two domains – its custom on-premises domain (xxxUPNxxx.xxxCustomDomainxxx.xxx) that you added in Lab 1, and its Microsoft 365 cloud domain (xxxxxZZZZZZ.onmicrosoft.com).

3. You can see from this display that the domain type for each domain is already set to **Authoritative,** so you don’t need to make any changes here. 

4. However, let’s assume that you set the domain type to **Internal Relay** when you initially created the custom **xxxUPNxxx.xxxCustomDomainxxx.xxx** domain. If you wanted to change it now to **Authoritative,** you would perform the following steps (you can perform the first step to see the window and the corresponding options, but the domain is already set to Authoritative, so you can’t actually make this change):

	- Select this domain in the list, and then select the **pencil (edit)** icon on the menu bar. 

	- In the window for this domain, under **This accepted domain is:** you would select the **Authoritative** option and then select **Save**. However, since you did not make any changes, select **Cancel** to close this window.

5. This concludes the exercise on reviewing Exchange Online features. You can close the **Exchange admin center** tab in your Edge browser. This will return you to the **Microsoft 365 admin center** tab, which you will access in the next exercise.


# Proceed to Lab 3 - Exercise 2


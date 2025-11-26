# Windows-Server-Backup-Restore

Windows Server System Backup and Restore – Practical Summary This project shows how to create a system backup of a Windows Server and how to restore it later when needed.

✅ What I did: Took a System Backup (includes system state and essential system files).

Used the Windows Server Backup tool to create the backup.

Saved the backup to a different drive or location.

Planned to restore the server's system using this backup (for recovery purposes).

🎯 Purpose: To show how to protect the Windows Server system using backup and restore in case of failures or system issues.

## Step
#### 1.In this screenshot ,I have created some users,Later,I will delete them and then restore the system to bring them back.
<img width="895" height="634" alt="1" src="https://github.com/user-attachments/assets/6909cccd-1766-4308-a0c3-fee17b57e119" />

#### 2.Click on "Add Roles and Features" to install the Windows Server Backup feature.
<img width="983" height="718" alt="2" src="https://github.com/user-attachments/assets/81a964c1-066a-4713-9e2e-d520d5f6d00b" />

#### 3.In the Features section, check the Windows Server Backup option, then click Next and proceed with the installation. Once the installation is complete, go to the Tools menu. At the bottom, you will find Windows Server Backup click on it to open.
<img width="812" height="584" alt="3" src="https://github.com/user-attachments/assets/c7d6911e-2357-4a20-a70c-5cde9ba46f99" />

#### 4.Now, click on Local Backup. You will see two options: Backup Schedule (used to configure daily backups) and Backup Once (used for a one-time manual backup). In this practical, I will perform a Backup Once operation.
<img width="1013" height="671" alt="4" src="https://github.com/user-attachments/assets/4432bc5b-2de7-4cb2-9807-54bce9b9e277" />

#### 5.Click on Backup Once, then select the Custom option and click Next to proceed.
<img width="670" height="559" alt="5" src="https://github.com/user-attachments/assets/b5631c88-b346-4b15-8f67-2e2de0d3300a" />

#### 6. Click on Add Items to select the components you want to include in the backup
<img width="665" height="553" alt="6" src="https://github.com/user-attachments/assets/55b6fbaf-7831-4c8b-8470-f1434f27df4a" />

#### 7. Select System State, as this backup will include Active Directory and other essential system services.
<img width="546" height="377" alt="7" src="https://github.com/user-attachments/assets/9bee9759-0a81-4484-b63f-1a8807655d34" />

#### 8. I am going to store the backup on the E: drive, but you can choose any location based on your requirements.
<img width="661" height="548" alt="8" src="https://github.com/user-attachments/assets/46c6b21e-9511-4dc4-984b-fee1734921a0" />

#### 9. Now, select your destination drive and click Next to continue.
<img width="663" height="551" alt="9" src="https://github.com/user-attachments/assets/68f55b34-f8b8-432c-8605-9d289cd46e43" />

#### 10. On the Confirmation page, click Backup to start the process.
<img width="668" height="550" alt="10" src="https://github.com/user-attachments/assets/cbc0afee-6072-4258-9afa-a5a16c2cf6a1" />

#### 11. You can now see that the system backup process has started.
<img width="662" height="547" alt="11" src="https://github.com/user-attachments/assets/b644f7b8-8af6-4cb8-b13e-75877dd25a0d" />

#### 12. The system backup has been completed successfully.
<img width="661" height="550" alt="12" src="https://github.com/user-attachments/assets/5bc4d0a1-d964-48a4-bfcc-ca223394764b" />

#### 13. You can see that the backup has been successfully saved to the E: drive.
<img width="940" height="245" alt="13" src="https://github.com/user-attachments/assets/400af46a-2e1c-4f3a-bad7-89a387845ac1" />

#### 14. Now that the backup is complete, we will delete the users we created earlier. After that, we will proceed with the restoration to recover them.
<img width="963" height="692" alt="14" src="https://github.com/user-attachments/assets/5932e82b-d75d-43d8-940f-ec4240f573cf" />

#### 15. Now, open Windows Server Backup and click on Recover to begin the restoration process.
<img width="967" height="718" alt="15" src="https://github.com/user-attachments/assets/3ccd2a63-2689-4cbe-90b6-86ab09f1870e" />

#### 16. To recover the system backup, we must boot into Directory Services Restore Mode (DSRM); otherwise, an error will occur during the restoration process.


 What is DSRM (Directory Services Restore Mode)? DSRM (Directory Services Restore Mode) is a special boot mode in Windows Server used for performing maintenance or recovery tasks related to Active Directory.

🔍 Why is DSRM used? It temporarily disables Active Directory so you can safely perform tasks like:

Restoring system state (e.g., from a backup)

Repairing or recovering Active Directory

Troubleshooting domain controller issues
<img width="739" height="569" alt="16" src="https://github.com/user-attachments/assets/e77ca173-0351-45ec-b032-01e40a4f0066" />

#### 17. To enter DSRM mode, press Windows + R, type msconfig, and press Enter.
<img width="411" height="235" alt="17" src="https://github.com/user-attachments/assets/85a0e6be-74ef-49a4-a068-5bd34c9a7e65" />

#### 18. Then, go to the Boot tab, check the Safe boot option, and select Active Directory repair. After that, click Apply, then OK.
<img width="566" height="381" alt="18" src="https://github.com/user-attachments/assets/8722e523-2efa-4713-b4a7-caa982419949" />

#### 19. Your system will now restart and boot into Directory Services Restore Mode (DSRM).
<img width="442" height="273" alt="19" src="https://github.com/user-attachments/assets/00bbf6c0-5ff2-4684-a15d-2fea6258fe10" />

#### 20. While in DSRM mode, open Windows Server Backup, and click on Recover to begin the restoration process.
<img width="1008" height="624" alt="20" src="https://github.com/user-attachments/assets/a5e39243-8917-403d-aed3-cd6d612c238e" />

#### 21. Click Next
<img width="736" height="575" alt="21" src="https://github.com/user-attachments/assets/5099aefc-5a87-4fe0-97ce-064143f9e76e" />

#### 22. Select the date and time when the backup was created.
<img width="738" height="575" alt="22" src="https://github.com/user-attachments/assets/1a6cffc8-7228-4512-9a40-7be58b46141b" />

#### 23. Now, select the type of backup you want to restore. In this case, I am restoring the System State backup.
<img width="742" height="575" alt="23" src="https://github.com/user-attachments/assets/f2643335-10da-4ca7-aa8d-0455b6ddd8d3" />

#### 24. Click Next the OK
<img width="742" height="585" alt="24" src="https://github.com/user-attachments/assets/2688e731-3904-4388-b6f1-6adcae9b46bd" />
<img width="876" height="684" alt="25" src="https://github.com/user-attachments/assets/83f04b5b-dbe0-454f-8d11-d6dbd599db53" />

#### 25. Now,Click on Recover to start the restoration process.
<img width="593" height="469" alt="26" src="https://github.com/user-attachments/assets/246ddb00-8ff2-4642-9729-07a00814e88b" />

#### 26. You can now see that the data recovery process has startted.
<img width="596" height="468" alt="27" src="https://github.com/user-attachments/assets/fb13e392-1f5e-4aed-b1db-8cb5a8c07926" />

#### 27. Once the recovery is complete, restart your system and exit DSRM mode by following the same steps in msconfig, but this time uncheck Safe boot, then click Apply and OK.
<img width="603" height="464" alt="28" src="https://github.com/user-attachments/assets/744c02b3-3bc2-4b9c-9ba7-757b50e19f27" />

#### 28. You can now see that the users we previously deleted have been successfully restored.
<img width="993" height="630" alt="29" src="https://github.com/user-attachments/assets/6887d944-4b08-4d75-9e56-05b20fb4d6e8" />

#### 29.All data has been successfully restored.
<img width="1022" height="754" alt="30" src="https://github.com/user-attachments/assets/d05a8d10-6403-4fe8-8091-2a790bbc86d7" />











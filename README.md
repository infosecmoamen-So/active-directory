<h1>Centralized Identity & Access Management (IAM) via Active Directory</h1>

### [YouTube Demonstration](https://youtu.be/)

<h2>Description</h2>
This project demonstrates the deployment, orchestration, and compliance governance of an enterprise-level centralized Identity and Access Management (IAM) framework using Windows Active Directory Domain Services (AD DS). The practical workflow simulates core duties within a systems administration and security infrastructure role, focusing on automated directory instantiation via elevated PowerShell frameworks, user identity lifecycle governance under strict password hygiene compliance, Role-Based Access Control (RBAC) modeling via structural group nesting, and the mitigation of privilege creep (identity drift). Furthermore, it addresses enterprise endpoint control by deploying, linking, and enforcing specific Group Policy Objects (GPOs) targeted at Organizational Units (OUs) to maintain a secure configuration baseline across corporate network domains in accordance with the Principle of Least Privilege (PoLP).
<br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> (Automated structural installation & directory environment post-deployment configuration)
- <b>Active Directory Administrative Center (ADAC)</b> (Centralized management of users, global security group mappings, and nested memberships)
- <b>Group Policy Management Console (GPMC)</b> (Authoring, linking, auditing, and enforcing organizational unit policies and security baselines)

<h2>Environments Used </h2>

- <b>Windows Server</b> (Virtual Machine Cloud Sandbox Environment)
- <b>Remote Desktop Protocol (RDP)</b> (Secure graphical network operational session)

<h2>Program walk-through:</h2>

<p align="center">
Launch the initial cloud instance environment deployment setup menu within the laboratory platform: <br/>
<img src="https://i.imgur.com/AOiHBxD.png" height="80%" width="80%" alt="Start Lab Instance"/>
<br />
<br />
Acknowledge the live active environment instance allocation provisioning the secure Windows Virtual Machine controls: <br/>
<img src="https://i.imgur.com/wi1OJXD.png" height="80%" width="80%" alt="Windows VM Panel"/>
<br />
<br />
Initiate the secure RDP interface to establish an operational graphic workspace with the target Windows operating system: <br/>
<img src="https://i.imgur.com/xNdcIoX.png" height="80%" width="80%" alt="Windows OS Workspace"/>
<br />
<br />
Open the Windows Start Menu, navigate to the command line utility ecosystem, and execute Windows PowerShell with administrative privileges ("Run as Administrator"): <br/>
<img src="https://i.imgur.com/g097cw5.png" height="80%" width="80%" alt="Elevated PowerShell Shell"/>
<br />
<br />
Execute the automated sequence installation script to spin up the core Active Directory Domain Services (AD DS) framework: <br/>
<code>C:\Qwiklabs\ADSetup\active_directory_install.ps1</code> <br/>
<img src="https://i.imgur.com/4qCmGsi.png" height="80%" width="80%" alt="AD DS Script Installation"/>
<br />
<br />
Observe the systemic automated endpoint reboot sequence causing a standard RDP session connection drop panel: <br/>
<img src="https://i.imgur.com/DE9uqXP.png" height="80%" width="80%" alt="RDP Disconnect Warning"/>
<br />
<br />
Reconnect to the Windows Server, launch an elevated PowerShell shell, and run the secondary post-deployment network root domain baseline configuration routine script (<code>C:\Qwiklabs\ADSetup\configure_active_directory.ps1</code>). Once complete, open the Start Menu and launch the Active Directory Administrative Center (ADAC): <br/>
<img src="https://i.imgur.com/ykNdzeq.jpeg" height="80%" width="80%" alt="Launching ADAC Application"/>
<br />
<br />
Access the primary directory node dashboard interface under the managed enterprise infrastructure root domain "example (local)": <br/>
<img src="https://i.imgur.com/rOH6Kib.jpeg" height="80%" width="80%" alt="ADAC Management Console"/>
<br />
<br />
Navigate into the structural "Users" object container path, open the Tasks menu section on the right, and choose New > User option: <br/>
<img src="https://i.imgur.com/uV7AzFj.jpeg" height="80%" width="80%" alt="Identity Creation Submenu"/>
<br />
<br />
Populate the mandatory security fields and identity properties to provision a new employee domain profile for "Alex" (User Sam Account Name: alex): <br/>
<img src="https://i.imgur.com/hig3CE6.jpeg" height="80%" width="80%" alt="User Profile Properties Metadata"/>
<br />
<br />
Observe the operational security default where the newly provisioned directory asset is instantiated in a strict "Disabled" state: <br/>
<img src="https://i.imgur.com/zrmIpwH.jpeg" height="80%" width="80%" alt="Disabled Baseline Identity Check"/>
<br />
<br />
Test directory security compliance controls by attempting to force-enable the account, generating an error due to the absence of a defined complex password baseline: <br/>
<img src="https://i.imgur.com/0EJ5EZU.jpeg" height="80%" width="80%" alt="Account Enforcement Error Warning"/>
<br />
<br />
Select the "Reset password" context menu parameter interface to input a standardized corporate credential complexity string: <br/>
<img src="https://i.imgur.com/BOrVTrJ.png" height="80%" width="80%" alt="Credential Injection Window"/>
<br />
<br />
Enforce mandatory credential rotation by explicitly marking the "User must change password at next logon" checkbox to ensure administrator credential secrecy, then successfully transition the account to "Enabled": <br/>
<img src="https://i.imgur.com/vnU8giJ.jpeg" height="80%" width="80%" alt="Enforcing Access Governance Controls"/>
<br />
<br />
Access the task layout options panel to instantiate a new global network operational unit security entity under the Group option: <br/>
<img src="https://i.imgur.com/USwEcXQ.jpeg" height="80%" width="80%" alt="Group Object Generation Submenu"/>
<br />
<br />
Define the mandatory naming parameters to structure the global corporate deployment block under the moniker "Python Developers": <br/>
<img src="https://i.imgur.com/eCgvvP8.jpeg" height="80%" width="80%" alt="Group Mapping Configuration Panel"/>
<br />
<br />
Right-click the newly compiled cluster asset entry and select the "Add to another group" linking management sequence: <br/>
<img src="https://i.imgur.com/5QG66lk.jpeg" height="80%" width="80%" alt="Initiating Nesting Path Selection"/>
<br />
<br />
Specify the destination parent container "Developers" and utilize the "Check Names" logic verification matrix to establish optimized nested security groups: <br/>
<img src="https://i.imgur.com/TSyxepY.jpeg" height="80%" width="80%" alt="Validating Structural Hierarchy Mapping"/>
<br />
<br />
Double-click on the "Python Developers" group node object to display its global configuration attributes and mapping layout workspace: <br/>
<img src="https://i.imgur.com/TWXG66D.jpeg" height="80%" width="80%" alt="Group Attributes Layout"/>
<br />
<br />
Navigate to the "Members" structural path list link, call the identity allocation interface browser, and map user account "Alex" to the target team roster: <br/>
<img src="https://i.imgur.com/1CZVR3Z.png" height="80%" width="80%" alt="Mapping Active Identity Membership"/>
<br />
<br />
Audit employee user "Alosha" to investigate department transfer adjustments by launching the user's properties and filtering the "Member Of" tab details: <br/>
<img src="https://i.imgur.com/nl6ulGy.jpeg" height="80%" width="80%" alt="Auditing Group Membership Fields"/>
<br />
<br />
Remediate role drift and privilege creep by selecting the stale "Java Developers" asset, clicking "Remove" to strip excessive access rights, and then using "Add" to assign membership inside the current "Python Developers" group: <br/>
<img src="https://i.imgur.com/2mJGswm.jpeg" height="80%" width="80%" alt="Remediating Privilege Creep Overlap"/>
<br />
<br />
Open the Windows Start Menu, look up administrative applications, and initialize the Group Policy Management Console (GPMC) to audit domain endpoint policies: <br/>
<img src="https://i.imgur.com/4bgCkjV.jpeg" height="80%" width="80%" alt="Launching Group Policy Console"/>
<br />
<br />
Expand the domain structural hierarchy system to pinpoint, isolate, and audit the specific targeted "Developers" Organizational Unit (OU): <br/>
<img src="https://i.imgur.com/Bl0mZfr.jpeg" height="80%" width="80%" alt="Isolating the Target Organizational Unit"/>
<br />
<br />
Right-click the "Developers" OU and click "Create a GPO in this domain, and Link it here...", assigning the enforcement envelope the baseline name "New Wallpaper": <br/>
<img src="https://i.imgur.com/Va4tvX5.jpeg" height="80%" width="80%" alt="Deploying Localized Boundary GPO Link"/>
<br />
<br />
Right-click the newly mapped GPO container object and open the "Edit" workspace context layer to prompt the Group Policy Management Editor application: <br/>
<img src="https://i.imgur.com/eIyF6zv.jpeg" height="80%" width="80%" alt="Invoking Group Policy Core Editor"/>
<br />
<br />
Navigate the policy blueprint node structure down the following administrative container tree path: <br/>
<code>User Configuration > Policies > Administrative Templates > Desktop > Desktop</code> <br/>
<img src="https://i.imgur.com/AX5oeaK.jpeg" height="80%" width="80%" alt="Traversing Administrative Policy Schema Path"/>
<br />
<br />
Isolate the specific policy property file named "Desktop Wallpaper" and double-click the item entry node to configure its operational environment boundaries: <br/>
<img src="https://i.imgur.com/1GF8nEx.jpeg" height="80%" width="80%" alt="Accessing Wallpaper Policy Rule Configuration"/>
<br />
<br />
Switch the administrative status to "Enabled" and inject the exact local endpoint system file storage path reference (<code>C:\Qwiklabs\wallpaper.jpg</code>) to lock down the baseline across targeted client nodes: <br/>
<img src="https://i.imgur.com/jTu6ITt.jpeg" height="80%" width="80%" alt="Enforcing Centralized Infrastructure Baselines"/>
</p>

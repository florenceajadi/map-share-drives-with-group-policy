<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Map Share Drives with Group Policy</h1>
This tutorial outlines the implementation of Mapping Share Drives with Group Policy in Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Map Share Drives with Group Policy](https://youtu.be/cG7M3Z-Cek4)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
  
<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Create two new groups: Group A and Group B
- Create a new Domain User called Jackie Robbins
- Create two share groups and giving permissions in Server Manager
- Verify change is made by logging into user accounts
- Create a new GPO.
- Run command prompt
- Verify change is made by logging into user accounts


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="" height="80%" width="80%""/>


</p>
<p>
Diagram
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/c78a49b3-6d88-435b-8145-4e23c1157e47" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/f9f6c05c-de37-456e-ab30-e7c7d6a960c7" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/4cea0c43-e6d7-49ed-98e6-e299b5785cd8" height="80%" width="80%""/>

</p>
<p>
Created two groups called Group A and Group B within Organizational Unit Domain Groups. a new Share folder on Server Manager called 'Profiles$' so the folder stays hiddern. Also allowing who is permitted to have access to Profiles$.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/e4e337f2-0c5a-40a3-993e-5d88c6fa002b" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/2ad71870-1ae3-4ad0-8ef8-45f70d6e4631" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/5c28c909-e94d-4214-9fb9-a045f0e4458a" height="80%" width="80%""/>

</p>
<p>
Added user Jeremy Collins as a member of Group A. Created a new user named Jackie Robbins and added Jackie Robbins to Group B member.
</p>
<p>
<img src="https://github.com/user-attachments/assets/6ca05210-197c-48f8-976b-2690a843dc30" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/2e4d4e55-e6e0-4bfd-8917-e1f81dc90c34" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/d0c56e2b-4fd5-4ec0-a71c-690b10ecfc46" height="80%" width="80%""/>

</p>
<p> Creating two share folders for Group A and Group B, authorizing permission access. </p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/b464b2c5-b3c4-449e-b669-66139042421b" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/3c396aaa-b32e-43c1-a27c-5a7a6bd5965a" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/36ebaf7d-1476-433f-a9d9-f960ea717d2e" height="80%" width="80%""/>
</p>

<p>
I am logged into user Jeremy.Collins account who has access to Group A folder. As you can see, Jeremy Collins is a member of Group A, so he shouldn't have access to Group B folder.
  I did the same for Jackie.Robbins account who has access to Group B folder. As you can see, Jackie Robbins is a member of Group B, so she shouldn't have access to Group A folder.
</p>
<p>
<img src="https://github.com/user-attachments/assets/4b2e9fd5-146a-43c7-86bd-cf1d4fc279aa" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/aeb4b0d8-a665-4217-b44c-7d8555cc1adc" height="80%" width="80%""/>

</p>
<p>Created two shared folders: Group A and Group B </p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/777e9985-93b6-4f45-acc4-a7d97a7cd7ff" height="80%" width="80%""/>
</p>
<p>
  Created a new GPO called 'Group A Mapped Drive'
</p>
<p>
  <img src="https://github.com/user-attachments/assets/b73be96b-acd5-4995-b757-36f0268a13f4" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/8ec464ed-52dc-4754-8f47-2b96fef09310" height="80%" width="80%"" />
</p>
<p> Able to create a new mapped drive. Also able to add GROUP A to the Security Filtering.</p>
<p>
  <img src="https://github.com/user-attachments/assets/43b7ea8e-ca30-4994-b359-18d212cd1337" height="80%" width="80%""/>
</p>
<p>Created a new GPO called 'Group B Mapped Drive' </p>
<p>
  <img src="https://github.com/user-attachments/assets/41d95497-f3dc-4af4-ae42-1733f867e255" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/4ceb508f-285f-4f5c-8686-4b6392ab321b" height="80%" width="80%""/>
</p>
<p>Able to create a mapped drive. Also able to add GROUP B to the Security Filtering.</p>
  <p>
    <img src="https://github.com/user-attachments/assets/cc3999fe-0b9d-4772-b2f9-b2f6ab328dcf" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/da35876d-6e8c-4bf8-806f-b6121c6cf157" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/893aa7b7-5c6c-46fb-b46b-fdfad3e3f1cd" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/d530759e-1216-4965-80a5-81239221ad0c" height="80%" width="80%""/>
                                        
</p>

  
<p>
Able to create Delegation for Authenticated Users giving them read access permission. </p>

<p>
  <img src="https://github.com/user-attachments/assets/f16ce49c-2e17-4d4c-ae47-f89c7a25ab60" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/a3ce4fad-b244-42dd-9d0f-9d2adf363778" height="80%" width="80%""/>
</p>
<p>logged into Jeremy Collins account, using command prompt to run gpupdate /force. Also to see if the Group A drive would be located in the pc, which it was. </p>
<p>
  <img src="https://github.com/user-attachments/assets/beb3b541-74d2-4e0b-ad81-6909a7a05b1c" height="80%" width="80%""/>
  <img src="https://github.com/user-attachments/assets/feaf7336-d7b6-4d70-997b-222f79126ace" height="80%" width="80%""/>
</p>
<p>logged into Jackie Robbins account, using command prompt to run gpupdate /force. Also to see if the Group B drive would be located in the pc, which it was. </p>

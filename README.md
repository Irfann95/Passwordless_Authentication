<h1>Tutorial : How to configure a Passwordless Authentification in Keycloak</h1>

<p>Keycloak is an open-source software devellopped by Redhat allowing to create an unique authentification method across identity and access management.In other words, this software allows the security of mobile et web aplications by managing users identity and by controling the ressources access. There are differents fonctionalitys in Keycloak such as management of users, authentification, authorization ant management of sessions for web and mobiles applications. Here, I will you show how to configure a passwordless authentification thanks to Keycloak </p>

<h2>Prerequisite</h2>
To configure a passwordless authentification, you have, of cource, to install Keyclaok. I send you an installation guide here:  https://www.keycloak.org/docs/18.0/server_installation/ <br>
<br>Important: Install et set up the latest version of java is required.

<h2>Tutorial</h2>

Once installation is finish, you're supposed to be connected on Keycloak as an administrator and this menu supposed to be shown. <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/0d807052-4630-4709-bc30-07fb712a460c" alt="Texte alternatif" width="800" height="400">

Then, you have to click on "master" and click "create realm". A realm is isolate space where you manage objects, including users, applications, roles, and groups. Then you can rename your realm.

<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/431a5118-1830-452d-b322-dd5fc27beab2" alt="Texte alternatif" width="300" height="200"><img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/dfad20f5-0d56-4765-9cfa-b8e13ade0b19" alt="Texte alternatif" width="300" height="200">

Once your realm created, click to "Authentification" in Configure Menu and click on browser file, duplicate this flow ansd rename the duplicated flow "OTP and WebAuthn".<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/cfa0ffda-3135-480b-a768-f873742d5751" alt="Texte Alternatif" width="350" height="200">
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/ad1b683d-f15f-4e51-ac5e-950bbd07caf0" alt="Texte alternatif">

Then, go to flow details, delete these two steps ; "Username Password Form" and "OTP and WebAuthn Browser - Conditional OTP. add step to OTP and WebAuthn forms.<br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/0cca3417-b713-46b4-8b6e-778be5d1d8e3" alt="" width="300" height="200"> <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/b1a168fa-ed30-4635-b79d-f27a99c1dea2" alt="" width="400" height="200"> <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/20bfcf79-b875-45b7-8860-a48fe70a653f" alt="" width="400" height="200"> <br>
<br>
Click on "Add step" to OTP and WebAuthn forms and add "Username Form" and "WebAuthn Passwordless Authenticator".<br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/8d42a1fd-0803-4778-9c31-44e6791d8a1a" alt=""> <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/d21f4175-824b-49df-bcb8-59748411cbaf" alt=""><br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/bc749186-3942-4b01-a74d-f41939f45ffc"><br>
<br>
Important : the WebAuthn Passwordless Authenticator must to be required and not Alternative. <br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/607ad067-1848-40b9-a784-86bab6f57820">

<br>
After deleting and adding these steps on you're flow, the flow plan supposed to look like this : 
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/9745fe8a-3955-456e-97b8-08c71fd80b0a"> <br>
<br>
Then, click in the case "Action", click "Blind flow", verify that binding type is Browser flow and save your flow.<br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/aaeaf4e0-45d2-45f1-99cd-1d6f11c89cd6"><br>
<br>
Then, go to required actions, and check boxes like this : <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/d331f2d9-243c-48c2-8d72-c5bdeb6c8543"><br>
<br>
Next, go to the realm settings and activtate the use registration in login. <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/9217d658-84a6-4bbc-bee5-9cb300e50556"> <br>
<br>

Now, you are confingured the Passwordless Authentification method in your realm.

<h2>Test</h2>

Now, a function test can be performed. Let's get start:
First of all, you need to go to the "clients" section under "manage". Then click on the URL of client named "account". <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/762d5370-3fd9-41a6-92a7-10bd0b2c9401"> <br>
<br>
A new home window supposed to be open. Now we try to sign in with Passwordless Authentification. <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/883d5d62-ba41-46c6-8043-348aa173d664"> <br>
<br>
Click on "Sign" at top right.<br>
<br>
We want to be connected as an user, and and since we are a new users, we have to click on "resgister" and complete the form. <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/883d5d62-ba41-46c6-8043-348aa173d664"> <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/aed714b0-c65e-444c-82ad-69513ab39602" width="300" height="400"> <br>
<br>
After completing the form, click on "register" and on the link allowing to reveal a QR code. Scan the QRCode in you're phone and, normally, you're supposed to be connected as an user.
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/458a705d-4795-4cd7-8ecb-cf06f4b19f2d"> <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/55ff12a0-8b0f-4805-8706-392be1f252ec" ><br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/eec2cca8-4cb5-4790-873a-5263a6c57217" width="300" height="400">


Return to your administrator account, and go to the "Users" section. Normally, you can view your user account in this section and save the user's details.
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/c5a4d9a9-7dd8-448d-a40c-b1b6ec04536e"><br>
<br>

Go back to your user account and sign out, now you can sign in by scanning the QR Code.




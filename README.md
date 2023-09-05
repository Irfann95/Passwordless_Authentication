<h1>Tutorial : How to configure a Passwordless Authentification in Keycloak</h1>

<p>Keycloak is an open-source software devellopped by Redhat allowing to create an unique authentification method across identity and access management.In other words, this software allows the security of mobile et web aplications by managing users identity and by controling the ressources access. There are differents fonctionalitys in Keycloak such as management of users, authentification, authorization ant management of sessions for web and mobiles applications. Here, I will you show how to configure a passwordless authentification thanks to Keycloak </p>

<h2>Prerequisite</h2>
To configure a passwordless authentification, you have, of cource, to install Keyclaok. I send you an installation guide here:  https://www.keycloak.org/docs/18.0/server_installation/ 
Important: Install et set up the latest version of java is required.

<h2>Tutorial</h2>

Once installation is finish, you're supposed to be connected on Keycloak as an administrator and this menu supposed to be shown. <br>
<br>
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/0d807052-4630-4709-bc30-07fb712a460c" alt="Texte alternatif" width="800" height="400">

Then, you have to click on "master" and click "create realm". A realm is isolate space where you manage objects, including users, applications, roles, and groups. Then you can rename your realm.

<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/431a5118-1830-452d-b322-dd5fc27beab2" alt="Texte alternatif" width="300" height="200"><img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/dfad20f5-0d56-4765-9cfa-b8e13ade0b19" alt="Texte alternatif" width="350" height="200">

Once your realm created, click to "Authentification" in Configure Menu and click on browser file and duplicate this flow.
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/cfa0ffda-3135-480b-a768-f873742d5751" alt="Texte Alternatif" width="350" height="200">
<img src="https://github.com/Irfann95/Passwordless_Authentication/assets/142778082/ad1b683d-f15f-4e51-ac5e-950bbd07caf0" alt="Texte alternatif">



# ownCloud Quickstart 
### This guide includes selected highlights about preparing, installing, configuring, and managing users on your ownCloud Server.  Quickstart instructions about installing clients and connecting the clients to your organization's ownCloud server are also included in this guide.
## Preparing to Install Your ownCloud Server

You must install the ownCloud Server on one of the [officially supported Linux operating systems](https://doc.owncloud.org/server/latest/admin_manual/installation/system_requirements.html).  The installation environment must include Apache 2.4 web server, MySQL/MariaDB with InnoDB storage engine (MyISAM is not supported), and PHP 5.6 or later.  

The installation host must have command-line or Cron access.  It is preferable that your environment have both types of access.

A scale-out deployment, or federated cloud sharing, is recommended to ensure that ownCloud instances are kept to a managable size.
## ownCloud Server Installation
You can install your ownCloud server using:
- [Linux Package Manager](https://doc.owncloud.org/server/latest/admin_manual/installation/linux_installation.html) 
- [Source Tarball](https://doc.owncloud.org/server/latest/admin_manual/installation/source_installation.html)
- [Docker Image](https://doc.owncloud.org/server/latest/admin_manual/installation/docker/)
- [Appliance](%28https://doc.owncloud.org/server/latest/admin_manual/appliance/installation.html%29) 

## ownCloud Server  Configuration
There are many server and supporting application items which you must configure.  These include:
- [Database configuration](https://doc.owncloud.org/server/latest/admin_manual/configuration/database/)
- [File Sharing and Management](https://doc.owncloud.org/server/latest/admin_manual/configuration/files/)
- [LDAP Proxy-Cache Server Installation and Configuration](https://doc.owncloud.org/server/latest/admin_manual/configuration/ldap/ldap_proxy_cache_server_setup.html)
- [Mimetypes Management](https://doc.owncloud.org/server/latest/admin_manual/configuration/mimetypes/index.html)
- [Server Configuration](https://doc.owncloud.org/server/latest/admin_manual/configuration/server/index.html)

By default, your ownCloud server is configured under the route 
``/owncloud`` , using the default http port ``8080``.

The default is: 
``https://yourhostIP_or_name.com/owncloud``

You specify every URL (except the loopback address, which is whiteliested by default) that will used by users to access your ownCloud server in the the ``config.php`` file, under the ``trusted_domains`` setting.     

Users are allowed to log into your ownCloud server only when they point their browsers to a URL that is listed in the `trusted_domains` setting.

A typical ``trusted_domains`` configuration is like:
<code>
			'trusted_domains' => [
			 0 => 'localhost',
			 1 => 'yourserverIP_or_name.example.com',
			 2 => '192.168.1.11',
		],

## Adding User Accounts to the ownCloud Server
Add user accounts on the User Management page of your ownCloud User Interface, accessible by connecting to your ownCloud server and logging in with your administrator userID and password.

Create a new user account by:
- Entering the new user's Login Name and initial password
- Specifying any optional Groups memberships
- Clicking the Create button to complete user creation

See [User Management](https://doc.owncloud.org/server/10.0/admin_manual/configuration/user/) for complete details about user creation and management.
## Connecting to the ownCloud Server with Desktop and Mobile Clients
You can connect to your organization's ownCloud server using desktop (Windows, Mac, or Linux)  and mobile (IOS and Android) clients.  

All client installations require that you enter the information provided by your ownCloud administrator:

- The address of your organization's ownCloud server
- Your userID and password

Download the ownCloud Desktop clients [here.](https://owncloud.org/download/)  View the complete desktop client manual [here](https://doc.owncloud.org/desktop/latest/).
Download the ownCloud mobile clients from:

- [IOS App Store](https://itunes.apple.com/us/app/owncloud/id543672169?ls=1&mt=8)   
	- View the entire IOS App manual [here](https://doc.owncloud.org/ios/).
- [Google Play Store](https://play.google.com/store/apps/details?id=com.owncloud.android)  
	- View the entire Android App manual [here](https://doc.owncloud.org/android/).
     


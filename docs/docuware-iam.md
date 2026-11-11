# DocuWare for Docusign IAM

Learn how to install, configure, and use the **DocuWare Extension for Docusign** to connect your DocuWare environment with Docusign, retrieve document information, update index fields, and store signed documents.

## Overview

The DocuWare Extension for Docusign, developed by **ePillars Systems LLC**, integrates DocuWare document management with Docusign eSignature and Maestro workflows.

The integration enables users to:

- Connect DocuWare Cloud or supported on-premises environments to Docusign.
- Access DocuWare File Cabinets and retrieve document index information.
- Search and select existing DocuWare records.
- Create records and update document index fields through Docusign workflows.
- Store completed signed documents in DocuWare.
- Configure Private or Shared connections according to business requirements.

## How to Install and Configure

### Step 1: Locate the DocuWare App in Docusign App Center

In your Docusign account, navigate to **App Center** and search for **DocuWare** by ePillars Systems LLC.

![DocuWare app in Docusign App Center](docuwareasset/01-docuware-app-center.png)

Click **Install App**.

### Step 2: Connect Your DocuWare Account

1. After installing the application, open the DocuWare app from Docusign App Center.
2. Click **Connect Account**.

<img src="docuwareasset/02-connect-account.png" width="500" alt="Connect DocuWare account">

3. Review the authorization information and click **Install and Authorize**.

<img src="docuwareasset/03-install-and-authorize.png" width="500" alt="Install and authorize DocuWare extension">

### Step 3: Choose the Connection Type

Select the connection type that meets your organization's requirements.

<img src="docuwareasset/04-connection-type.png" width="500" alt="Choose Private or Shared DocuWare connection">

- **Private:** The connection is intended for the individual user.
- **Shared:** The connection can be shared with authorized users according to the available Docusign connection settings.

Choose **Private** or **Shared**, then click **Next**.

### Step 4: Name Your DocuWare Connection

Enter a meaningful name to identify the DocuWare connection.

<img src="docuwareasset/05-connection-name.png" width="500" alt="Name the DocuWare connection">

For example:

`DocuWare Production`

or

`DocuWare Test Environment`

Click **Login** to continue.

### Step 5: Enter Your DocuWare Connection Details

The DocuWare connection page will appear.

<img src="docuwareasset/06-docuware-login.png" width="500" alt="DocuWare connection login screen">

Enter the following information:

- **DocuWare Base URL:** Your DocuWare server address, for example, `https://company.docuware.cloud`.
- **Organization:** Your DocuWare organization name.
- **Username:** Your DocuWare user account.
- **Password:** The password associated with your DocuWare account.

Click **Connect Securely**.

The application validates the connection information before proceeding to the authorization screen.

### Step 6: Grant User Consent

After entering the DocuWare connection details, the authorization page appears.

<img src="docuwareasset/07-docuware-consent.png" width="500" alt="DocuWare OAuth authorization consent screen">

Review the displayed information:

- DocuWare Organization
- DocuWare Username
- Requested integration access

Click **Allow Access** to authorize the connection between Docusign and DocuWare.

After successful authorization, Docusign completes the connection process.

## How to Use the App

The DocuWare Extension supports data retrieval, record creation, index-field updates, and signed-document storage through its configured Docusign capabilities.

### 1. Read Data from DocuWare

In Docusign Maestro Workflow Builder:

1. Open your workflow.
2. Click **Add Step**.
3. Select **Read from DocuWare**.
4. Select your configured DocuWare connection.
5. Choose the required File Cabinet.
6. Configure the search criteria and select the document fields to retrieve.

The Read action can retrieve DocuWare index information for use in subsequent workflow steps.

For example, a workflow can search for a document using:

- Document ID
- Company
- Document Number
- Document Type
- Other searchable index fields configured in the File Cabinet

### 2. Create Records in DocuWare

Use **Writeback to DocuWare** to create a new record.

1. Click **Add Step** in Maestro Workflow Builder.
2. Select **Writeback to DocuWare**.
3. Select the DocuWare connection and File Cabinet.
4. Choose **Create**.
5. Select the DocuWare index fields to populate.
6. Map the fields to workflow data or enter the required values.
7. Save the step.

When the workflow executes successfully, the configured Create action submits the record information to DocuWare.

### 3. Update Existing DocuWare Index Fields

Use **Writeback to DocuWare → Update** to modify index fields on an existing document.

1. Add a **Writeback to DocuWare** step.
2. Select the DocuWare connection.
3. Choose the required File Cabinet.
4. Select **Update**.
5. Select the index fields to update.
6. Map each selected field to the required workflow value.
7. Configure a matching rule to identify the existing document.

**Example: Updating a document status**

- **File Cabinet:** Accounting
- **Field to update:** Status
- **New value:** Approved
- **Matching field:** Document ID
- **Operator:** Equal to
- **Workflow value:** Document ID of the existing DocuWare record

The matching value must identify the intended document. When using a dynamic workflow field, ensure that it contains a valid Document ID before the Writeback step executes.

Once the workflow completes successfully, the selected index fields are updated in DocuWare.

### 4. Store Signed Documents in DocuWare

The extension also includes a File Output capability for storing completed Docusign documents in DocuWare.

Depending on the configured workflow and extension capabilities, users can:

- Select a DocuWare destination.
- Store completed signed documents.
- Associate signed documents with existing DocuWare records.
- Maintain signed documents within the organization's document management environment.

Configure the destination and required document information in the relevant Docusign workflow or supported file-output process.

## Frequently Asked Questions

### Does the DocuWare Extension support DocuWare Cloud and on-premises installations?

The integration is designed to work with DocuWare Cloud and supported on-premises environments. Connectivity and authentication requirements may vary by deployment.

### Can multiple users connect using different DocuWare accounts?

Yes. The integration is designed to support separate DocuWare connections for different users and organizations, subject to the configured connection permissions.

### What is the difference between Private and Shared connections?

- **Private:** Intended for use by the individual connection owner.
- **Shared:** Allows the connection to be made available to other authorized users according to Docusign's connection-sharing settings.

### Is my DocuWare password stored by Docusign?

The extension uses an OAuth connection flow between Docusign and the ePillars integration service. The DocuWare credentials are submitted to the integration service over HTTPS for authentication.

Credential and token storage are managed according to the integration service's configured authentication and security implementation. Consult your administrator or ePillars support for deployment-specific storage details.

### Can I update existing DocuWare documents?

Yes. The **Writeback to DocuWare → Update** action can update supported document index fields when the workflow correctly identifies the existing document.

### Can I create new records in DocuWare?

Yes. The extension supports creating records through its configured Data IO Create action.

### Can I store completed Docusign documents in DocuWare?

Yes. The extension includes a File Output capability for storing completed signed documents in DocuWare, subject to the configured destination and workflow.

### How do I revoke access?

You can disconnect or remove the connection using the available Docusign App Center or connected-app management options.

Contact your administrator if you need to revoke associated integration access or credentials.

## Need Help or Custom Support?

If you encounter issues installing the DocuWare Extension, configuring authentication, creating workflows, updating index fields, or storing signed documents, contact the ePillars Systems support team.

- **Email Support:** [support@epillars.com](mailto:support@epillars.com)
- **Contact Portal:** [https://www.epillars.com/contact](https://www.epillars.com/contact)
- **Website:** [https://www.epillars.com](https://www.epillars.com)


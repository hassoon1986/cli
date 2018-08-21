---

copyright:

  years: 2018


lastupdated: "2018-08-20"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# Managing Accounts, Users, and Orgs
 {: #ibmcloud_commands_account}

<table summary="ibmcloud commands that you can use to manage accounts, orgs, spaces and roles.">
<caption>Table 1. Commands for managing accounts, orgs, spaces and roles</caption>
 <thead>
 <th colspan="5">Commands for managing accounts, orgs, spaces, and roles</th>
 </thead>
 <tbody>
 <tr>
 <td>[ibmcloud account orgs](cli_acct_org_role.html#ibmcloud_account_orgs)</td>
 <td>[ibmcloud account org](cli_acct_org_role.html#ibmcloud_account_org)</td>
 <td>[ibmcloud account org-create](cli_acct_org_role.html#ibmcloud_account_org_create)</td>
 <td>[ibmcloud account org-replicate](cli_acct_org_role.html#ibmcloud_account_org_replicate)</td>
 <td>[ibmcloud account org-rename](cli_acct_org_role.html#ibmcloud_account_org_rename)</td>
 </tr>
 <tr>
 <td>[ibmcloud account spaces](cli_acct_org_role.html#ibmcloud_account_spaces)</td>
 <td>[ibmcloud account space](cli_acct_org_role.html#ibmcloud_account_space)</td>
 <td>[ibmcloud account space-create](cli_acct_org_role.html#ibmcloud_account_space_create)</td>
 <td>[ibmcloud account space-rename](cli_acct_org_role.html#ibmcloud_account_space_rename)</td>
 <td>[ibmcloud account space-delete](cli_acct_org_role.html#ibmcloud_account_space_delete)</td>
 </tr>
 <tr>
 <td>[ibmcloud account org-users](cli_acct_org_role.html#ibmcloud_account_org_users)</td>
 <td>[ibmcloud account org-user-add](cli_acct_org_role.html#ibmcloud_account_org_user_add)</td>
 <td>[ibmcloud account org-user-remove](cli_acct_org_role.html#ibmcloud_account_org_user_remove)</td>
 <td>[ibmcloud account org-roles](cli_acct_org_role.html#ibmcloud_account_org_roles)</td>
 <td>[ibmcloud account org-role-set](cli_acct_org_role.html#ibmcloud_account_org_role_set)</td>
 </tr>
 <tr>
 <td>[ibmcloud account org-role-unset](cli_acct_org_role.html#ibmcloud_account_org_role_unset)</td>
 <td>[ibmcloud account space-users](cli_acct_org_role.html#ibmcloud_account_space_users)</td>
 <td>[ibmcloud account space-roles](cli_acct_org_role.html#ibmcloud_account_space_roles)</td>
 <td>[ibmcloud account space-role-set](cli_acct_org_role.html#ibmcloud_account_space_role_set)</td>
 <td>[ibmcloud account space-role-unset](cli_acct_org_role.html#ibmcloud_account_space_role_unset)</td>
</tr>
 <td>[ibmcloud account list](cli_acct_org_role.html#ibmcloud_account_list)</td>
 <td>[ibmcloud account org-account](cli_acct_org_role.html#ibmcloud_account_org_account)</td>
 <td>[ibmcloud account users](cli_acct_org_role.html#ibmcloud_account_users)</td>
 <td>[ibmcloud account user-remove](cli_acct_org_role.html#ibmcloud_account_user_remove)</td>
 <td>[ibmcloud account user-invite](cli_acct_org_role.html#ibmcloud_account_user_invite)</td>
 </tr>
 <tr>
  <td>[ibmcloud account user-reinvite](cli_acct_org_role.html#ibmcloud_account_user_reinvite)</td>
  <td>[ibmcloud app domain-cert](cli_acct_org_role.html#ibmcloud_app_domain_cert)</td>
  <td>[ibmcloud app domain-cert-add](cli_acct_org_role.html#ibmcloud_app_domain_cert_add)</td>
  <td>[ibmcloud app domain-cert-remove](cli_acct_org_role.html#ibmcloud_app_domain_cert_remove)</td>
 </tr>
 </tbody>
 </table>

 ### ibmcloud account orgs
{: #ibmcloud_account_orgs}

List all organizations

```
ibmcloud account orgs [-r REGION] [--guid]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>-r <i>REGION</i> (optional)</dt>
   <dd>For which region the organization information is shown. If set to 'all', all organizations in all regions are listed.</dd>
   <dt>--guid (optional)</dt>
   <dd>Display the GUID of the organizations.</dd>
   </dl>

<strong>Examples</strong>:

List all the organizations in region: `us-south` with the GUID displayed

```
ibmcloud account orgs -r us-south --guid
```

### ibmcloud account org
{: #ibmcloud_account_org}

Show the information for the specified organization.

```
ibmcloud account org ORG_NAME [--guid]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization.</dd>
   <dt>--guid (optional)</dt>
   <dd>Display the GUID of the organization.</dd>
   </dl>

<strong>Examples</strong>:

Show the information of organization `IBM` with the GUID displayed

```
ibmcloud account org IBM --guid
```

### ibmcloud account org-create
{: #ibmcloud_account_org_create}

Create a new organization. This operation can only be performed by account owner.

```
ibmcloud account org-create ORG_NAME [-f]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization being created.</dd>
   <dt>-f</dt>
   <dd>Force creation without confirmation.</dd>
   </dl>

<strong>Examples</strong>:

Create an organization named `IBM`.

```
ibmcloud account org-create IBM
```

### ibmcloud account org-replicate
{: #ibmcloud_account_org_replicate}

Replicate an org from the current region to another region.

```
ibmcloud account org-replicate ORG_NAME REGION_NAME
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the existing org that is to be replicated.</dd>
   <dt>REGION_NAME (required)</dt>
   <dd>The name of the region that hosts the replicated org.</dd>
   </dl>

<strong>Examples</strong>:

Replicate the org `myorg` to the region `eu-gb`:

```
ibmcloud account org-replicate myorg eu-gb
```

### ibmcloud account org-rename
{: #ibmcloud_account_org_rename}

Rename an organization. This operation can be done only by an org manager.

```
ibmcloud account org-rename OLD_ORG_NAME NEW_ORG_NAME
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>OLD_ORG_NAME (required)</dt>
   <dd>The old name of the org that is to be renamed.</dd>
   <dt>NEW_ORG_NAME (required)</dt>
   <dd>The new name of the org that it is renamed to.</dd>
   </dl>

### ibmcloud account spaces
{: #ibmcloud_account_spaces}

List all spaces

```
ibmcloud account spaces [-o ORG_NAME] [-r REGION-NAME]
```

<strong>Command options</strong>:
   <dl>
   <dt>-o</dt>
   <dd>Organization name. List the spaces under the organization specified. Default to current organization if not specified.</dd>
   <dt>-r</dt>
   <dd>Region name. List the spaces under the region specified. Default to current region if not specified.</dd>
   </dl>

### ibmcloud account space
{: #ibmcloud_account_space}

This command has the same function and options as the [cf space ![External link icon](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/space.html){: new_window} command.

### ibmcloud account space-create
{: #ibmcloud_account_space_create}

This command has the same function and options as the [cf create-space ![External link icon](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-space.html){: new_window} command.

### ibmcloud account space-rename
{: #ibmcloud_account_space_rename}


This command has the same function and options as the [cf rename-space ![External link icon](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/rename-space.html){: new_window} command.

### ibmcloud account space-delete
{: #ibmcloud_account_space_delete}


This command has the same function and options as the [cf delete-space ![External link icon](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-space.html){: new_window} command.

### ibmcloud account org-users
{: #ibmcloud_account_org_users}

Display users in the specified organization by role.

```
ibmcloud account org-users ORG_NAME [-a]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>ORG_NAME (required)</dt>
<dd>The name of the organization.</dd>
<dt>-a (optional)</dt>
<dd>List all the users in the specified organization, not grouped by role.</dd>
</dl>

### ibmcloud account org-user-add
{: #ibmcloud_account_org_user_add}

Add a user into org (org manager required).

```
 ibmcloud account org-user-add USER_NAME ORG
```

### ibmcloud account org-user-remove
{: #ibmcloud_account_org_user_remove}

Remove a user from org (org manager or user him/herself only)

```
   ibmcloud account org-user-remove USER_NAME ORG [-f, --force]
```

<strong>Command options</strong>:
<dl>
<dt>--force, -f</dt>
<dd>Force deletion without confirmation.</dd>
</dl>

### ibmcloud account org-roles
{: #ibmcloud_account_org_roles}

Get all organization roles of the current user

```
ibmcloud account org-roles [-u USER_ID]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
  <dl>
   <dt>-u</dt>
   <dd>User ID. If not specified, default to current user.</dd>
  </dl>

### ibmcloud account org-role-set
{: #ibmcloud_account_org_role_set}

Assign an organization role to a user. This operation can be performed only by an organization manager.

```
ibmcloud account org-role-set USER_NAME ORG_NAME ORG_ROLE
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
  <dl>
   <dt>USER_NAME (required)</dt>
   <dd>The name of the user being assigned.</dd>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization this user is assigned to.</dd>
   <dt>ORG_ROLE (required)</dt>
   <dd>The name of the organization role this user is assigned to. For example:
   <ul>
   <li>OrgManager: This role can invite and manage users, select and change plans, and set spending limits.</li>
   <li>BillingManager: This role can create and manage the billing account and payment information.</li>
   <li>OrgAuditor: This role has read-only access to org information and reports.</li>
   </ul>
   </dd>
  </dl>

<strong>Examples</strong>:

Assign user `Mary` to the organization `IBM` as `OrgManager` role:

```
ibmcloud account org-role-set Mary IBM OrgManager
```
<!-- Begin Staging URL vs Prod URL -->
**Note**: You can set org/space roles using the CLI, but if you want to set the other permissions, you have to use the UI. For further details, see [Assigning user access](/docs/iam/assignaccess.html#assignaccess).
<!-- Begin Staging URL vs Prod URL -->

### ibmcloud account org-role-unset
{: #ibmcloud_account_org_role_unset}

Remove an organization role from a user. This operation can be performed only by an organization manager.

```
ibmcloud account org-role-unset USER_NAME ORG_NAME ORG_ROLE
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>USER_NAME (required)</dt>
   <dd>The name of the user being removed.</dd>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization this user is removed from.</dd>
   <dt>ORG_ROLE (required)</dt>
   <dd>The name of the organization role this user is removed from. For example:
   <ul>
   <li>OrgManager: This role can invite and manage users, select and change plans, and set spending limits.</li>
   <li>BillingManager: This role can create and manage the billing account and payment information.</li>
   <li>OrgAuditor: This role has read-only access to org information and reports.</li>
   </ul>
   </dd>
    </dl>

<strong>Examples</strong>:

Remove user `Mary` from the organization `IBM` as `OrgManager` role:

```
ibmcloud account org-role-unset Mary IBM OrgManager
```

### ibmcloud account space-users
{: #ibmcloud_account_space_users}

Display users in the specified space by role.

```
ibmcloud account space-users ORG_NAME SPACE_NAME
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
   <dl>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization.</dd>
   <dt>SPACE_NAME (required)</dt>
   <dd>The name of the space.</dd>
   </dl>

### ibmcloud account space-role-set
{: #ibmcloud_account_space_role_set}

Assign a space role to a user. This operation can be performed only by a space manager.

```
ibmcloud account space-role-set USER_NAME ORG_NAME SPACE_NAME SPACE_ROLE
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:

   <dl>
   <dt>USER_NAME (required)</dt>
   <dd>The name of the user being assigned.</dd>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization this user is assigned to.</dd>
   <dt>SPACE_NAME (required)</dt>
   <dd>The name of the space this user is assigned to.</dd>
   <dt>SPACE_ROLE (required)</dt>
   <dd>The name of the space role this user is assigned to. For example:
   <ul>
   <li>SpaceManager: This role can invite and manage users, and enable features for a given space.</li>
   <li>SpaceDeveloper: This role can create and manage apps and services, and see logs and reports.</li>
   <li>SpaceAuditor: This role can view logs, reports, and settings for the space.</li>
   </ul></dd>
    </dl>

<strong>Examples</strong>:

Assign user `Mary` to the organization `IBM` and space `Cloud` as `SpaceManager` role:

```
ibmcloud account space-role-set Mary IBM Cloud SpaceManager
```

### ibmcloud account space-role-unset
{: #ibmcloud_account_space_role_unset}

Remove a space role from a user. This operation can be performed only by a space manager.

```
ibmcloud account space-role-unset USER_NAME ORG_NAME SPACE_NAME SPACE_ROLE
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:

   <dl>
   <dt>USER_NAME (required)</dt>
   <dd>The name of the user being removed.</dd>
   <dt>ORG_NAME (required)</dt>
   <dd>The name of the organization this user is removed from.</dd>
   <dt>SPACE_NAME (required)</dt>
   <dd>The name of the space this user is removed from.</dd>
   <dt>SPACE_ROLE (required)</dt>
   <dd>The name of the space role this user is removed from. For example:
   <ul>
   <li>SpaceManager: This role can invite and manage users, and enable features for a given space.</li>
   <li>SpaceDeveloper: This role can create and manage apps and services, and see logs and reports.</li>
   <li>SpaceAuditor: This role can view logs, reports, and settings for the space.</li>
   </ul></dd>
    </dl>


<strong>Examples</strong>:

Remove user `Mary` from the organization `IBM` and space `Cloud` as `SpaceManager` role:

```
ibmcloud account space-role-unset Mary IBM Cloud SpaceManager
```

### ibmcloud account list
{: #ibmcloud_account_list}

List all accounts of the current user

```
ibmcloud account list
```

<strong>Prerequisites</strong>:  Endpoint, Login

### ibmcloud account org-account
{: #ibmcloud_account_org_account}

Display the account of specified organization(org user required)

```
ibmcloud account org-account ORG_NAME [--guid]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
  <dt>--guid (optional)</dt>
  <dd>Display account ID only</dd>
</dl>

### ibmcloud account users
{: #ibmcloud_account_users}

Displays users associated with the account. This operation can be performed only by the account owner.

```
ibmcloud account users
```

### ibmcloud account user-remove
{: #ibmcloud_account_user_remove}

Remove a user from an account(account owner only)

```
ibmcloud account user-remove USER_ID [-c ACCOUNT_ID] [-f, --force]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>USER_ID (required)</dt>
<dd>User id</dd>
<dt>-c ACCOUNT_ID</dt>
<dd>Account ID. If not specified, default to current account.</dd>
<dt>-f, --force</dt>
<dd>Force removal without confirmation.</dd>
</dl>

### ibmcloud account user-invite
{: #ibmcloud_account_user_invite}

Invite a user to the account

```
ibmcloud account user-invite USER_EMAIL [-o ORG [--org-role ORG_ROLE] [-s SPACE, --space-role SPACE_ROLE]]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
   <dt>USER_EMAIL (required)</dt>
   <dd>The email of the user being invited.</dd>
   <dt>-o ORG</dt>
   <dd>Organization to invite user to</dd>
   <dt>--org-role ORG_ROLE</dt>
   <dd>Organization role. Valid inputs are: OrgManager, BillingManager, OrgAuditor and OrgUser. If omitted, the OrgUser role will be set.</dd>
   <dt>-s SPACE</dt>
   <dd>Space to invite user to</dd>
   <dt>--space-role SPACE_ROLE</dt>
   <dd>Space role. Valid inputs are: SpaceManager, SpaceDeveloper and SpaceAuditor.</dd>
</dl>

### ibmcloud account user-reinvite
{: #ibmcloud_account_user_reinvite}

Resend invitation to a user (account admin)

```
ibmcloud account user-reinvite USER_EMAIL
```
<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
   <dt>USER_EMAIL (required)</dt>
   <dd>The email of the user being re-invited.</dd>
</dl>

### ibmcloud app domain-cert
{: #ibmcloud_app_domain_cert}

List the certificate information of a domain.

```
ibmcloud app domain-cert DOMAIN_NAME
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>DOMAIN_NAME (required)</dt>
<dd>The domain that hosts the certificate.</dd>
</dl>


<strong>Examples</strong>:

View the certificate information of the domain `ibmcxo-eventconnect.com`:

```
ibmcloud app domain-cert ibmcxo-eventconnect.com
```

### ibmcloud app domain-cert-add
{: #ibmcloud_app_domain_cert_add}

Add a certificate to the specified domain in the current org.

```
ibmcloud app domain-cert-add DOMAIN -k PRIVATE_KEY_FILE -c CERT_FILE [-p PASSWORD] [-i INTERMEDIATE_CERT_FILE] [-t TRUST_STORE_FILE]
```

<strong>Prerequisites</strong>:  Endpoint, Login, Target

<strong>Command options</strong>:
   <dl>
   <dt>DOMAIN (required)</dt>
   <dd>The domain that the certificate is added to.</dd>
   <dt>-k <i>PRIVATE_KEY_FILE</i> (required)</dt>
   <dd>The private key file path.</dd>
   <dt>-c <i>CERT_FILE</i> (required)</dt>
   <dd>The certificate file path.</dd>
   <dt>-p <i>PASSWORD</i> (optional)</dt>
   <dd>The password for the certificate.</dd>
   <dt>-i <i>INTERMEDIATE_CERT_FILE</i> (optional)</dt>
   <dd>The intermediate certificate file path.</dd>
   <dt>-t <i>TRUST_STORE_FILE</i> (optional)</dt>
   <dd>The trust store file.</dd>
   </dl>


<strong>Examples</strong>:

Add a certificate to the domain `ibmcxo-eventconnect.com`:

```
ibmcloud app domain-cert-add ibmcxo-eventconnect.com -k key_file.key -c cert_file.crt -p 123 -i inter_cert.cert
```

### ibmcloud app domain-cert-remove
{: #ibmcloud_app_domain_cert_remove}

Remove a certificate from the specified domain in current org.

```
ibmcloud app domain-cert-remove DOMAIN [-f]
```

<strong>Prerequisites</strong>:  Endpoint, Login, Target

<strong>Command options</strong>:

   <dl>
   <dt>DOMAIN (required)</dt>
   <dd>Domain to remove the certificate from.</dd>
   <dt>-f  (optional)</dt>
   <dd>Force deletion without confirmation.</dd>
   </dl>
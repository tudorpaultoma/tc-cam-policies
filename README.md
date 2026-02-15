# Administrator CAM Policy - Restricted User/Group Management

## Purpose
Grants full access to all Tencent Cloud services while preventing modifications to CAM users and groups.

## Scope

### ✅ Allowed Operations
- Full access to all Tencent Cloud services and resources
- Service role creation and management (e.g., TKE accessing TCR)
- Custom policy creation and management
- Read/view access to CAM users and groups
- Attaching policies to service roles

### ❌ Denied Operations
- Creating, deleting, or modifying CAM users
- Creating, deleting, or modifying CAM groups
- Attaching or detaching policies to/from users and groups
- Managing user access keys
- Managing SAML providers and configurations

## Use Case
Ideal for delegated administrators who need to manage infrastructure and services but should not alter IAM user/group permissions.

## File
- `full-admin-no-cam.json` - The CAM policy ready to be imported into Tencent Cloud Console

## How to Use
1. Log in to Tencent Cloud Console
2. Navigate to **CAM → Policies → Create Custom Policy → By Policy Syntax**
3. Copy and paste the contents of `full-admin-no-cam.json`
4. Attach the policy to the desired CAM group

## Example Scenario
A user with this policy can:
- Create a TKE cluster
- Create a service role for the TKE cluster to access TCR
- Attach the appropriate TCR access policy to the role

But **cannot**:
- Add or remove users from CAM groups
- Change group policy attachments
- Create or modify CAM users

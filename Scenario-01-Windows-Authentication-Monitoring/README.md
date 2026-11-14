
## Evidence and Investigation Results

### 1. Windows Audit Policy Configuration

The Windows audit policy subcategory override was enabled to ensure advanced audit policies take precedence.

![Audit Policy Override](Evidence/01-audit-policy-subcategory-override.png)

### 2. Account Logon Auditing

Credential Validation and Other Account Logon Events were configured for Success and Failure auditing.

![Account Logon Audit Policy](Evidence/02-account-logon-audit-policy.png)

### 3. Test Account Configuration

The `soc_lab` account was verified as a standard user belonging to the Users group.

![SOC Lab Account](Evidence/03-soc-lab-account-membership.png)

### 4. Windows Successful Authentication Event

Windows Event ID 4624 was generated and investigated. The event confirmed a successful interactive login.

![Windows Event 4624](Evidence/04-windows-event-4624-xml.png)

### 5. Wazuh Event Collection

The corresponding Windows authentication event was successfully collected and indexed by Wazuh.

![Wazuh Event 4624](Evidence/05-wazuh-event-4624.png)

### 6. Wazuh Detection Rule

Wazuh matched the event against Rule ID 60118, identifying it as a Windows workstation logon success.

![Wazuh Rule 60118](Evidence/06-wazuh-rule-60118.png)

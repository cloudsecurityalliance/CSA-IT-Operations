# Threat model for airtable.com

Original map as PNG (from Miro)

```mermaid
graph LR

SSO -->|prevents|AccountHijackingAccount_Hijacking[Account_Hijacking]
Account_Hijacking -->|results_in|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]
Account_Hijacking -->|results_in|Export_of_sensitive_data[Export_of_sensitive_data]

Alteration_or_deletion_of_data -->|compromises|Airtable_Data[Airtable_Data]
Export_of_sensitive_data -->|compromises|Airtable_Data[Airtable_Data]

User_Education -->|prevents|Accidental_Misuse[Accidental_Misuse]
Accidental_Misuse -->|results_in|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]
Accidental_Misuse -->|results_in|Export_of_sensitive_data[Export_of_sensitive_data]

Attacker_Breaks_Into_Airtable -->|results_in|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]
Attacker_Breaks_Into_Airtable -->|results_in|Export_of_sensitive_data[Export_of_sensitive_data]

Least_privilege_model -->|prevents|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]
Least_privilege_model -->|prevents|Export_of_sensitive_data[Export_of_sensitive_data]
Least_privilege_model -->|prevents|Accidental_Misuse[Accidental_Misuse]

Log_monitoring -->|detects|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]
Backups -->|remediate|Alteration_or_deletion_of_data[Alteration_or_deletion_of_data]

Airtable_defaults_to_open -->|prevents|Least_privilege_model[Least_privilege_model]
Least_privilege_model -->|prevents|Sharing_and_adhoc_workgroups[Sharing_and_adhoc_workgroups]

Airtable_culture_of_sharing -->|enables|Sharing_and_adhoc_workgroups[Sharing_and_adhoc_workgroups]
Airtable_culture_of_sharing -->|prevents|Least_privilege_model[Least_privilege_model]
```

# What we've learned from the threat model

## We can secure our accounts by using SSO

## We can recover data as we have backups

## We can detect alterations/deletions via logs

But this would require a massive amount of time, or buying some technology and tuning it, seeing as how we have logs and backups we can retroactively handle this. 

## User education

## Airtable can be made secure but this will impact functionality

Airtable is designed to support and enable adhoc work/groups/mashups with access to data across groups. In general the product has made choices that prize collaboration and adhoc data sharing over security. You can lock it down with a least privilege model but this will heavily impact the usability.


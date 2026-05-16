### Overview
A sophisticated multi-stage attack against a hospital network resulted in patient data exfiltration and full ransomware deployment. The attacker leveraged a phishing campaign, CobaltStrike C2 infrastructure, and lateral movement through privileged credentials to ultimately compromise a Senior IT Administrator account.

### Attack Timeline

```
May 1, 2024      → First machine (RQJQ-MACHINE) compromised via phishing
May 14, 2024     → Attacker establishes C2 via CobaltStrike (93.238.22.122)
June 17, 2024    → Credential theft; lateral movement to andavis (IT Admin)
13:35 UTC        → lockbyte_ransomer.exe copied to network share
14:22 UTC        → patient_data_exporter.exe downloaded
14:23 UTC        → Patient records exported from hospital server
17:18 UTC        → Stolen data uploaded to secure-health-access.com
17:36 UTC        → Evidence deletion (del patient_data_*.zip)
14:49 UTC        → Ransom note discovered: We_Have_Your_Data_Pay_Up.txt
```

### Infection Chain

```
Malicious Ad (raisinkanes.com)
        ↓
Redirect: nothing-to-see-here.net
        ↓
Redirect: totally-legit-domain.com
        ↓
Phishing Payload: Raisin_Kane_Promo_Offer.docx / Raisin_Kane_Free_Meal_Voucher.pdf
        ↓
Dropped: cobaltstrike.exe (RQJQ-MACHINE / user: evbrowne)
        ↓
C2 Beacon → 93.238.22.122
        ↓
Recon: advanced-ip-scanner.exe
        ↓
Exfil: network_diagrams.pdf, credentials.txt, important_network_info.zip
        ↓
Lateral movement → AMFB-MACHINE (andavis / Senior IT Admin)
        ↓
Deploy: lockbyte_ransomer.exe → \\jojos-hospital.org\shared\spread_ransomware.exe
        ↓
Exfil: patient_data_1.zip → https://secure-health-access.com/upload/
        ↓
Cover tracks: del patient_data_*.zip
        ↓
Ransom dropped: We_Have_Your_Data_Pay_Up.txt
```

### Indicators of Compromise (IOCs)

| Type | Value |
|------|-------|
| Attacker IPs | `203.0.113.1`, `203.0.113.2` |
| C2 IP | `93.238.22.122` |
| Malicious Domains | `secure-health-access.com`, `emr-help.net`, `raisinkanes.com`, `nothing-to-see-here.net`, `totally-legit-domain.com` |
| File Hashes (SHA256) | `97c348e95c8a8aeb8808f76434d73a92bbcb6b4586788365762b22624990b018` (ransom note) |
| Process Hash | `0d663ea9485770015ce187c5796b5e171bcf4b14d48175e7189a3456ccd8cb16` (patient_data_exporter.exe) |
| Malicious Executables | `lockbyte_ransomer.exe`, `patient_data_exporter.exe`, `cobaltstrike.exe`, `advanced-ip-scanner.exe` |
| Compromised Account | `andavis` — `anthony_davis@jojoshospital.org` (Senior IT Administrator) |
| Password Hash | `a9fbcdd6b449063a2ff822ea7d266402` |

### Tools & Techniques (MITRE ATT&CK)

| Technique | ID | Tool Used |
|-----------|-----|-----------|
| Phishing: Spearphishing Link | T1566.002 | Malicious .docx / .pdf lures |
| Command & Control | T1219 | CobaltStrike (cobaltstrike.exe) |
| Discovery — Network Scanning | T1046 | advanced-ip-scanner.exe |
| Lateral Movement | T1021 | Stolen admin credentials |
| Exfiltration Over Web Service | T1567 | curl + secure-health-access.com |
| Data Encrypted for Impact | T1486 | lockbyte_ransomer.exe |
| Indicator Removal | T1070.004 | `del patient_data_*.zip` |

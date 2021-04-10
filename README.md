# Restrictive DMARC Record

### Example:
```
v=DMARC1;p=reject;pct=100;fo=1;adkim=s;aspf=s;rua=mailto:dmarc@example.com;ruf=mailto:dmarc@example.com
```
### Explanation:

|Tag|Required|Explanation|Example|Rationale|
|---|---|---|---|---|
|v|yes|protocol version|v=DMARC1|Protocol version must be specified|
|p|yes|domain policy|p=reject|DMARC failures should result in email rejection|
|pct|no|percentage of emails filtered|pct=100|All emails should be filtered|
|fo|no|generate failure report if either SPF or DKIM are not aligned|fo=1|The misalignment of either SPF or DKIM should generate a failure report|
|adkim|no|DKIM alignment|adkim=s|DKIM misalignment should result in a failure|
|aspf|no|SPF alignment|aspf=s|SPF misalignment should result in a failure|
|rua|no|aggregate report address|rua=mailto:dmarc@example.com|DMARC reports should be directed to a specific mailbox and reviewed|
|ruf|no|forensic report address|ruf=mailto:dmarc@example.com|DMARC reports should be directed to a specific mailbox and reviewed|

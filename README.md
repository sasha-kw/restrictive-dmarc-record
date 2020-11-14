# restrictive-dmarc-record

### Example:
```
v=DMARC1;p=reject;pct=100;fo=1;adkim=s;aspf=s;rua=mailto:dmarc@example.com;ruf=mailto:dmarc@example.com
```
### Explanation:

|tag|required|explanation|example|rationale|
|---|---|---|---|---|
|v|yes|protocol version|v=DMARC1|required|
|p|yes|domain policy|p=reject|required|
|pct|no|percentage of emails filtered|pct=100|TODO|
|fo|no|generate failure report if either SPF or DKIM are not aligned|fo=1|TODO|
|adkim|no|dkim alignment|adkim=s|TODO|
|aspf|no|spf alignment|spf=s|TODO|
|rua|no|aggregate report address|rua=mailto:dmarc@example.com|TODO|
|ruf|no|forensic report address|ruf=mailto:dmarc@example.com|TODO|

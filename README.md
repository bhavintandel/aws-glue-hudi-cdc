# aws-glue-hudi-cdc

Repository to deploy sample pipeline which demonstrate CDC using AWS Glue 


## Get from github

```python
import os
import urllib3

http = urllib3.PoolManager()

r = http.request('GET', 'https://github.com/bhavintandel/aws-glue-hudi-cdc/archive/main.zip')

filename = os.path.join(os.getcwd(), 'repo.zip')
with open(filename, 'wb') as f:
    f.write(r.content)

import zipfile

zip = zipfile.ZipFile(filename)
print (zip.namelist())
```

## Bibliography

* https://aws.amazon.com/blogs/big-data/writing-to-apache-hudi-tables-using-aws-glue-connector/

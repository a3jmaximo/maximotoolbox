# Automation Script: Set the PM Description Upon Save

## Busness Scenario: 
### Create a standard and predictable descriptions when a PM record is saved.  This will ensure uniform descriptions across all PM records.

## Author: A3J Group info@a3jgroup.com

### Script name is PM.SAVE and is called when PM record is saved.

```markdown
from psdi.mbo import MboConstants
if mbo.isNull('ASSETNUM'):
    mbo.setValue('DESCRIPTION',mbo.getString('WORKTYPE') + " " + mbo.getString("LOCATION"),MboConstants.NOACCESSCHECK)
else:
    mbo.setValue('DESCRIPTION',mbo.getString('WORKTYPE') + " " + mbo.getString("ASSETNUM"),MboConstants.NOACCESSCHECK)

```

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

# Summary

This module looks through the org's standardized deployment collections, notes the deployments, and reports any deployments of the same apps which are directly deployed to other collections, and which collections. The idea is to limit the number of duplicated one-off deployments, to limit the overall number of deployments and thus limit time spent troubleshooting broken deployments.  

# Org-specific warning
Note: this module is currently written specifically for use in the College of Engineering of the University of Illinois. It's published mostly for reference and requires refactoring for use in other organizations.  

### Example usage

1. Download `Report-UnnecessaryDirectDeployments.psm1` to `$HOME\Documents\WindowsPowerShell\Modules\Report-UnnecessaryDirectDeployments\Report-UnnecessaryDirectDeployments.psm1`.
2. Run it.
  - e.g. `Report-UnnecessaryDirectDeployments`
3. Review the generated CSV.

### Parameters

#### -OutputPath
Optional string.  
The location where the log and generated CSV will be created.  
Default path is `c:\engrit\logs`.  
Output filenames are `Report-UnnecessaryDirectDeployments_<timestamp>.csv/log`.  

#### -SiteCode
Optional string. Recommend leaving default.  
The site code of the MECM site to query.  
Default is `MP0`.  

#### -Provider
Optional string. Recommend leaving default.  
The SMS provider machine name.  
Default is `sccmcas.ad.uillinois.edu`.  

#### -CMPSModulePath
Optional string. Recommend leaving default.  
The path to the ConfigurationManager Powershell module installed on the local machine (as part of the admin console).  
Default is `$($ENV:SMS_ADMIN_UI_PATH)\..\ConfigurationManager.psd1`.  

# Notes
- By mseng3. See my other projects here: https://github.com/mmseng/code-compendium.

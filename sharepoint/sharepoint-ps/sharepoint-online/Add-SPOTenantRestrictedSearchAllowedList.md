---
external help file: sharepointonline.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spotenantrestrictedsearchallowedlist
applicable: SharePoint Online
title: Add-SPOTenantRestrictedSearchAllowedList
schema: 2.0.0
author: praporwal-microsoft
ms.author: praporwal
ms.reviewer:
---

# Add-SPOTenantRestrictedSearchAllowedList

## SYNOPSIS

Adds a list of sites to the restricted search allowed list.

## SYNTAX

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesList <List[string]> [<CommonParameters>]
```

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl <string> [-ContainsHeader <bool>] [<CommonParameters>]
```

## DESCRIPTION

Restricted SharePoint search gives Global and SharePoint Administrators the ability to enable or disable organization-wide search. When enabled, this control offers up to 100 sites to be included in organization-wide search, including user's previously accessed files and content from user's frequent sites. The allow list is a set of curated sites where the administrator has reviewed the permissions and applied data governance to them. The allow list supports sites, hub sites and communication sites.

## EXAMPLES

### EXAMPLE 1

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesList @("https://contoso.sharepoint.com/sites/Marketing", "https://contoso.sharepoint.com/sites/Benefits")
```

This example lets the administrator add the given sites to the allowed list.

### EXAMPLE 2

```powershell
Add-SPOTenantRestrictedSearchAllowedList -SitesListFileUrl .\AllowList.csv
```

This example lets the administrator add sites to the allowed list by giving a CSV file containing the list of site URLs.

## PARAMETERS

### -SitesList

List of allowed sites.

```yaml
Type: String[]
Parameter Sets: SitesList
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SitesListFileUrl

File that has the list of site URLs that can be added to an allowed list when the tenant is set to restricted tenant search mode. Below is a sample input file containing site URLs without header.

```console
https://contosomarketing.sharepoint.com/sites/CommunicationSite
https://contosomarketing.sharepoint.com/sites/Finance
https://contosomarketing.sharepoint.com/sites/Marketing
https://contosomarketing.sharepoint.com/sites/TestSite
```

```yaml
Type: String
Parameter Sets: SitesListFileUrl
Applicable: SharePoint Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainsHeader

Indicates whether the given CSV file contains header. If set to True, the first row in the file will be treated as the header and will be skipped.

```yaml
Type: Boolean
Parameter Sets: SitesListFileUrl
Applicable: SharePoint Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## RELATED LINKS

[Get-SPOTenantRestrictedSearchMode](Get-SPOTenantRestrictedSearchMode.md)

[Set-SPOTenantRestrictedSearchMode](Set-SPOTenantRestrictedSearchMode.md)

[Get-SPOTenantRestrictedSearchAllowedList](Get-SPOTenantRestrictedSearchAllowedList.md)

[Remove-SPOTenantRestrictedSearchAllowedList](Remove-SPOTenantRestrictedSearchAllowedList.md)

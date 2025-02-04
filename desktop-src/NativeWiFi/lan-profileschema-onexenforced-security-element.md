---
title: OneXEnforced (security) element
description: Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.
ms.topic: reference
ms.date: 06/20/2023
topic_type: 
- APIRef
- kbSyntax
api_name: 
- OneXEnforced
api_type: 
- Schema
api_location: 
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
---

# OneXEnforced (security) Element

The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication. When **OneXEnforced** is `TRUE`, the automatic configuration service must use 802.1X for port authentication. When **OneXEnforced** is `FALSE`, the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.

This element is optional. The default value is `FALSE`.

This element has a meaningful value only if [**OneXEnabled**](lan-profileschema-security-msm-element.md#onexenabled) is `TRUE`. If **OneXEnabled** is `FALSE`, then the value of this element is ignored.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.

## Requirements

| Requirement | Value |
|-------------------------------------|------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>       |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/> |

## See also

<dl> <dt>

**Definition context of element in schema**
</dt> <dt>

[**security**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Possible immediate parent element in schema instance**
</dt> <dt>

[**security (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

---
author: swapnil1993
ms.author: swapnil1993
title: "ContentType AddCopy"
description: "Add copy of site content type to a list"
localization_priority: Normal
doc_type: apiPageType
ms.prod: "sharepoint"
---

# Add copy of site content type to a list

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]
Add copy of [site][site] [content type][contentType]  to a [list][list].
 
  

## Permissions  

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions_reference.md).

  

|Permission type | Permissions (from least to most privileged) |

|:--------------------|:---------------------------------------------------------|

|Delegated (work or school account) | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All  |

|Delegated (personal Microsoft account) | Not supported. |

|Application | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All |

  

## HTTP request
<!-- {
  "blockType": "ignored"
}
-->
```http

POST /sites/{site-id}/lists/{list-id}/contentTypes/addCopy
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Parameter|Type|Required|Description|
|-|-|-|-|
|contentType| string | Yes| Canonical url to the site content type whose copy will be added to the list|

## Response

If successful, this call returns a `204 No Content` response

## Example

### Request
<!-- {
  "blockType": "request",
  "name": "contenttype_addcopy"
}
-->
```http
https://graph.microsoft.com/beta/sites/id/lists/{list-id}/contentTypes/addCopy
Content-Type: application/json

{
  "contentType": "https://graph.microsoft.com/beta/sites/id/contentTypes/0x0101"
}
```



### Response


<!-- { "blockType": "response" } -->

```http

HTTP/1.1 204 No Content

```

[site]: ../resources/site.md
[list]: ../resources/list.md
[contentType]: ../resources/contentType.md
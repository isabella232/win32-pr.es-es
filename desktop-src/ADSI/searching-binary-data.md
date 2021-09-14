---
title: Buscar datos binarios
description: Aunque la característica de búsqueda ADSI solo admite la búsqueda de datos de cadena, es posible buscar datos binarios.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Búsqueda de ADSI de datos binarios
- ADSI de datos binarios
- ADSI de datos binarios, buscar datos binarios
- ADSI ADSI, código de ejemplo C/C++, búsqueda de datos binarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172153"
---
# <a name="searching-binary-data"></a>Buscar datos binarios

Aunque la característica de búsqueda ADSI solo admite la búsqueda de datos de cadena, es posible buscar datos binarios. Para ello, use la función [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) para convertir los datos binarios en una cadena que se pueda usar con los métodos de búsqueda. La búsqueda de datos binarios es especialmente útil al buscar un GUID o un SID porque estos tipos de datos se almacenan como datos binarios.

Cuando se usa [**la función ADsEncodeBinaryData,**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) la memoria asignada se debe liberar mediante la [**función FreeADsMem.**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)

En el siguiente ejemplo de código de C++ se muestra cómo compilar una cadena de consulta para buscar un objeto que tiene un valor **objectGUID** determinado.


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 





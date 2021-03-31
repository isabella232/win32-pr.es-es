---
title: Buscar datos binarios
description: Aunque la característica de búsqueda ADSI solo admite la búsqueda de datos de cadena, es posible buscar datos binarios.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Búsqueda de datos binarios ADSI
- Datos binarios ADSI
- Datos binarios ADSI, buscar datos binarios
- ADSI ADSI, código de ejemplo C/C++, buscar datos binarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075065"
---
# <a name="searching-binary-data"></a><span data-ttu-id="bf1f6-107">Buscar datos binarios</span><span class="sxs-lookup"><span data-stu-id="bf1f6-107">Searching Binary Data</span></span>

<span data-ttu-id="bf1f6-108">Aunque la característica de búsqueda ADSI solo admite la búsqueda de datos de cadena, es posible buscar datos binarios.</span><span class="sxs-lookup"><span data-stu-id="bf1f6-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="bf1f6-109">Para ello, utilice la función [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) para convertir los datos binarios en una cadena que se puede utilizar con los métodos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bf1f6-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="bf1f6-110">La búsqueda de datos binarios es especialmente útil al buscar un GUID o SID porque estos tipos de datos se almacenan como datos binarios.</span><span class="sxs-lookup"><span data-stu-id="bf1f6-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="bf1f6-111">Cuando se usa la función [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , la memoria asignada se debe liberar mediante la función [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="bf1f6-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="bf1f6-112">En el ejemplo de código de C++ siguiente se muestra cómo crear una cadena de consulta para buscar un objeto que tiene un valor **objectGUID** determinado.</span><span class="sxs-lookup"><span data-stu-id="bf1f6-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


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



 

 





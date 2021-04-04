---
title: Código de ejemplo para crear una representación de cadena enlazable de un GUID
description: El siguiente ejemplo de código se puede utilizar para devolver una representación de cadena de un GUID que se puede utilizar para enlazar con el objeto.
ms.assetid: e39a6994-4328-40f2-8cb5-8b1f971e50d8
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, crear una representación de cadena enlazable de un GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6614ebeaf1028452ba75c0fc5dbaffb364e1ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075132"
---
# <a name="example-code-for-creating-a-bindable-string-representation-of-a-guid"></a><span data-ttu-id="02472-104">Código de ejemplo para crear una representación de cadena enlazable de un GUID</span><span class="sxs-lookup"><span data-stu-id="02472-104">Example Code for Creating a Bindable String Representation of a GUID</span></span>

<span data-ttu-id="02472-105">El siguiente ejemplo de código se puede utilizar para devolver una representación de cadena de un GUID que se puede utilizar para enlazar con el objeto.</span><span class="sxs-lookup"><span data-stu-id="02472-105">The following code example can be used to return a string representation of a GUID that can be used to bind to the object.</span></span>


```C++
//*******************************************************************
//
//  GUIDtoBindableString()
//
//  Converts a GUID into a string that can be used for binding with  
//  the <GUID= or <WKGUID= syntax. The caller must free the allocated  
//  string with the FreeADsStr when it is no longer required.
//
//*******************************************************************

HRESULT GUIDtoBindableString(LPGUID pGUID, LPWSTR *ppGUIDString)
{
    if((!pGUID) || (ppGUIDString==NULL))
    {
        return E_INVALIDARG;
    }

    // Build bindable GUID string.
    DWORD dwBytes =  sizeof(GUID);
    WCHAR szByte[3];
    LPWSTR pwszGUID = new WCHAR[(dwBytes * 2) + 1];
    if(NULL == pwszGUID)
    {
        return E_OUTOFMEMORY;
    }

    *pwszGUID = NULL;

    HRESULT hr = S_OK;
    LPBYTE lpByte;
    DWORD dwItem;

    // Loop through to add each byte to the string.
    for(dwItem = 0, 
        lpByte = (LPBYTE)pGUID; dwItem < dwBytes; 
        dwItem++)
    {
        // Append to pwszGUID, double-byte, byte at dwItem index.
        swprintf_s(szByte, L"%02x", lpByte[dwItem]);
        wcscat_s(pwszGuid, szByte);
    }
    
    // Allocate memory for the string.
    *ppGUIDString = AllocADsStr(pwszGUID);

    delete [] pwszGUID;
    
    if(NULL != *ppGUIDString)
    {
        hr = S_OK;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    
    // Caller must free ppGUIDString using FreeADsStr.
    return hr;
}
```



 

 





---
title: Código de ejemplo para enlazar a objetos conocidos
description: En este tema se incluye un ejemplo de código que enlaza a un objeto conocido mediante la cadena de enlace WKGUID.
ms.assetid: 59345173-5598-4b0a-976c-c5741b785ce1
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , enlace a objetos conocidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f60a1bbf457bab5b6a22a1b4b5470a4f4dbb4c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887164"
---
# <a name="example-code-for-binding-to-well-known-objects"></a>Código de ejemplo para enlazar a objetos conocidos

En el siguiente ejemplo de código de C++ se muestra cómo enlazar a un objeto conocido mediante la cadena de enlace WKGUID.


```C++
//*********************************************************
//
//  BindToWellKnownObject()
//
//  Binds to one of the well-known objects in the current domain 
//  with the current user credentials. pwszGUID must be one of  
//  the GUID strings defined in NTDSAPI.H, such as 
//  GUID_USERS_CONTAINER_W.
//
//******************************************************************

HRESULT BindToWellKnownObject(LPCWSTR pwszGUID, IADs **ppObject)
{
    if(NULL == ppObject)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppObject = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[lstrlenW(pwszFormat) + 
                           lstrlenW(pwszGUID) + 
                           lstrlenW(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, pwszGUID, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (LPVOID*)ppObject);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 





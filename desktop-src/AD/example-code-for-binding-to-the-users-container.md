---
title: Código de ejemplo para enlazar al contenedor del usuario
description: En este tema se incluye un ejemplo de código que se enlazará al contenedor de usuarios en el dominio actual y devolverá e IADsContainer interfaz para el contenedor.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , enlace al contenedor del usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f270f1814f996e84b3fa57f9753219c957cb05cd7cf29a9622f4a64f3b907d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694568"
---
# <a name="example-code-for-binding-to-the-users-container"></a>Código de ejemplo para enlazar al contenedor del usuario

El siguiente ejemplo de código de C++ se enlaza al contenedor de usuarios del dominio actual y devuelve e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interfaz para el contenedor. Para obtener más información sobre el enlace a objetos conocidos, vea [Enlace a objetos Well-Known mediante WKGUID.](binding-to-well-known-objects-using-wkguid.md)


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

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

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

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



 

 
---
title: Código de ejemplo para enlazar con el contenedor del usuario
description: En este tema se incluye un ejemplo de código que se enlazará al contenedor usuarios en el dominio actual y la interfaz devolverá e IADsContainer del contenedor.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, enlazar al contenedor del usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db1ccb3d2331c4ccef5bbf28f58fa5c046337c7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077521"
---
# <a name="example-code-for-binding-to-the-users-container"></a><span data-ttu-id="57383-104">Código de ejemplo para enlazar con el contenedor del usuario</span><span class="sxs-lookup"><span data-stu-id="57383-104">Example Code for Binding to the User's Container</span></span>

<span data-ttu-id="57383-105">En el siguiente ejemplo de código de C++ se enlaza al contenedor usuarios en el dominio actual y se devuelve e interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="57383-105">The following C++ code example binds to the users container in the current domain and return and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface for the container.</span></span> <span data-ttu-id="57383-106">Para obtener más información sobre el enlace a objetos conocidos, vea [enlazar a objetos de Well-Known mediante WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="57383-106">For more information about binding to well-known objects, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>


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



 

 
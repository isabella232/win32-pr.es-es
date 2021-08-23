---
title: Recuperar objetos eliminados
description: Los objetos eliminados se almacenan en el contenedor Objetos eliminados.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Recuperación de objetos eliminados de AD
- object AD , recuperando objetos eliminados
- Active Directory, mediante, recuperar objetos eliminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b033a992599fecfc372bf578c1bade54867fd8332c3e114103a69264f736b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025093"
---
# <a name="retrieving-deleted-objects"></a>Recuperar objetos eliminados

Los objetos eliminados se almacenan en el contenedor Objetos eliminados. Normalmente, el contenedor Objetos eliminados no es visible, pero un miembro del grupo de administradores puede enlazar el contenedor Objetos eliminados. Se puede enumerar el contenido del contenedor Objetos eliminados y se pueden obtener atributos de objeto eliminados individuales mediante la interfaz [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) con la preferencia de búsqueda **\_ SEARCHPREF \_ TOMBSTONE de ADS.**

El contenedor Objetos eliminados se puede obtener enlazando al GUID conocido **GUID \_ DELETED OBJECTS \_ \_ CONTAINER** definido en Ntdsapi.h. Para obtener más información sobre el enlace a GUID conocidos, vea Enlace a [objetos Well-Known mediante WKGUID.](binding-to-well-known-objects-using-wkguid.md)

Especifique la **opción BIND \_ FAST \_ ADS** al enlazar al contenedor Objetos eliminados. Esto significa que las interfaces ADSI usadas para trabajar con un objeto en Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)no se pueden usar en el contenedor Objetos eliminados. Para obtener más información y un ejemplo de código que muestra cómo enlazar al contenedor Objetos eliminados, vea la función de ejemplo GetDeletedObjectsContainer a continuación.

-   [Enumerar objetos eliminados](#enumerating-deleted-objects)
-   [Buscar un objeto eliminado específico](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Enumerar objetos eliminados

La [**interfaz IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) se usa para buscar objetos eliminados.

**Para enumerar los objetos eliminados**

1.  Obtenga la [**interfaz IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para el contenedor Objetos eliminados. Esto se logra enlazando al contenedor Objetos eliminados y solicitando la **interfaz IDirectorySearch.** Para obtener más información y un ejemplo de código que muestra cómo enlazar al contenedor Objetos eliminados, vea el siguiente ejemplo de función **GetDeletedObjectsContainer.**
2.  Establezca la **preferencia \_ de búsqueda SEARCHPREF \_ SEARCH SCOPE \_ de ADS** en ADS SCOPE **\_ \_ ONELEVEL** mediante el [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) También se puede usar la preferencia **\_ ADS SCOPE \_ SUBTREE,** pero el contenedor Objetos eliminados es solo un nivel, por lo que el uso de **ADS SCOPE \_ \_ SUBTREE** es redundante.
3.  Establezca la **preferencia \_ de búsqueda SEARCHPREF \_ TOMBSTONE de ADS** en **TRUE.** Esto hace que la búsqueda incluya objetos eliminados.
4.  Establezca la **preferencia de búsqueda ADS \_ SEARCHPREF \_ PAGESIZE** en un valor menor o igual que 1000. Esto es opcional, pero si no se hace, no se pueden recuperar más de 1000 objetos eliminados.
5.  Establezca el filtro de búsqueda en la [**llamada a IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) en "(isDeleted=**TRUE**)". Esto hace que la búsqueda solo recupere objetos con el **atributo isDeleted** establecido en **TRUE.**

Para obtener un código de ejemplo de código que muestra cómo enumerar objetos eliminados, vea el siguiente ejemplo de función **EnumDeletedObjects.**

La búsqueda se puede refinar aún más agregando al filtro de búsqueda como se muestra en [dialecto LDAP.](/windows/desktop/ADSI/ldap-dialect) Por ejemplo, para buscar todos los objetos eliminados con un nombre que comience por "Jeff", el filtro de búsqueda se establecería en "(&(isDeleted=**TRUE**)(cn=Jeff \* ))".

Dado que los objetos eliminados quitan la mayoría de sus atributos cuando se eliminan, no es posible enlazar directamente a un objeto eliminado. La **opción BIND FAST \_ \_ ADS** debe especificarse al enlazar a un objeto eliminado. Esto significa que las interfaces ADSI usadas para trabajar con un objeto Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)no se pueden usar en un contenedor de objetos eliminados.

## <a name="finding-a-specific-deleted-object"></a>Buscar un objeto eliminado específico

También es posible encontrar un objeto eliminado específico. Si se **conoce el objectGUID** del objeto , se puede usar para buscar el objeto con ese **objeto específicoGUID.** Para obtener más información y un ejemplo de código que muestra cómo buscar un objeto eliminado específico, vea **FindDeletedObjectByGUID** a continuación.

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

En el siguiente ejemplo de código de C++ se muestra cómo enlazar al contenedor Objetos eliminados.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
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

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
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



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

En el siguiente ejemplo de código de C++ se muestra cómo enumerar los objetos en el contenedor Objetos eliminados.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

En el siguiente ejemplo de código de C++ se muestra cómo buscar un objeto eliminado específico de la **propiedad objectGUID del** objeto.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 
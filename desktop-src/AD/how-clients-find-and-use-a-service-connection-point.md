---
title: Cómo buscan y utilizan los clientes un punto de conexión de servicio
description: En el ejemplo de código siguiente se muestra cómo una aplicación cliente busca un punto de conexión de servicio (SCP) en el catálogo global.
ms.assetid: d3163c22-22fe-4606-8cad-6f3a87f8fc36
ms.tgt_platform: multiple
keywords:
- puntos de conexión de servicio AD, cómo los clientes buscan y usan
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edf75a0002f9351903ed1c5eca79f498cb4a078d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487434"
---
# <a name="how-clients-find-and-use-a-service-connection-point"></a><span data-ttu-id="70692-104">Cómo buscan y utilizan los clientes un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="70692-104">How Clients Find and Use a Service Connection Point</span></span>

<span data-ttu-id="70692-105">En el ejemplo de código siguiente se muestra cómo una aplicación cliente busca un punto de conexión de servicio (SCP) en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="70692-105">The following code example shows how a client application searches the Global Catalog for a Service Connection Point (SCP).</span></span> <span data-ttu-id="70692-106">En este ejemplo de código, la aplicación cliente tiene una cadena GUID codificada de forma rígida que identifica el servicio.</span><span class="sxs-lookup"><span data-stu-id="70692-106">In this code example, the client application has a hard-coded GUID string that identifies the service.</span></span> <span data-ttu-id="70692-107">El instalador del servicio almacenó la misma cadena de GUID que uno de los valores del atributo de **palabras clave** de varios valores de SCP.</span><span class="sxs-lookup"><span data-stu-id="70692-107">The service installer stored the same GUID string as one of the values of the SCPs multi-value **keywords** attribute.</span></span>

<span data-ttu-id="70692-108">Este ejemplo consta de dos rutinas.</span><span class="sxs-lookup"><span data-stu-id="70692-108">This sample consists of two routines.</span></span> <span data-ttu-id="70692-109">La rutina **GetGC** recupera un puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para un catálogo global (GC).</span><span class="sxs-lookup"><span data-stu-id="70692-109">The **GetGC** routine retrieves an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer for a Global Catalog (GC).</span></span> <span data-ttu-id="70692-110">La rutina **ScpLocate** usa los métodos **IDirectorySearch** para buscar en el GC.</span><span class="sxs-lookup"><span data-stu-id="70692-110">The **ScpLocate** routine uses the **IDirectorySearch** methods to search the GC.</span></span>

<span data-ttu-id="70692-111">El GC contiene una réplica parcial de cada objeto del bosque, pero no contiene todos los atributos de SCP que requiere el cliente.</span><span class="sxs-lookup"><span data-stu-id="70692-111">The GC contains a partial replica of every object in the forest, but does not contain all of the SCP attributes that the client requires.</span></span> <span data-ttu-id="70692-112">En primer lugar, el cliente debe buscar en el GC para buscar el SCP y recuperar su DN.</span><span class="sxs-lookup"><span data-stu-id="70692-112">First, the client must search the GC to find the SCP and retrieve its DN.</span></span> <span data-ttu-id="70692-113">Después, el cliente usa el DN del SCP para enlazar con un puntero [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) en el SCP.</span><span class="sxs-lookup"><span data-stu-id="70692-113">Then the client uses the SCP's DN to bind to an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pointer on the SCP.</span></span> <span data-ttu-id="70692-114">Después, el cliente llama al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar el resto de los atributos.</span><span class="sxs-lookup"><span data-stu-id="70692-114">The client then calls the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve the rest of the attributes.</span></span>


```C++
//***************************************************************************
//
//  ScpLocate()
//
//  All strings returned by ScpLocate must be freed by the caller using 
//  FreeADsStr after it is finished using them.
//
//***************************************************************************

DWORD ScpLocate (
    LPWSTR *ppszDN,                  // Returns distinguished name of SCP.
    LPWSTR *ppszServiceDNSName,      // Returns service DNS name.
    LPWSTR *ppszServiceDNSNameType,  // Returns type of DNS name.
    LPWSTR *ppszClass,               // Returns name of service class.
    USHORT *pusPort)                 // Returns service port.
{
    HRESULT hr;
    IDirectoryObject *pSCP = NULL;
    ADS_ATTR_INFO *pPropEntries = NULL;
    IDirectorySearch *pSearch = NULL;
    ADS_SEARCH_HANDLE hSearch = NULL;

    // Get an IDirectorySearch pointer for the Global Catalog. 
    hr = GetGCSearch(&pSearch);
    if (FAILED(hr)) 
    {
        fprintf(stderr,"GetGC failed 0x%x",hr);
        goto Cleanup;
    }

    // Set up a deep search.
    // Thousands of objects are not expected in this example, therefore
    // query for 1000 rows per page.
    ADS_SEARCHPREF_INFO SearchPref[2];
    DWORD dwPref = sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;

    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;

    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    fprintf (stderr, "SetSearchPreference: 0x%x\n", hr);
    if (FAILED(hr))
    {
        fprintf (stderr, "Failed to set search prefs: hr:0x%x\n", hr);
        goto Cleanup;
    } 

    // Execute the search. From the GC get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    LPWSTR rgszDN[] = {L"distinguishedName"};

    // Search for a match of the product GUID.
    hr = pSearch->ExecuteSearch(    L"keywords=A762885A-AA44-11d2-81F1-00C04FB9624E",
                                    rgszDN,
                                    1,
                                    &hSearch);

    fprintf (stderr, "ExecuteSearch: 0x%x\n", hr);

    if (FAILED(hr)) 
    {
        fprintf (stderr, "ExecuteSearch failed: hr:0x%x\n", hr);
        goto Cleanup;
    } 

    // Loop through the results. Each row should be an instance of the 
    // service identified by the product GUID.
    // Add logic to select from multiple service instances.
    hr = pSearch->GetNextRow(hSearch);
    if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
    {
        ADS_SEARCH_COLUMN Col;

        hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
        *ppszDN = AllocADsStr(Col.pADsValues->CaseIgnoreString);
        pSearch->FreeColumn(&Col);
        hr = pSearch->GetNextRow(hSearch);
    }

    // Bind to the DN to get the other properties.
    LPWSTR lpszLDAPPrefix = L"LDAP://";
    DWORD dwSCPPathLength = wcslen(lpszLDAPPrefix) + wcslen(*ppszDN) + 1;
    LPWSTR pwszSCPPath = new WCHAR[dwSCPPathLength];
    if(pwszSCPPath)
    {
        wcscpy_s(pwszSCPPath, lpszLDAPPrefix);
        wcscat_s(pwszSCPPath, *ppszDN);
    }       
    else
    {
        fprintf(stderr,"Failed to allocate a buffer");
        goto Cleanup;
    }               

    hr = ADsGetObject(  pwszSCPPath,
                        IID_IDirectoryObject,
                        (void**)&pSCP);

    // Free the string buffer
    delete pwszSCPPath;

    if (SUCCEEDED(hr)) 
    {
        // Properties to retrieve from the SCP object.
        LPWSTR rgszAttribs[]=
        {
            {L"serviceClassName"},
            {L"serviceDNSName"},
            {L"serviceDNSNameType"},
            {L"serviceBindingInformation"}
        };

        DWORD dwAttrs = sizeof(rgszAttribs)/sizeof(LPWSTR);
        DWORD dwNumAttrGot;
        hr = pSCP->GetObjectAttributes( rgszAttribs,
                                        dwAttrs,
                                        &pPropEntries,
                                        &dwNumAttrGot);
        if(FAILED(hr)) 
        {
            fprintf (stderr, "GetObjectAttributes Failed. hr:0x%x\n", hr);
            goto Cleanup;
        }

        // Loop through the entries returned by GetObjectAttributes 
        // and save the values in the appropriate buffers. 
        for (int i = 0; i < (LONG)dwAttrs; i++) 
        {
            if ((wcscmp(L"serviceDNSName", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszServiceDNSName = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceDNSNameType", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszServiceDNSNameType = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceClassName", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *ppszClass = AllocADsStr(pPropEntries[i].pADsValues->CaseIgnoreString);
            }

            if ((wcscmp(L"serviceBindingInformation", pPropEntries[i].pszAttrName)==0) &&
                (pPropEntries[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING)) 
            {
                *pusPort=(USHORT)_wtoi(pPropEntries[i].pADsValues->CaseIgnoreString);
            }
        }
    }

Cleanup:
    if (pSCP) 
    {
        pSCP->Release();
        pSCP = NULL;
    }

    if (pPropEntries)
    {
        FreeADsMem(pPropEntries);
        pPropEntries = NULL;
    }

    if (pSearch)
    {
        if (hSearch)
        {
            pSearch->CloseSearchHandle(hSearch);
            hSearch = NULL;
        }
        
        pSearch->Release();
        pSearch = NULL;
    }

    return hr;
}

//***************************************************************************
//
//  GetGCSearch()
//
//  Retrieves an IDirectorySearch pointer for a Global Catalog (GC)
//
//***************************************************************************

HRESULT GetGCSearch(IDirectorySearch **ppDS)
{
    HRESULT hr;
    IEnumVARIANT *pEnum = NULL;
    IADsContainer *pCont = NULL;
    IDispatch *pDisp = NULL;
    VARIANT var;
    ULONG lFetch;

    *ppDS = NULL;

    // Bind to the GC: namespace container object. The true GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained using enumeration.
    hr = ADsOpenObject( L"GC:",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsContainer,
                        (void**)&pCont);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    // Get an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont, &pEnum);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    // Now enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum, 1, &var, &lFetch);
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
        goto cleanup;
    } 

    if ((hr == S_OK) && (lFetch == 1))
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
    }

cleanup:
    if (pEnum)
    {
        ADsFreeEnumerator(pEnum);
        pEnum = NULL;
    }

    if (pCont)
    {
        pCont->Release();
        pCont = NULL;
    }
    
    if (pDisp)
    {
        pDisp->Release();
        pDisp = NULL;
    }

    return hr;
}
```



 

 
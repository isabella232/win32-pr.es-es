---
title: Enumerar las réplicas de un servicio
description: En este tema se incluye un ejemplo de código que enumera las instancias instaladas de un servicio replicado en distintos equipos host en una empresa.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995cd665476a55b6bf717f356fafa54b0d2e10e6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104533094"
---
# <a name="enumerating-the-replicas-of-a-service"></a>Enumerar las réplicas de un servicio

En este tema se incluye un ejemplo de código que enumera las instancias instaladas de un servicio replicado en distintos equipos host en una empresa. Para cambiar la contraseña de la cuenta de servicio para cada instancia de un servicio replicado, use este ejemplo de código junto con el ejemplo de código del tema [cambio de la contraseña en la cuenta de usuario del servicio](changing-the-password-on-a-serviceampaposs-user-account.md) .

En el ejemplo de código se supone que cada instancia de servicio tiene su propio objeto de punto de conexión de servicio (SCP) en el directorio. Un SCP es un objeto de la clase [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) . Esta clase tiene un atributo **Keywords** , que es un atributo con varios valores que se replica en cada catálogo global (GC) del bosque. El atributo **Keywords** del SCP de cada instancia contiene el GUID del producto del servicio. Esto permite buscar todos los SCP para las distintas instancias de servicio buscando en un GC los objetos con un atributo **Keywords** que sea igual al GUID del producto.

En el ejemplo de código se obtiene un puntero [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) a un GC y se usa el método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) para buscar los SCP. Tenga en cuenta que el GC contiene una réplica parcial para cada SCP. Es decir, contiene algunos de los atributos SCP, pero no todos. En este ejemplo de código, céntrese en el atributo **serviceDNSName** , que contiene el nombre DNS del servidor host para esa instancia de servicio. Dado que **serviceDNSName** no es uno de los atributos replicados en un GC, en el ejemplo de código se usa un proceso de dos pasos para recuperarlo. En primer lugar, utiliza la búsqueda de GC para obtener el nombre distintivo (DN) del SCP y luego usa ese DN para enlazar directamente con el SCP para recuperar la propiedad **serviceDNSName** .


```C++
HRESULT EnumerateServiceInstances(
       LPWSTR szQuery,                // Search string filter.
       LPWSTR *pszAttribs,            // An array of attributes 
                                      // to retrieve.
       DWORD dwAttribs,               // # of attributes requested.
       DWORD *pdwAttribs,             // # of attributes retrieved.
       ADS_ATTR_INFO **ppPropEntries  // Returns a pointer to the 
                                      // retrieved attributes.
        )
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
BSTR  bstrPath = NULL;
ULONG lFetch;
IADs *pADs = NULL;
int iRows=0;
static IDirectorySearch *pSearch = NULL;
static ADS_SEARCH_HANDLE hSearch = NULL;

// Parameters for IDirectoryObject.
IDirectoryObject *pSCP = NULL;
 
// Structures and parameters for IDirectorySearch.
DWORD               dwPref;
ADS_SEARCH_COLUMN   Col;
ADS_SEARCHPREF_INFO SearchPref[2];
 
// First time through; set up the search.
if (pSearch == NULL) 
{
    // Bind to the GC: namespace container object. The GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained through enumeration.
    hr = ADsGetObject(L"GC:", 
        IID_IADsContainer, 
        (void**) &pCont );
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsGetObject(GC) failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Obtain an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont,&pEnum);
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum,1,&var,&lFetch);
    if (( hr == S_OK ) && ( lFetch == 1 ) ) 
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IADs, (void**)&pADs);
        if (hr == S_OK) 
            hr = pADs->get_ADsPath(&bstrPath);
    }
    if (FAILED(hr)) {
        _tprintf(TEXT("Enumeration failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Now bstrPath contains the ADsPath for the current GC.  
    // Bind the GC to get the search interface.
    hr = ADsGetObject(bstrPath, 
                      IID_IDirectorySearch, 
                      (void**)&pSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("Failed to bind search root: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Set up a deep search.
    // Thousands of objects are not expected
    // in this example; request 1000 rows per page.
    dwPref=sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;
 
    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;
 
    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    if (FAILED(hr))    {
        _tprintf(TEXT("Failed to set search prefs: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Execute the search. From the GC, get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    hr = pSearch->ExecuteSearch(szQuery, pszAttribs, 1, &hSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("ExecuteSearch failed: 0x%x\n"), hr);
        goto Cleanup;
    } 
}
 
// Get the next row.
hr = pSearch->GetNextRow(hSearch);
 
// Process the row.
if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
{
    // Get the distinguished name of the object in this row.
    hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
    if FAILED(hr) { 
        _tprintf(TEXT("GetColumn failed: 0x%x\n"), hr);
        goto Cleanup;
    }
    // Bind to the DN to get the properties.
    if (Col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
    {
        LPWSTR szSCPPath = 
          new WCHAR[7 + lstrlenW(Col.pADsValues->CaseIgnoreString) + 1];
        wcscpy_s(szSCPPath, L"LDAP://");
        wcscat_s(szSCPPath, Col.pADsValues->CaseIgnoreString);
        hr = ADsGetObject(szSCPPath, 
                          IID_IDirectoryObject,
                          (void**)&pSCP);
        delete szSCPPath;
        if (SUCCEEDED(hr)) 
        {
            hr = pSCP->GetObjectAttributes(pszAttribs, dwAttribs,
                          ppPropEntries, pdwAttribs);
            if(FAILED(hr)) {
                _tprintf(TEXT("GetObjectAttributes Failed."), hr);
                goto Cleanup;
            }
        }
    }
    pSearch->FreeColumn(&Col);}
 
Cleanup:
if (bstrPath)
    SysFreeString(bstrPath);
if (pSCP) 
    pSCP->Release();
if (pCont) 
    pCont->Release();
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pADs) 
    pADs->Release();
if (pDisp)
    pDisp->Release();
 
return hr;
 
}
```



 

 
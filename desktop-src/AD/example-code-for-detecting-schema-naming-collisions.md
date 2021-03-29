---
title: Código de ejemplo para detectar colisiones de nomenclatura de esquemas
description: En este tema se incluye un ejemplo de código que detecta colisiones de nomenclatura de esquemas.
ms.assetid: e56cefcf-ea34-4217-9aa7-2f0d4a4d06a4
ms.tgt_platform: multiple
keywords:
- Código de ejemplo para detectar colisiones de nomenclatura de esquemas AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861b7a93a53c47a234b63b5f52887a22557a2d1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773189"
---
# <a name="example-code-for-detecting-schema-naming-collisions"></a><span data-ttu-id="9c688-104">Código de ejemplo para detectar colisiones de nomenclatura de esquemas</span><span class="sxs-lookup"><span data-stu-id="9c688-104">Example Code for Detecting Schema Naming Collisions</span></span>

<span data-ttu-id="9c688-105">En este tema se incluye un ejemplo de código que detecta colisiones de nomenclatura de esquemas.</span><span class="sxs-lookup"><span data-stu-id="9c688-105">This topic includes a code example that detects schema naming collisions.</span></span>

<span data-ttu-id="9c688-106">El siguiente ejemplo de código de C/C++ consulta el esquema para los atributos de nomenclatura de claves en un objeto **ClassSchema** o **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="9c688-106">The following C/C++ code example queries the schema for the key naming attributes on a **classSchema** or **attributeSchema** object.</span></span>

<span data-ttu-id="9c688-107">Devuelve **true** si se encuentran atributos o clases en conflicto.</span><span class="sxs-lookup"><span data-stu-id="9c688-107">It returns **TRUE** if conflicting attributes or classes are found.</span></span> <span data-ttu-id="9c688-108">Devuelve **false** si el atributo o la clase con el **CN**, **lDAPDisplayName**, **OID**, **schemaIDGUID** o **LinkId** especificado no entra en conflicto con el esquema y, por tanto, es seguro agregarlo al esquema.</span><span class="sxs-lookup"><span data-stu-id="9c688-108">It returns **FALSE** if the attribute or class with the specified **cn**, **lDAPDisplayName**, **OID**, **schemaIDGUID**, or **linkID** does not conflict with the schema and, therefore, is safe to add to the schema.</span></span>


```C++
/********************************************************************

    FindCollidingAttributesOrClasses()

********************************************************************/

HRESULT FindCollidingAttributesOrClasses(
    IDirectorySearch *pSchemaNC, // IDirectorySearch pointer to 
                                 // schema naming context.
    LPWSTR szName,
    LPWSTR szLDAPDisplayName,
    LPWSTR szOID,
    const GUID * pSchemaIDGUID,
    DWORD dwLinkID, // Value is zero (0) if the attribute is not linked,
                    // or if checking for class.
    BOOL *pfIsColliding)
{
    if (!pSchemaNC || 
        !szName ||
        !szLDAPDisplayName || 
        !szOID || 
        !pSchemaIDGUID)
    {
        return E_POINTER;
    }
 
    HRESULT hr = E_FAIL;
        
    LPWSTR szBuffer = NULL;
        
    hr = ADsEncodeBinaryData((LPBYTE)pSchemaIDGUID, 
                             sizeof(GUID), 
                             &szBuffer);
    if (SUCCEEDED(hr))
    {
        LPWSTR pwszFormatLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s)(linkID=%d))";
        LPWSTR pwszFormatNoLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s))";
        LPWSTR szFilter = new WCHAR[lstrlenW(pwszFormatLinkID) + 
                                    lstrlenW(szName) + 
                                    lstrlenW(szLDAPDisplayName) + 
                                    lstrlenW(szOID) + 
                                    lstrlenW(szOID) +
                                    lstrlenW(szBuffer) +
                                    20 +
                                    1];

        if(szFilter)
        {
            if (dwLinkID > 0L)
            {
                swprintf_s(szFilter,
                    pwszFormatLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer,
                    dwLinkID);
            }
            else
            {
                swprintf_s(szFilter,
                    pwszFormatNoLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer);
            }
            
            // Attributes are one-level deep in the Schema 
            // container so only search one level.
            ADS_SEARCHPREF_INFO SearchPrefs[2];
            SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
            SearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

            SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
            SearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[1].vValue.Integer = 1000;
            
            int iCount = 0;
            
            // Set the search preference
            hr = pSchemaNC->SetSearchPreference(
                   SearchPrefs, 
                   sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO)
                 );
            if (SUCCEEDED(hr))
            {
                LPWSTR pszAttribs[] = {
                    L"lDAPDisplayName", 
                    L"cn", 
                    L"attributeID", 
                    L"governsID", 
                    L"schemaIDGUID", 
                    L"linkID", 
                    L"objectCategory"
                };

                // Handle used for searching
                ADS_SEARCH_HANDLE hSearch = NULL;
                DWORD x = 0L;
                
                hr = pSchemaNC->ExecuteSearch(szFilter,
                                pszAttribs,
                                sizeof(pszAttribs)/sizeof(LPWSTR),
                                &hSearch);
                if (SUCCEEDED(hr))
                {
                    // Call IDirectorySearch::GetNextRow() 
                    // to retrieve the next row  of data.
                    hr = pSchemaNC->GetFirstRow(hSearch);
                    while (hr != S_ADS_NOMORE_ROWS)
                    {
                        // Keep track of count.
                        iCount++;

                        // Get the next row
                        hr = pSchemaNC->GetNextRow(hSearch);
                    }
            
                    // Close the search handle to cleanup
                    pSchemaNC->CloseSearchHandle(hSearch);

                    if(SUCCEEDED(hr))
                    {
                        if (0 == iCount)
                        {
                            *pfIsColliding = FALSE;
                        }
                        else
                        {
                            *pfIsColliding = TRUE;
                        }

                        hr = S_OK;
                    }
                }
            }

            delete szFilter;
        }
            
        FreeADsMem(szBuffer);
    }
    
    return hr;
}
```



 

 





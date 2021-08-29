---
title: Realizar una consulta de ámbito de atributo
description: La consulta de ámbito de atributo es una preferencia de búsqueda que permite realizar una búsqueda de atributos con valores de nombre distintivo de un objeto.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Realización de un ADSI de consulta de ámbito de atributo
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Consulta de ámbito de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40251665f487919ce22b78057c6026324b49e33764545b55c38310265474484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637805"
---
# <a name="performing-an-attribute-scope-query"></a>Realizar una consulta de ámbito de atributo

La consulta de ámbito de atributo es una preferencia de búsqueda que permite realizar una búsqueda de atributos con valores de nombre distintivo de un objeto. El atributo que se va a buscar puede ser único o multivalor, pero debe ser del tipo **ADS \_ DN \_ STRING.** Cuando se realiza la búsqueda, ADSI enumerará los valores de nombre distintivo del atributo y realizará la búsqueda en los objetos representados por los nombres distintivos. Por ejemplo, si se realiza una [](/windows/desktop/ADSchema/a-member) búsqueda con ámbito de atributo del atributo miembro de  un objeto de grupo, ADSI enumerará los nombres distintivos en el atributo de miembro y buscará en cada uno de los miembros del grupo los criterios de búsqueda especificados.

Si se realiza una consulta con ámbito de atributo en un atributo que no es de tipo **ADS \_ DN \_ STRING**, se producirá un error en la búsqueda. La consulta con ámbito de atributo también requiere que la preferencia **\_ SEARCHPREF \_ SEARCH \_ SCOPE de ADS** se establezca en ADS SCOPE **\_ \_ BASE**. La preferencia **\_ ADS SEARCHPREF SEARCH \_ \_ SCOPE** se establecerá automáticamente en **ADS SCOPE \_ \_ BASE,** pero si la preferencia **\_ SEARCHPREF \_ SEARCH SCOPE \_ de ADS** se establece en cualquier otro valor, [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) producirá un error **con E ADS BAD \_ \_ \_ PARAMETER**.

Los resultados de una consulta de ámbito de atributo pueden abarcar varios servidores y es posible que un servidor no devuelva todos los datos solicitados para todas las filas devueltas. Si esto ocurre, cuando se recupera la última fila mediante una llamada a [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**IDirectorySearch::GetFirstRow,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)ADSI devolverá **S ADS \_ \_ ERRORSOCCURRED** en lugar de **S ADS \_ \_ NOMORE \_ ROWS**.

Para especificar una consulta de ámbito de atributo, establezca una opción de búsqueda **\_ ADS SEARCHPREF \_ ATTRIBUTE \_ QUERY** con un valor DE CADENA **ADSTYPE CASE \_ \_ IGNORE \_** establecido en el valor lDAPDisplayName del atributo que se buscará en la matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Esta operación se muestra en el ejemplo de código siguiente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



En el ejemplo de código siguiente se muestra cómo usar la opción **\_ de búsqueda SEARCHPREF \_ ATTRIBUTE \_ QUERY** de ADS.


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



Cuando se ejecuta esta búsqueda y se enumeran los resultados, devolvería el nombre **,** el número de teléfono  y el número de oficina de todos los objetos de usuario incluidos en la lista de atributos de miembro del grupo.  

Control de errores: los resultados de una consulta de ámbito de atributo pueden abarcar varios servidores y es posible que un servidor no devuelva todos los datos solicitados para todas las filas devueltas. Si esto ocurre, cuando se recupera la última fila mediante una llamada a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**GetFirstRow,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)ADSI devolverá **S ADS \_ \_ ERRORSOCCURRED**, en lugar de **S ADS \_ \_ NOMORE \_ ROWS**.

 

 
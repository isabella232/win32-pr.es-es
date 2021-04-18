---
title: Realización de una consulta de ámbito de atributo
description: La consulta de ámbito de atributo es una preferencia de búsqueda que permite realizar una búsqueda de los atributos con valores de nombre distintivo de un objeto.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Realización de una consulta de ámbito de atributo ADSI
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, consulta de ámbito de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656409"
---
# <a name="performing-an-attribute-scope-query"></a><span data-ttu-id="4b095-105">Realización de una consulta de ámbito de atributo</span><span class="sxs-lookup"><span data-stu-id="4b095-105">Performing an Attribute Scope Query</span></span>

<span data-ttu-id="4b095-106">La consulta de ámbito de atributo es una preferencia de búsqueda que permite realizar una búsqueda de los atributos con valores de nombre distintivo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="4b095-106">The attribute scope query is a search preference that enables a search of an object's distinguished name valued attributes to be performed.</span></span> <span data-ttu-id="4b095-107">El atributo que se va a buscar puede ser uno o varios valores, pero debe ser del tipo de **\_ \_ cadena DN de ADS** .</span><span class="sxs-lookup"><span data-stu-id="4b095-107">The attribute to search can be either single or multi-valued, but must be of the **ADS\_DN\_STRING** type.</span></span> <span data-ttu-id="4b095-108">Cuando se realice la búsqueda, ADSI enumerará los valores de nombre distintivo del atributo y realizará la búsqueda en los objetos representados por los nombres distintivos.</span><span class="sxs-lookup"><span data-stu-id="4b095-108">When the search is performed, ADSI will enumerate the distinguished name values of the attribute and perform the search on the objects represented by the distinguished names.</span></span> <span data-ttu-id="4b095-109">Por ejemplo, si se realiza una búsqueda de ámbito de atributo del atributo de [**miembro**](/windows/desktop/ADSchema/a-member) de un objeto de grupo, ADSI enumerará los nombres distintivos en el atributo de **miembro** y buscará en cada uno de los miembros del grupo los criterios de búsqueda especificados.</span><span class="sxs-lookup"><span data-stu-id="4b095-109">For example, if an attribute scoped search is performed of the [**member**](/windows/desktop/ADSchema/a-member) attribute of a group object, ADSI will enumerate the distinguished names in the **member** attribute and search each of the members of the group for the specified search criteria.</span></span>

<span data-ttu-id="4b095-110">Si se realiza una consulta de ámbito de atributo en un atributo que no es del **tipo \_ \_ cadena DN de ADS**, se producirá un error en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4b095-110">If an attribute scoped query is performed on an attribute that is not of type **ADS\_DN\_STRING**, the search will fail.</span></span> <span data-ttu-id="4b095-111">La consulta de ámbito de atributo también requiere que la preferencia de **\_ ámbito de \_ búsqueda \_ de ADS SEARCHPREF** esté establecida en la **\_ \_ base del ámbito de ADS**.</span><span class="sxs-lookup"><span data-stu-id="4b095-111">The attribute scoped query also requires that the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference be set to **ADS\_SCOPE\_BASE**.</span></span> <span data-ttu-id="4b095-112">La preferencia del **\_ ámbito de \_ búsqueda \_ de ADS SEARCHPREF** se establecerá automáticamente en la **\_ \_ base del ámbito de ADS**, pero si la preferencia del **\_ \_ \_ ámbito de búsqueda de ADS SEARCHPREF** está establecida en cualquier otro valor, se producirá un error en [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) con el **\_ parámetro E ADS \_ incorrectos \_**.</span><span class="sxs-lookup"><span data-stu-id="4b095-112">The **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference will automatically be set to **ADS\_SCOPE\_BASE**, but if the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference is set to any other value, [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) will fail with **E\_ADS\_BAD\_PARAMETER**.</span></span>

<span data-ttu-id="4b095-113">Los resultados de una consulta de ámbito de atributo pueden abarcar varios servidores y un servidor puede no devolver todos los datos solicitados para todas las filas devueltas.</span><span class="sxs-lookup"><span data-stu-id="4b095-113">The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="4b095-114">Si esto ocurre, cuando se recupere la última fila mediante una llamada a [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI devolverá **s \_ ADS \_ ERRORSOCCURRED** en lugar de **s \_ ADS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4b095-114">If this occurs, when the last row is retrieved by calling [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED** instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

<span data-ttu-id="4b095-115">Para especificar una consulta de ámbito de atributo, establezca una opción de búsqueda de **\_ consultas de \_ atributos \_ de ADS SEARCHPREF** con un valor de **\_ \_ \_ cadena ignore case de ADSTYPE** en el lDAPDisplayName del atributo que se va a buscar en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="4b095-115">To specify an attribute scope query, set an **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option with an **ADSTYPE\_CASE\_IGNORE\_STRING** value set to the lDAPDisplayName of the attribute to search in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="4b095-116">Esta operación se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b095-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



<span data-ttu-id="4b095-117">En el ejemplo de código siguiente se muestra cómo usar la opción de búsqueda de **\_ consultas de \_ atributos \_ de ADS SEARCHPREF** .</span><span class="sxs-lookup"><span data-stu-id="4b095-117">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option.</span></span>


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



<span data-ttu-id="4b095-118">Cuando se ejecuta esta búsqueda y se enumeran los resultados, se devuelve el **nombre**, el **número de teléfono** y el **número de oficina** de todos los objetos de usuario contenidos en la lista de atributos de **miembro** del grupo.</span><span class="sxs-lookup"><span data-stu-id="4b095-118">When this search is executed and the results are enumerated, it would return the **name**, **telephone number**, and **office number** of all of the user objects contained in the group's **member** attribute list.</span></span>

<span data-ttu-id="4b095-119">Control de errores: los resultados de una consulta de ámbito de atributo pueden abarcar varios servidores y un servidor puede no devolver todos los datos solicitados para todas las filas devueltas.</span><span class="sxs-lookup"><span data-stu-id="4b095-119">Error handling: The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="4b095-120">Si esto ocurre, cuando se recupera la última fila mediante una llamada a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) o [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI devolverá **s \_ ADS \_ ERRORSOCCURRED**, en lugar de **s \_ ADS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4b095-120">If this occurs, when the last row is retrieved by calling [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED**, instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

 

 
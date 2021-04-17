---
title: Recuperando objetos eliminados
description: Los objetos eliminados se almacenan en el contenedor de objetos eliminados.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Recuperando objetos eliminados AD
- objeto AD, recuperar objetos eliminados
- Active Directory, usar, recuperar objetos eliminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487410"
---
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="4ab11-106">Recuperando objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="4ab11-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="4ab11-107">Los objetos eliminados se almacenan en el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="4ab11-108">Normalmente, el contenedor de objetos eliminados no es visible, pero el contenedor de objetos eliminados se puede enlazar a un miembro del grupo de administradores.</span><span class="sxs-lookup"><span data-stu-id="4ab11-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="4ab11-109">Se puede enumerar el contenido del contenedor de objetos eliminados y se pueden obtener atributos de objeto eliminados individuales mediante la interfaz [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) con la preferencia de búsqueda de **marcadores de \_ \_ exclusión de SEARCHPREF de ADS** .</span><span class="sxs-lookup"><span data-stu-id="4ab11-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="4ab11-110">El contenedor de objetos eliminados se puede obtener enlazando al **\_ \_ \_ contenedor de objetos eliminados GUID** de GUID conocido definido en ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="4ab11-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="4ab11-111">Para obtener más información sobre el enlace a GUID conocidos, vea [enlazar a objetos de Well-Known mediante WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="4ab11-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="4ab11-112">Especifique la opción de **\_ \_ enlace rápido de ADS** al enlazar con el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="4ab11-113">Esto significa que las interfaces ADSI utilizadas para trabajar con un objeto en Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), no se pueden usar en el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="4ab11-114">Para obtener más información y un ejemplo de código que muestra cómo enlazar con el contenedor de objetos eliminados, consulte la siguiente función de ejemplo de GetDeletedObjectsContainer.</span><span class="sxs-lookup"><span data-stu-id="4ab11-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="4ab11-115">Enumerar objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="4ab11-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="4ab11-116">Buscar un objeto eliminado específico</span><span class="sxs-lookup"><span data-stu-id="4ab11-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="4ab11-117">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="4ab11-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="4ab11-118">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="4ab11-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="4ab11-119">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="4ab11-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="4ab11-120">Enumerar objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="4ab11-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="4ab11-121">La interfaz [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) se utiliza para buscar objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="4ab11-122">**Para enumerar los objetos eliminados**</span><span class="sxs-lookup"><span data-stu-id="4ab11-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="4ab11-123">Obtenga la interfaz [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="4ab11-124">Esto se logra enlazando al contenedor de objetos eliminados y solicitando la interfaz **IDirectorySearch** .</span><span class="sxs-lookup"><span data-stu-id="4ab11-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="4ab11-125">Para obtener más información y un ejemplo de código que muestra cómo enlazar con el contenedor de objetos eliminados, vea el siguiente ejemplo de la función **GetDeletedObjectsContainer** .</span><span class="sxs-lookup"><span data-stu-id="4ab11-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="4ab11-126">Establezca la preferencia de búsqueda del **\_ ámbito de \_ búsqueda \_ de ADS SEARCHPREF** en el **ámbito de ADS \_ \_** con el método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="4ab11-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="4ab11-127">También se puede usar la preferencia de **\_ \_ subárbol de ámbito de ADS** , pero el contenedor de objetos eliminados solo es un nivel, por lo que el uso de **\_ \_ subárbol de ámbito de ADS** es redundante.</span><span class="sxs-lookup"><span data-stu-id="4ab11-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="4ab11-128">Establezca la preferencia de búsqueda de **registros de marcadores de exclusión de ADS \_ \_ SEARCHPREF** en **true**.</span><span class="sxs-lookup"><span data-stu-id="4ab11-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="4ab11-129">Esto hace que la búsqueda incluya objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="4ab11-130">Establezca la preferencia de búsqueda **\_ SEARCHPREF de \_ las páginas de anuncios** en un valor menor o igual que 1000.</span><span class="sxs-lookup"><span data-stu-id="4ab11-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="4ab11-131">Esto es opcional, pero si no se hace, no se pueden recuperar más de 1000 objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="4ab11-132">Establezca el filtro de búsqueda en la llamada [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) a "(IsDeleted =**true**)".</span><span class="sxs-lookup"><span data-stu-id="4ab11-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="4ab11-133">Esto hace que la búsqueda solo recupere objetos con el atributo **IsDeleted** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="4ab11-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="4ab11-134">Para ver un código de ejemplo de código que muestra cómo enumerar los objetos eliminados, vea el siguiente ejemplo de la función **EnumDeletedObjects** .</span><span class="sxs-lookup"><span data-stu-id="4ab11-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="4ab11-135">La búsqueda se puede afinar más agregando al filtro de búsqueda tal y como se muestra en el [dialecto LDAP](/windows/desktop/ADSI/ldap-dialect).</span><span class="sxs-lookup"><span data-stu-id="4ab11-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="4ab11-136">Por ejemplo, para buscar todos los objetos eliminados con un nombre que comience por "Juan", el filtro de búsqueda se establecería en "(& (isDeleted =**true**) (CN = Juan \* ))".</span><span class="sxs-lookup"><span data-stu-id="4ab11-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="4ab11-137">Dado que los objetos eliminados tienen la mayoría de sus atributos quitados cuando se eliminan, no es posible enlazar directamente a un objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="4ab11-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="4ab11-138">Se debe especificar la opción de **\_ \_ enlace rápido de ADS** al enlazar con un objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="4ab11-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="4ab11-139">Esto significa que las interfaces ADSI utilizadas para trabajar con un objeto Active Directory Domain Services, como [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), no se pueden usar en un contenedor de objetos eliminado.</span><span class="sxs-lookup"><span data-stu-id="4ab11-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="4ab11-140">Buscar un objeto eliminado específico</span><span class="sxs-lookup"><span data-stu-id="4ab11-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="4ab11-141">También es posible encontrar un objeto eliminado específico.</span><span class="sxs-lookup"><span data-stu-id="4ab11-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="4ab11-142">Si se conoce el **objectGUID** del objeto, se puede usar para buscar el objeto con ese **objectGUID** específico.</span><span class="sxs-lookup"><span data-stu-id="4ab11-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="4ab11-143">Para obtener más información y un ejemplo de código que muestra cómo buscar un objeto eliminado específico, vea **FindDeletedObjectByGUID** a continuación.</span><span class="sxs-lookup"><span data-stu-id="4ab11-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="4ab11-144">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="4ab11-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="4ab11-145">En el ejemplo de código de C++ siguiente se muestra cómo enlazar con el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="4ab11-146">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="4ab11-146">EnumDeletedObjects</span></span>

<span data-ttu-id="4ab11-147">En el ejemplo de código de C++ siguiente se muestra cómo enumerar los objetos del contenedor objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="4ab11-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="4ab11-148">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="4ab11-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="4ab11-149">En el ejemplo de código de C++ siguiente se muestra cómo buscar un objeto eliminado específico de la propiedad **objectGUID** del objeto.</span><span class="sxs-lookup"><span data-stu-id="4ab11-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 
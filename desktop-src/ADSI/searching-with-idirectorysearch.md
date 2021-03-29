---
title: Buscar con la interfaz IDirectorySearch
description: La interfaz IDirectorySearch proporciona una interfaz de alto nivel y poca sobrecarga para consultar datos de un directorio o un catálogo global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Buscar con la interfaz IDirectorySearch ADSI
- Consultas ADSI, interfaces de consulta, IDirectorySearch
- ADSI ADSI, código de ejemplo C/C++, buscar un directorio con IDirectorySearch
- ADSI de IDirectorySearch, usar para buscar en un directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904829"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="89419-107">Buscar con la interfaz IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="89419-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="89419-108">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona una interfaz de alto nivel y poca sobrecarga para consultar datos de un directorio o un catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89419-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="89419-109">La interfaz com **IDirectorySearch** solo se puede usar con vtable y, por lo tanto, no está disponible para los entornos de desarrollo basados en automatización.</span><span class="sxs-lookup"><span data-stu-id="89419-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="89419-110">**Para realizar una búsqueda**</span><span class="sxs-lookup"><span data-stu-id="89419-110">**To perform a search**</span></span>

1.  <span data-ttu-id="89419-111">Enlazar a un objeto en el directorio.</span><span class="sxs-lookup"><span data-stu-id="89419-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="89419-112">Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el puntero [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="89419-113">Ejecute la búsqueda con el puntero [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="89419-114">Llame al método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) y pase un filtro de búsqueda, los nombres de atributo solicitados y otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="89419-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="89419-115">Para obtener más información sobre la sintaxis del filtro de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="89419-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="89419-116">La ejecución de la consulta es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="89419-116">Query execution is provider-specific.</span></span> <span data-ttu-id="89419-117">Con algunos proveedores, la ejecución de la consulta real no se realiza hasta que se llama a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="89419-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="89419-118">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona directamente con los filtros de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89419-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="89419-119">No se requieren el dialecto SQL ni el dialecto LDAP.</span><span class="sxs-lookup"><span data-stu-id="89419-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="89419-120">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona métodos para enumerar el conjunto de resultados, fila por fila.</span><span class="sxs-lookup"><span data-stu-id="89419-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="89419-121">El método [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la primera fila y [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) le lleva a la fila siguiente de la fila actual.</span><span class="sxs-lookup"><span data-stu-id="89419-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="89419-122">Cuando se ha alcanzado la última fila, al llamar a estos métodos, se devuelve el \_ \_ código de error de filas nomores \_ .</span><span class="sxs-lookup"><span data-stu-id="89419-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="89419-123">Por el contrario, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) mueve una fila cada vez.</span><span class="sxs-lookup"><span data-stu-id="89419-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="89419-124">Un \_ \_ \_ valor devuelto por un número de filas de los anuncios de S indica que ha alcanzado la primera fila del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="89419-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="89419-125">Estos métodos operan en el conjunto de resultados, residente en memoria, en el cliente.</span><span class="sxs-lookup"><span data-stu-id="89419-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="89419-126">Por lo tanto, cuando se realizan búsquedas en páginas y asincrónicas y la \_ opción resultados de caché está desactivada \_ , el desplazamiento hacia atrás puede tener consecuencias inesperadas.</span><span class="sxs-lookup"><span data-stu-id="89419-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="89419-127">Cuando haya encontrado la fila adecuada, llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obtener elementos de datos, columna por columna.</span><span class="sxs-lookup"><span data-stu-id="89419-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="89419-128">Para cada llamada, se pasa el nombre de la columna de interés.</span><span class="sxs-lookup"><span data-stu-id="89419-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="89419-129">El elemento de datos devuelto es un puntero a una estructura de [**\_ \_ columnas de búsqueda de ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) .</span><span class="sxs-lookup"><span data-stu-id="89419-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="89419-130">**Getcolumn (** asigna esta estructura automáticamente, pero debe liberarla con [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span><span class="sxs-lookup"><span data-stu-id="89419-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="89419-131">Llame a [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para completar la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89419-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="89419-132">**Para realizar una búsqueda de directorio**</span><span class="sxs-lookup"><span data-stu-id="89419-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="89419-133">Enlazar a un proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="89419-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="89419-134">Puede ser un controlador de dominio o un proveedor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89419-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="89419-135">Recuperar la interfaz com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una llamada a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); es posible que esta operación se haya realizado en el paso 1 durante el enlace inicial.</span><span class="sxs-lookup"><span data-stu-id="89419-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="89419-136">Opcionalmente, llame a [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para seleccionar las opciones para administrar los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89419-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="89419-137">Llame a [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span><span class="sxs-lookup"><span data-stu-id="89419-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="89419-138">En función de las opciones establecidas en [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , puede iniciar la ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="89419-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="89419-139">Llame a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para trasladar el índice de fila (interno a [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) a la primera fila.</span><span class="sxs-lookup"><span data-stu-id="89419-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="89419-140">Lea los datos de la fila mediante [**getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)y, a continuación, llame a [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar la memoria asignada por **getcolumn (**.</span><span class="sxs-lookup"><span data-stu-id="89419-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="89419-141">Repita el paso 5 hasta que se recuperen todos los datos del resultado de la búsqueda, o hasta que [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) devuelva el resto de filas de S \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="89419-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="89419-142">Llame a [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) y [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) cuando haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="89419-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="89419-143">En el ejemplo de código siguiente se muestra este escenario.</span><span class="sxs-lookup"><span data-stu-id="89419-143">The following code example shows this scenario.</span></span> <span data-ttu-id="89419-144">Para empezar a enlazar a ADSI, llame a la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="89419-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="89419-145">Esto proporciona un puntero a la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="89419-146">Ahora que hay una interfaz COM para una instancia de IDirectoryInterface, llame a [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span><span class="sxs-lookup"><span data-stu-id="89419-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="89419-147">Cree una matriz de nombres de atributo para preparar la llamada a la función [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="89419-148">Los nombres de atributo se definen en el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="89419-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="89419-149">Para obtener más información acerca de la definición de esquema, vea [modelo de esquema ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="89419-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="89419-150">Se devuelven los nombres de atributo enumerados, si el objeto lo admite, como el conjunto de resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89419-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="89419-151">Ahora, llame a la función [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="89419-152">La búsqueda no se ejecuta hasta que se llama al método [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="89419-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="89419-153">Llame a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar las filas en el resultado.</span><span class="sxs-lookup"><span data-stu-id="89419-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="89419-154">A continuación, se consulta a cada fila el atributo "Description".</span><span class="sxs-lookup"><span data-stu-id="89419-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="89419-155">Si se encuentra el atributo, se muestra.</span><span class="sxs-lookup"><span data-stu-id="89419-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="89419-156">Para finalizar la búsqueda, llame al método [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .</span><span class="sxs-lookup"><span data-stu-id="89419-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="89419-157">Tenga en cuenta que si no se establece un tamaño de página, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) se bloquea hasta que se devuelve el conjunto de resultados completo al cliente.</span><span class="sxs-lookup"><span data-stu-id="89419-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="89419-158">Si se establece tamaño de página, **GetNextRow** se bloquea hasta que se devuelve la primera página (tamaño de página = número de filas de una página).</span><span class="sxs-lookup"><span data-stu-id="89419-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="89419-159">Si se establece el tamaño de página y la consulta se va a ordenar y no está buscando por lo menos un atributo indexado, se omite el valor de tamaño de página y el servidor calcula el conjunto de resultados completo antes de devolver los datos.</span><span class="sxs-lookup"><span data-stu-id="89419-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="89419-160">Esto tiene el efecto de que el **GetNextRow** se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="89419-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="89419-161">Para cambiar esta consulta de una búsqueda de directorio a una búsqueda de catálogo global, se cambia la llamada a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="89419-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 
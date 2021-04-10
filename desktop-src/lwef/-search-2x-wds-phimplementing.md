---
title: Implementar un controlador de protocolo para WDS
description: La creación de un controlador de protocolo implica la implementación de ISearchProtocol para administrar objetos UrlAccessor, IUrlAccessor para generar metadatos acerca de e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, y IFilterto filtrar archivos propietarios o para enumerar y filtrar archivos almacenados jerárquicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149222"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="dbc06-103">Implementar un controlador de protocolo para WDS</span><span class="sxs-lookup"><span data-stu-id="dbc06-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="dbc06-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dbc06-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="dbc06-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dbc06-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="dbc06-106">La creación de un controlador de protocolo implica la implementación de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) para administrar objetos UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) para generar metadatos acerca de e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para filtrar los archivos propietarios o para enumerar y filtrar los archivos almacenados jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="dbc06-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="dbc06-107">El controlador de protocolo debe ser multiproceso.</span><span class="sxs-lookup"><span data-stu-id="dbc06-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="dbc06-108">Esta sección contiene los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dbc06-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="dbc06-109">Nota sobre las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="dbc06-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="dbc06-110">Interfaces del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="dbc06-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="dbc06-111">IFilters para contenedores</span><span class="sxs-lookup"><span data-stu-id="dbc06-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="dbc06-112">Agregar funcionalidad de opciones de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="dbc06-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="dbc06-113">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="dbc06-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="dbc06-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbc06-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="dbc06-115">Nota sobre las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="dbc06-115">Note on URLs</span></span>

<span data-ttu-id="dbc06-116">Microsoft Windows Desktop Search (WDS) usa las direcciones URL para identificar de forma única los elementos de un sistema de archivos, dentro de un almacén similar a la base de datos o en la Web.</span><span class="sxs-lookup"><span data-stu-id="dbc06-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="dbc06-117">Una dirección URL que define un nodo de entrada se denomina página de inicio. WDS comienza en la página de inicio y rastrea de forma recursiva el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="dbc06-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="dbc06-118">La estructura de direcciones URL típica es:</span><span class="sxs-lookup"><span data-stu-id="dbc06-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="dbc06-119">Si desea agregar un nuevo almacén de datos, debe seleccionar un nombre para identificarlo que no entra en conflicto con los actuales.</span><span class="sxs-lookup"><span data-stu-id="dbc06-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="dbc06-120">Se recomienda esta Convención de nomenclatura: companyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="dbc06-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="dbc06-121">Interfaces del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="dbc06-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="dbc06-122">**ISearchProtocol**</span><span class="sxs-lookup"><span data-stu-id="dbc06-122">**ISearchProtocol**</span></span>

<span data-ttu-id="dbc06-123">La interfaz [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) invoca, inicializa y administra objetos UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="dbc06-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="dbc06-124">Para obtener más información sobre la implementación de la interfaz ISearchProtocol, consulte referencia de la **interfaz ISearchProtocol**.</span><span class="sxs-lookup"><span data-stu-id="dbc06-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="dbc06-125">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="dbc06-125">**IUrlAccessor**</span></span>

<span data-ttu-id="dbc06-126">En el caso de una dirección URL especificada, la interfaz [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera metadatos sobre la estructura de ubicación, así como los elementos contenidos, y enlaza esos elementos a un filtro.</span><span class="sxs-lookup"><span data-stu-id="dbc06-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="dbc06-127">Un objeto SearchProtocol crea una instancia del objeto **IUrlAccessor** y lo inicializa. sin embargo, también puede implementar un método de inicialización interno para que el objeto **IUrlAccessor** pueda realizar tareas de inicialización específicas del controlador de protocolo, como la validación de la dirección URL de un elemento al que se está accediendo o la comprobación de la hora de la última modificación para determinar si un archivo se debe procesar en el rastreo actual.</span><span class="sxs-lookup"><span data-stu-id="dbc06-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="dbc06-128">Se omiten las horas modificadas de los directorios.</span><span class="sxs-lookup"><span data-stu-id="dbc06-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="dbc06-129">El objeto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) debe enumerar los objetos secundarios para determinar si se ha producido alguna modificación o eliminación.</span><span class="sxs-lookup"><span data-stu-id="dbc06-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="dbc06-130">Gran parte del diseño del objeto **UrlAccessor** depende de si la estructura es jerárquica o basada en vínculos.</span><span class="sxs-lookup"><span data-stu-id="dbc06-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="dbc06-131">En el caso de los almacenes de datos jerárquicos, el objeto **UrlAccessor** debe encontrar un filtro que pueda enumerar su contenido.</span><span class="sxs-lookup"><span data-stu-id="dbc06-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="dbc06-132">Otra diferencia entre los controladores de protocolos jerárquicos y basados en vínculos es el uso del método IsDirectory.</span><span class="sxs-lookup"><span data-stu-id="dbc06-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="dbc06-133">En los controladores de protocolo basados en vínculos, este método debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="dbc06-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="dbc06-134">Los controladores de protocolo jerárquicos deben devolver los valores \_ correctos para los contenedores.</span><span class="sxs-lookup"><span data-stu-id="dbc06-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="dbc06-135">Para obtener más instrucciones sobre la implementación de una interfaz [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , vea la referencia de la [**interfaz IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .</span><span class="sxs-lookup"><span data-stu-id="dbc06-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="dbc06-136">**IProtocolHandlerSite**</span><span class="sxs-lookup"><span data-stu-id="dbc06-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="dbc06-137">Esta interfaz se usa para crear instancias de un objeto **SearchProtocol** y también proporciona el objeto **UrlAccessor** con un filtro adecuado para un identificador de clase especificado (CLSID).</span><span class="sxs-lookup"><span data-stu-id="dbc06-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="dbc06-138">IFilters para contenedores</span><span class="sxs-lookup"><span data-stu-id="dbc06-138">IFilters for Containers</span></span>

<span data-ttu-id="dbc06-139">Si va a implementar un controlador de protocolo jerárquico, debe implementar un componente de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor que enumere las direcciones URL que representan contenedores o carpetas.</span><span class="sxs-lookup"><span data-stu-id="dbc06-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="dbc06-140">El proceso de enumeración es un bucle a través de los métodos **GetChunk** y **GetValue** de la interfaz IFilter que devuelve una lista de direcciones URL que representan cada elemento del contenedor.</span><span class="sxs-lookup"><span data-stu-id="dbc06-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="dbc06-141">En primer lugar, **GetChunk** devuelve FULLPROSPEC con el conjunto de propiedades Gather \_ PROPSET y:</span><span class="sxs-lookup"><span data-stu-id="dbc06-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="dbc06-142">PID \_ GTHR \_ DIRLINK, la dirección URL del elemento sin la hora de la última modificación, o bien</span><span class="sxs-lookup"><span data-stu-id="dbc06-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="dbc06-143">PID \_ GTHR \_ DIRLINK \_ con \_ hora, la dirección URL junto con la hora de la última modificación</span><span class="sxs-lookup"><span data-stu-id="dbc06-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="dbc06-144">El GUID del conjunto de propiedades para GATHER \_ PROPSET es 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span><span class="sxs-lookup"><span data-stu-id="dbc06-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="dbc06-145">La propiedad PROPSPEC es PID \_ GTHR \_ DIRLINK = 2 o PID \_ GTHR \_ DIRLINK \_ con \_ Time = 12 decimal.</span><span class="sxs-lookup"><span data-stu-id="dbc06-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="dbc06-146">Devolver el PID \_ GTHR \_ DIRLINK con el \_ \_ tiempo es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indizarse sin llamar a los métodos ISearchProtocol->CreateUrlAccessor () y IUrlAccessor->GetLastModified ().</span><span class="sxs-lookup"><span data-stu-id="dbc06-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="dbc06-147">A continuación, **GetValue** devuelve un PROPVARIANT para la dirección URL (y la hora de la última modificación si se usa), como:</span><span class="sxs-lookup"><span data-stu-id="dbc06-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="dbc06-148">VT \_ LPWStr, la dirección URL del elemento secundario o</span><span class="sxs-lookup"><span data-stu-id="dbc06-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="dbc06-149">Vector de la dirección URL seguido de un FILETIME</span><span class="sxs-lookup"><span data-stu-id="dbc06-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="dbc06-150">En el código de ejemplo siguiente se muestra cómo compilar el PID adecuado \_ GTHR \_ DIRLINK \_ con \_ Time.</span><span class="sxs-lookup"><span data-stu-id="dbc06-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="dbc06-151">**ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONA "TAL CUAL" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.**</span><span class="sxs-lookup"><span data-stu-id="dbc06-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="dbc06-152">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbc06-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="dbc06-153">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="dbc06-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]
>
> <span data-ttu-id="dbc06-154">Un componente de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor siempre debe enumerar todas las direcciones URL secundarias aunque no hayan cambiado las direcciones URL secundarias, ya que el indexador detecta eliminaciones a través del proceso de enumeración.</span><span class="sxs-lookup"><span data-stu-id="dbc06-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="dbc06-155">Si la fecha de salida en un \_ vínculo de directorio \_ con \_ la hora indica que los datos no han cambiado, el indizador no actualiza los datos de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="dbc06-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="dbc06-156">La dirección URL física es la dirección URL que procesa el objeto **UrlAccessor** .</span><span class="sxs-lookup"><span data-stu-id="dbc06-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="dbc06-157">Si el filtro no emite un DisplayUrl descriptivo, WDS muestra la dirección URL física del usuario como parte de los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="dbc06-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="dbc06-158">El esquema de WDS contiene dos propiedades para controlar lo que se muestra al usuario final, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dbc06-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="dbc06-159">GUID</span><span class="sxs-lookup"><span data-stu-id="dbc06-159">GUID</span></span>                                 | <span data-ttu-id="dbc06-160">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="dbc06-160">PROPSPEC</span></span>      | <span data-ttu-id="dbc06-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbc06-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="dbc06-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="dbc06-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="dbc06-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="dbc06-163">DisplayFolder</span></span> | <span data-ttu-id="dbc06-164">Ruta de acceso de la carpeta que se muestra al usuario en los resultados de la búsqueda</span><span class="sxs-lookup"><span data-stu-id="dbc06-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="dbc06-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="dbc06-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="dbc06-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="dbc06-166">FolderName</span></span>    | <span data-ttu-id="dbc06-167">Nombre para mostrar de la carpeta principal</span><span class="sxs-lookup"><span data-stu-id="dbc06-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="dbc06-168">Si el código no emite DisplayFolder o nombreDeCarpeta, estos valores se calculan a partir de DisplayUrl.</span><span class="sxs-lookup"><span data-stu-id="dbc06-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="dbc06-169">Las barras diagonales de la dirección URL indican contenedores dentro del almacén o del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="dbc06-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="dbc06-170">Agregar funcionalidad de opciones de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="dbc06-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="dbc06-171">Para que el controlador de protocolo tenga una página de inicio predeterminada (y una dirección URL de nodo de entrada), debe implementar la interfaz **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="dbc06-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="dbc06-172">En versiones futuras de WDS, esta interfaz proporcionará enlaces al cuadro de diálogo Opciones para mejorar la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbc06-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="dbc06-173">Esta interfaz proporciona la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="dbc06-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="dbc06-174">Determina si se cumplen los requisitos para el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="dbc06-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="dbc06-175">Por ejemplo, el almacén del controlador del Protocolo puede requerir el acceso a una aplicación determinada para indizar correctamente los datos de la aplicación, pero esa aplicación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dbc06-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="dbc06-176">Identifica los requisitos mínimos que el controlador de protocolo necesita para procesar un elemento.</span><span class="sxs-lookup"><span data-stu-id="dbc06-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="dbc06-177">Los requisitos se pueden expresar en una descripción localizada y fácil de usar, como "Microsoft Outlook 2000 o superior".</span><span class="sxs-lookup"><span data-stu-id="dbc06-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="dbc06-178">Define las direcciones URL que el controlador de protocolo debe procesar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dbc06-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="dbc06-179">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="dbc06-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="dbc06-180">En la tabla siguiente se describen los métodos que debe implementar para la interfaz **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="dbc06-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="dbc06-181">Método</span><span class="sxs-lookup"><span data-stu-id="dbc06-181">Method</span></span>               | <span data-ttu-id="dbc06-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbc06-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc06-183">CheckRequirements</span><span class="sxs-lookup"><span data-stu-id="dbc06-183">CheckRequirements</span></span>    | <span data-ttu-id="dbc06-184">Determina si se cumplen los requisitos mínimos de un controlador de protocolo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dbc06-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="dbc06-185">GetDefaultCrawlScope</span><span class="sxs-lookup"><span data-stu-id="dbc06-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="dbc06-186">Devuelve una lista de direcciones URL predeterminadas dentro de un almacén especificado para un controlador de protocolo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dbc06-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="dbc06-187">GetRequirements</span><span class="sxs-lookup"><span data-stu-id="dbc06-187">GetRequirements</span></span>      | <span data-ttu-id="dbc06-188">Identifica una descripción localizada y descriptiva de los requisitos mínimos para un controlador de protocolo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dbc06-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dbc06-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbc06-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dbc06-190">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dbc06-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dbc06-191">Notificar el índice de cambios</span><span class="sxs-lookup"><span data-stu-id="dbc06-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="dbc06-192">Agregar iconos, vistas previas y menús contextuales con extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="dbc06-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="dbc06-193">Instalar y registrar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="dbc06-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 
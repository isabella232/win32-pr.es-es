---
description: La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar el controlador de protocolo a través del registro.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Instalar y registrar controladores de protocolo (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686624"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="c92d4-103">Instalar y registrar controladores de protocolo (búsqueda de Windows)</span><span class="sxs-lookup"><span data-stu-id="c92d4-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="c92d4-104">La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar el controlador de protocolo a través del registro.</span><span class="sxs-lookup"><span data-stu-id="c92d4-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="c92d4-105">La aplicación de instalación también puede Agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="c92d4-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="c92d4-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c92d4-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c92d4-107">Acerca de las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="c92d4-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="c92d4-108">Implementar interfaces de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="c92d4-109">ISearchProtocol y ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="c92d4-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="c92d4-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 y IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="c92d4-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="c92d4-111">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="c92d4-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="c92d4-112">Implementar controladores de filtro para contenedores</span><span class="sxs-lookup"><span data-stu-id="c92d4-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="c92d4-113">Instalación y registro de un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="c92d4-114">Directrices para registrar un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="c92d4-115">Registrar un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="c92d4-116">Registrar el controlador de tipo de archivo del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="c92d4-117">Asegurarse de que los elementos están indexados</span><span class="sxs-lookup"><span data-stu-id="c92d4-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="c92d4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c92d4-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="c92d4-119">Acerca de las direcciones URL</span><span class="sxs-lookup"><span data-stu-id="c92d4-119">About URLs</span></span>

<span data-ttu-id="c92d4-120">Windows Search usa las direcciones URL para identificar de forma única los elementos de la jerarquía del origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="c92d4-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="c92d4-121">La dirección URL que es el primer nodo de la jerarquía se denomina [raíz de búsqueda](-search-3x-wds-extidx-csm-searchroots.md); Windows Search comenzará la indexación en la raíz de búsqueda, solicitando que el controlador de protocolo Enumere los vínculos secundarios para cada dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="c92d4-122">La estructura de direcciones URL típica es:</span><span class="sxs-lookup"><span data-stu-id="c92d4-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="c92d4-123">La sintaxis de la dirección URL se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c92d4-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="c92d4-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c92d4-124">Syntax</span></span>           | <span data-ttu-id="c92d4-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c92d4-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="c92d4-126">Identifica el controlador de protocolo que se va a invocar para la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="c92d4-127">{SID de usuario}</span><span class="sxs-lookup"><span data-stu-id="c92d4-127">{user SID}</span></span>       | <span data-ttu-id="c92d4-128">Identifica el contexto de seguridad del usuario en el que se llama al controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="c92d4-129">Si no se identifica ningún identificador de seguridad (SID) de usuario, se llama al controlador de protocolo en el contexto de seguridad del servicio de sistema.</span><span class="sxs-lookup"><span data-stu-id="c92d4-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="c92d4-130">Define la jerarquía del almacén, donde cada barra diagonal ('/') es un separador entre los nombres de carpeta.</span><span class="sxs-lookup"><span data-stu-id="c92d4-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="c92d4-131">Representa una cadena única que identifica el elemento secundario (por ejemplo, el nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="c92d4-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="c92d4-132">El indexador de Windows Search recorta la barra diagonal final de las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="c92d4-133">Como resultado, no se puede confiar en la existencia de una barra diagonal final para identificar un directorio en lugar de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="c92d4-134">El controlador de protocolo debe ser capaz de controlar esta sintaxis de URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="c92d4-135">Asegúrese de que el nombre de protocolo que selecciona para identificar el origen de datos de Shell no entra en conflicto con los actuales.</span><span class="sxs-lookup"><span data-stu-id="c92d4-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="c92d4-136">Se recomienda esta Convención de nomenclatura: `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="c92d4-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="c92d4-137">Para obtener más información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c92d4-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="c92d4-138">Implementar interfaces de controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="c92d4-139">La creación de un controlador de protocolo requiere la implementación de las tres interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="c92d4-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="c92d4-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) para administrar objetos UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="c92d4-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="c92d4-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) para exponer las propiedades e identificar los filtros adecuados para los elementos del origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="c92d4-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="c92d4-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para filtrar los archivos propietarios o para enumerar y filtrar los archivos almacenados jerárquicamente.</span><span class="sxs-lookup"><span data-stu-id="c92d4-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="c92d4-143">Aparte de las tres interfaces obligatorias que se enumeran, las otras interfaces son opcionales y tiene la libertad de implementar las interfaces opcionales más adecuadas para la tarea a mano.</span><span class="sxs-lookup"><span data-stu-id="c92d4-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="c92d4-144">ISearchProtocol y ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="c92d4-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="c92d4-145">Las interfaces SearchProtocol inicializan y administran los objetos de UrlAccessor del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="c92d4-146">La interfaz [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) es una extensión opcional de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e incluye un método adicional para especificar más información sobre el usuario y el elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="c92d4-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 y IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="c92d4-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="c92d4-148">Las interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c92d4-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="c92d4-149">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c92d4-149">Interface</span></span>                                                 | <span data-ttu-id="c92d4-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="c92d4-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c92d4-151">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="c92d4-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="c92d4-152">En el caso de una dirección URL especificada, la interfaz [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporciona acceso a las propiedades del elemento que se expone en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="c92d4-153">También puede enlazar esas propiedades a un filtro específico del controlador de protocolo (es decir, un filtro distinto del asociado al nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="c92d4-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="c92d4-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (opcional)</span><span class="sxs-lookup"><span data-stu-id="c92d4-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="c92d4-155">La interfaz [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) extiende [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) con métodos que obtienen una página de códigos para las propiedades del elemento y su dirección URL de visualización, y que obtienen el tipo de elemento en la dirección URL (documento o directorio).</span><span class="sxs-lookup"><span data-stu-id="c92d4-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="c92d4-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (opcional)</span><span class="sxs-lookup"><span data-stu-id="c92d4-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="c92d4-157">La interfaz [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) extiende [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) con un método que obtiene una matriz de SID de usuario, lo que permite al host del Protocolo de búsqueda suplantar a estos usuarios para indizar el elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="c92d4-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (opcional)</span><span class="sxs-lookup"><span data-stu-id="c92d4-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="c92d4-159">La interfaz [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) extiende la funcionalidad de la interfaz [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) con un método que identifica si se debe indizar el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="c92d4-160">Un objeto SearchProtocol crea una instancia del objeto UrlAccessor y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="c92d4-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="c92d4-161">Las interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporcionan acceso a fragmentos importantes de información a través de los métodos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c92d4-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="c92d4-162">Método</span><span class="sxs-lookup"><span data-stu-id="c92d4-162">Method</span></span>                                                                                        | <span data-ttu-id="c92d4-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="c92d4-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c92d4-164">**IUrlAccessor::GetLastModified**</span><span class="sxs-lookup"><span data-stu-id="c92d4-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="c92d4-165">Devuelve la hora a la que se modificó la dirección URL por última vez.</span><span class="sxs-lookup"><span data-stu-id="c92d4-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="c92d4-166">Si esta hora es más reciente que la última vez que el indexador procesó esta dirección URL, se llama a los controladores de filtro (implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extraer los datos modificados (posiblemente) de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="c92d4-167">Se omiten las horas modificadas de los directorios.</span><span class="sxs-lookup"><span data-stu-id="c92d4-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="c92d4-168">**IUrlAccessor::IsDirectory**</span><span class="sxs-lookup"><span data-stu-id="c92d4-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="c92d4-169">Identifica si la dirección URL representa una carpeta que contiene las direcciones URL secundarias.</span><span class="sxs-lookup"><span data-stu-id="c92d4-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="c92d4-170">**IUrlAccessor::BindToStream**</span><span class="sxs-lookup"><span data-stu-id="c92d4-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="c92d4-171">Enlaza a una [interfaz IStream](/windows/win32/api/objidl/nn-objidl-istream) que representa los datos de un archivo en un almacén de datos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c92d4-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="c92d4-172">**IUrlAccessor::BindToFilter**</span><span class="sxs-lookup"><span data-stu-id="c92d4-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="c92d4-173">Enlaza a un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)específico del controlador de protocolo, que puede exponer propiedades para el elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="c92d4-174">**IUrlAccessor4::ShouldIndexItemContent**</span><span class="sxs-lookup"><span data-stu-id="c92d4-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="c92d4-175">Identifica si se debe indizar el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="c92d4-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="c92d4-176">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="c92d4-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="c92d4-177">La interfaz [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) se usa para crear instancias de un controlador de filtro, que se hospeda en un proceso aislado.</span><span class="sxs-lookup"><span data-stu-id="c92d4-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="c92d4-178">El controlador de filtro adecuado se obtiene para un identificador de clase persistente (CLSID), una clase de almacenamiento de documentos o una extensión de nombre de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="c92d4-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="c92d4-179">La ventaja de solicitar que el proceso de host se enlace a [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es que el proceso de host puede administrar el proceso de búsqueda de un controlador de filtro adecuado y controlar la seguridad implicada en la llamada al controlador.</span><span class="sxs-lookup"><span data-stu-id="c92d4-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="c92d4-180">Implementar controladores de filtro para contenedores</span><span class="sxs-lookup"><span data-stu-id="c92d4-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="c92d4-181">Si va a implementar un controlador de protocolo jerárquico, debe implementar un controlador de filtro para un contenedor que enumera las direcciones URL secundarias.</span><span class="sxs-lookup"><span data-stu-id="c92d4-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="c92d4-182">Un controlador de filtro es una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="c92d4-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="c92d4-183">El proceso de enumeración es un bucle a través de los métodos [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) y [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) de la interfaz **IFilter** . cada dirección URL secundaria se expone como el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c92d4-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="c92d4-184">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve las propiedades del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c92d4-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="c92d4-185">Para enumerar las direcciones URL secundarias, **IFilter:: GetChunk** devuelve uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c92d4-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="c92d4-186">[PKEY \_ Buscar \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="c92d4-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="c92d4-187">Dirección URL del elemento sin la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="c92d4-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="c92d4-188">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un PROPVARIANT que contiene la dirección URL secundaria.</span><span class="sxs-lookup"><span data-stu-id="c92d4-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="c92d4-189">[PKEY \_ Buscar \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="c92d4-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="c92d4-190">La dirección URL y la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="c92d4-190">The URL and the last modified time.</span></span> <span data-ttu-id="c92d4-191">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un PROPVARIANT que contiene un vector de la dirección URL secundaria y la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="c92d4-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="c92d4-192">Devolver [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indexarse sin llamar a los métodos [**ISearchProtocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) y [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .</span><span class="sxs-lookup"><span data-stu-id="c92d4-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="c92d4-193">En el ejemplo de código siguiente se muestra cómo devolver la propiedad [ \_ \_ UrlToIndexWithModificationTime de búsqueda de PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="c92d4-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c92d4-194">Copyright (c) Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="c92d4-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="c92d4-195">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="c92d4-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
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
> <span data-ttu-id="c92d4-196">Un componente de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contenedor siempre debe enumerar todas las direcciones URL secundarias aunque no hayan cambiado las direcciones URL secundarias, ya que el indexador detecta eliminaciones a través del proceso de enumeración.</span><span class="sxs-lookup"><span data-stu-id="c92d4-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="c92d4-197">Si la fecha de salida en [un \_ \_ UrlToIndexWithModificationTime de búsqueda de PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) indica que los datos no han cambiado, el indexador no actualiza los datos de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="c92d4-198">Instalación y registro de un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="c92d4-199">La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar los archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="c92d4-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="c92d4-200">Los controladores de protocolo deben implementar el registro automático para la instalación.</span><span class="sxs-lookup"><span data-stu-id="c92d4-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="c92d4-201">La aplicación de instalación también puede Agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell, que se describe en [asegurarse de que los elementos se indexan](#ensuring-that-your-items-are-indexed) al final de este tema.</span><span class="sxs-lookup"><span data-stu-id="c92d4-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="c92d4-202">Directrices para registrar un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="c92d4-203">Debe seguir estas instrucciones al registrar un controlador de protocolo:</span><span class="sxs-lookup"><span data-stu-id="c92d4-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="c92d4-204">El instalador debe utilizar el instalador EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="c92d4-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="c92d4-205">Se deben proporcionar las notas de la versión.</span><span class="sxs-lookup"><span data-stu-id="c92d4-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="c92d4-206">Se debe crear una entrada agregar o quitar programas para cada complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="c92d4-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="c92d4-207">El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.</span><span class="sxs-lookup"><span data-stu-id="c92d4-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="c92d4-208">Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.</span><span class="sxs-lookup"><span data-stu-id="c92d4-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="c92d4-209">Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo de nuevo en el complemento predeterminado para ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="c92d4-210">El instalador debe definir un ámbito de rastreo predeterminado para el indizador agregando una raíz de búsqueda y reglas de ámbito mediante el administrador de ámbito de rastreo (CSM).</span><span class="sxs-lookup"><span data-stu-id="c92d4-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="c92d4-211">Registrar un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="c92d4-212">Debe hacer 14 entradas en el registro para registrar el componente de controlador de protocolo, donde:</span><span class="sxs-lookup"><span data-stu-id="c92d4-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="c92d4-213">*Ver \_ Ind \_ ProgID* es el ProgID independiente de la versión de la implementación del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="c92d4-214">*Ver \_ El \_ identificador de programa (ProgID* ) de DEP es el ProgID dependiente de la versión de la implementación del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="c92d4-215">*CLSID \_ 1* es el CLSID de la implementación del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="c92d4-216">**Para registrar un controlador de protocolo:**</span><span class="sxs-lookup"><span data-stu-id="c92d4-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="c92d4-217">Registre el ProgID independiente de la versión con las claves y los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c92d4-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="c92d4-218">Registre el ProgID dependiente de la versión con los siguientes valores y claves:</span><span class="sxs-lookup"><span data-stu-id="c92d4-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="c92d4-219">Registre el CLSID del controlador de protocolo con las claves y los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c92d4-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="c92d4-220">Registre el controlador de protocolo con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="c92d4-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="c92d4-221">En el ejemplo siguiente, <Protocol Name> es el nombre del Protocolo, como archivo, MAPI, etc.:</span><span class="sxs-lookup"><span data-stu-id="c92d4-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="c92d4-222">Antes de Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="c92d4-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="c92d4-223">Registrar el controlador de tipo de archivo del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="c92d4-224">Debe crear dos entradas en el registro para registrar el controlador de tipo de archivo del controlador de protocolo (que también se conoce como extensión de Shell).</span><span class="sxs-lookup"><span data-stu-id="c92d4-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="c92d4-225">Asegurarse de que los elementos están indexados</span><span class="sxs-lookup"><span data-stu-id="c92d4-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="c92d4-226">Después de haber implementado el controlador de protocolo, debe especificar los elementos de Shell que va a indizar el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="c92d4-227">Puede usar el administrador de catálogo para iniciar la reindización (para obtener más información, vea [usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="c92d4-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="c92d4-228">También puede usar el administrador de ámbito de rastreo (CSM) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador (para obtener más información, consulte [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md) y [Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)).</span><span class="sxs-lookup"><span data-stu-id="c92d4-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="c92d4-229">También puede Agregar una raíz de búsqueda (para obtener más información, consulte [Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)).</span><span class="sxs-lookup"><span data-stu-id="c92d4-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="c92d4-230">Otra opción disponible es seguir el procedimiento descrito en el ejemplo REINDEX en los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="c92d4-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="c92d4-231">La interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) proporciona métodos que notifican al motor de búsqueda de los contenedores que se van a rastrear o inspeccionar, y a los elementos de esos contenedores incluir o excluir al rastrear o ver.</span><span class="sxs-lookup"><span data-stu-id="c92d4-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="c92d4-232">En Windows 7 y versiones posteriores, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extiende **ISearchCrawlScopeManager** con el método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) que obtiene la versión, que informa a los clientes de si el estado de la CSM ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c92d4-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92d4-233">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c92d4-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c92d4-234">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c92d4-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c92d4-235">Descripción de los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="c92d4-236">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="c92d4-237">Notificar el índice de cambios</span><span class="sxs-lookup"><span data-stu-id="c92d4-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="c92d4-238">Agregar iconos y menús contextuales</span><span class="sxs-lookup"><span data-stu-id="c92d4-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="c92d4-239">Código de ejemplo: extensiones de Shell para controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="c92d4-240">Crear un conector de búsqueda para un controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c92d4-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="c92d4-241">Controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="c92d4-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

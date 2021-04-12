---
description: Microsoft proporciona varios filtros estándar con Windows Search. Los clientes llaman a estos controladores de filtro (que son implementaciones de la interfaz de IFilter) para extraer texto y propiedades de un documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Controladores de filtro que se distribuyen con Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153971"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="ff424-104">Controladores de filtro que se distribuyen con Windows</span><span class="sxs-lookup"><span data-stu-id="ff424-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="ff424-105">Microsoft proporciona varios filtros estándar con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="ff424-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="ff424-106">Los clientes llaman a estos controladores de filtro (que son implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extraer texto y propiedades de un documento.</span><span class="sxs-lookup"><span data-stu-id="ff424-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="ff424-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ff424-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="ff424-108">Notas de implementación de Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="ff424-109">Implementación de Windows 7 y 10</span><span class="sxs-lookup"><span data-stu-id="ff424-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="ff424-110">Implementación de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff424-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="ff424-111">Implementación heredada</span><span class="sxs-lookup"><span data-stu-id="ff424-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="ff424-112">Filtros de Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="ff424-113">Controlador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="ff424-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="ff424-114">Controlador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="ff424-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="ff424-115">Controlador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="ff424-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="ff424-116">Controlador de filtro de texto sin formato</span><span class="sxs-lookup"><span data-stu-id="ff424-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="ff424-117">Controlador de filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="ff424-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="ff424-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ff424-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="ff424-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff424-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="ff424-120">Notas de implementación de Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="ff424-121">En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente.</span><span class="sxs-lookup"><span data-stu-id="ff424-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="ff424-122">Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan varios complementos.</span><span class="sxs-lookup"><span data-stu-id="ff424-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="ff424-123">Implementación de Windows 7 y 10</span><span class="sxs-lookup"><span data-stu-id="ff424-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="ff424-124">En Windows 7 y versiones posteriores, hay un nuevo comportamiento que se produce al registrar un controlador de filtro, un controlador de propiedades o una nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="ff424-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="ff424-125">Cuando se instala un nuevo controlador de propiedades o un controlador de filtro, los archivos con las extensiones correspondientes se vuelven a indizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ff424-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="ff424-126">En Windows 7 y versiones posteriores, se recomienda instalar un controlador de filtro junto con sus controladores de propiedades correspondientes y registrar el controlador de filtro antes del controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ff424-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="ff424-127">El registro del controlador de propiedades inicia una reindización inmediata de archivos indizados previamente sin requerir primero un reinicio, y aprovecha los controladores de filtro registrados previamente con el fin de indizar contenido.</span><span class="sxs-lookup"><span data-stu-id="ff424-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="ff424-128">Si solo se instala un controlador de filtro sin un controlador de propiedades correspondiente, la reindexación automática se produce después de un reinicio del servicio de indización o de un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff424-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="ff424-129">En el caso de las marcas de descripción de propiedades específicas de Windows 7, vea los temas de referencia siguientes: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) y [PROPDESC \_ SEARCHINFO \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="ff424-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="ff424-130">Implementación de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff424-130">Windows Vista Implementation</span></span>

<span data-ttu-id="ff424-131">En Windows Vista y versiones anteriores, si se instala un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o un controlador de propiedades, no se inicia una nueva indexación de los elementos existentes a menos que un fabricante de software independiente (ISV) llame explícitamente a una recompilación o reindexación de las direcciones URL coincidentes.</span><span class="sxs-lookup"><span data-stu-id="ff424-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="ff424-132">Hay dos diferencias principales entre las aplicaciones heredadas, como el servicio de Index Server y las aplicaciones más recientes como Windows Search que debe tener en cuenta al implementar filtros:</span><span class="sxs-lookup"><span data-stu-id="ff424-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="ff424-133">Uso de la interfaz [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .</span><span class="sxs-lookup"><span data-stu-id="ff424-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="ff424-134">Uso de controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff424-134">Use of property handlers.</span></span>

<span data-ttu-id="ff424-135">En primer lugar, Windows Vista y Windows Search 3,0 y versiones posteriores requieren [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="ff424-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="ff424-136">Para garantizar el rendimiento y la compatibilidad futura.</span><span class="sxs-lookup"><span data-stu-id="ff424-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="ff424-137">Para ayudar a aumentar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="ff424-137">To help increase security.</span></span> <span data-ttu-id="ff424-138">Los filtros implementados con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) son más seguros porque el contexto en el que se ejecuta el filtro no necesita los derechos para abrir archivos en el disco o a través de la red.</span><span class="sxs-lookup"><span data-stu-id="ff424-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="ff424-139">Aunque Windows Search solo usa [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), también puede incluir las implementaciones de interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) y/o [IPersistStorage interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) en los filtros para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ff424-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="ff424-140">La segunda diferencia principal es que Windows Vista y Windows Search 3,0 y versiones posteriores tienen un nuevo [sistema de propiedades](../properties/building-property-handlers.md) que usa controladores de propiedades para enumerar las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="ff424-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="ff424-141">Sin embargo, hay ocasiones en las que es necesario implementar un filtro que controla el contenido y las propiedades para:</span><span class="sxs-lookup"><span data-stu-id="ff424-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="ff424-142">Admitir implementaciones de MSSearch heredadas.</span><span class="sxs-lookup"><span data-stu-id="ff424-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="ff424-143">Atravesar vínculos.</span><span class="sxs-lookup"><span data-stu-id="ff424-143">Traverse links.</span></span>
- <span data-ttu-id="ff424-144">Conservar la información de idioma.</span><span class="sxs-lookup"><span data-stu-id="ff424-144">Preserve language information.</span></span>
- <span data-ttu-id="ff424-145">Filtrar elementos incrustados de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="ff424-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="ff424-146">En estas situaciones, se necesita una implementación de filtro completa, incluido el método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para tener acceso a los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ff424-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="ff424-147">Implementación heredada</span><span class="sxs-lookup"><span data-stu-id="ff424-147">Legacy Implementation</span></span>

<span data-ttu-id="ff424-148">Como se indicó anteriormente, Windows Vista y Windows Search incluyen un nuevo sistema de propiedades que encapsula las propiedades de un elemento que es independiente del contenido de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ff424-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="ff424-149">Este sistema de propiedades no existe en versiones anteriores de Microsoft Windows Desktop Search (WDS) 2. x.</span><span class="sxs-lookup"><span data-stu-id="ff424-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="ff424-150">Si el filtro debe admitir otras aplicaciones como se describió anteriormente, puede que tenga que administrar tanto el contenido como las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff424-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="ff424-151">Para obtener más información sobre el desarrollo de un filtro compatible, vea los siguientes temas, [IFilter (para aplicaciones heredadas)](/windows/win32/api/filter/nn-filter-ifilter)y [desarrollo de complementos de filtro (para aplicaciones heredadas)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="ff424-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="ff424-152">Filtros de Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-152">Windows Search Filters</span></span>

<span data-ttu-id="ff424-153">Microsoft proporciona varios filtros estándar con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="ff424-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="ff424-154">El contenido del archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  se resume en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ff424-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="ff424-155">Al hacer clic en el nombre de un controlador de filtro, se le remite a la descripción de esa implementación de **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="ff424-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="ff424-156">Controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="ff424-156">Filter handler</span></span>                                                  | <span data-ttu-id="ff424-157">Archivos filtrados</span><span class="sxs-lookup"><span data-stu-id="ff424-157">Files filtered</span></span>                              | <span data-ttu-id="ff424-158">DLL de IFilter</span><span class="sxs-lookup"><span data-stu-id="ff424-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="ff424-159">Controlador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="ff424-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="ff424-160">Extensión multipropósito de correo Internet (MIME)</span><span class="sxs-lookup"><span data-stu-id="ff424-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="ff424-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="ff424-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="ff424-162">Controlador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="ff424-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="ff424-163">HTML 3,0 o anterior</span><span class="sxs-lookup"><span data-stu-id="ff424-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="ff424-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="ff424-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="ff424-165">Controlador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="ff424-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="ff424-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="ff424-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="ff424-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="ff424-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="ff424-168">Controlador de filtro de texto sin formato</span><span class="sxs-lookup"><span data-stu-id="ff424-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="ff424-169">Archivos de texto sin formato: IFilter predeterminado</span><span class="sxs-lookup"><span data-stu-id="ff424-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="ff424-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="ff424-170">query.dll</span></span>    |
| [<span data-ttu-id="ff424-171">Controlador de filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="ff424-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="ff424-172">Archivos binarios: IFilter nulo</span><span class="sxs-lookup"><span data-stu-id="ff424-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="ff424-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="ff424-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="ff424-174">Controlador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="ff424-174">MIME Filter Handler</span></span>

<span data-ttu-id="ff424-175">El controlador de filtro MIME (en mimefilt.dll) extrae información de texto y propiedades de los archivos con las extensiones. eml,. mht y. MHTML.</span><span class="sxs-lookup"><span data-stu-id="ff424-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="ff424-176">Controlador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="ff424-176">HTML Filter Handler</span></span>

<span data-ttu-id="ff424-177">El controlador de filtro HTML (en nlhtml.dll) extrae información de texto y propiedades de la clase "htmlfiles" para que Windows Search pueda indizarla.</span><span class="sxs-lookup"><span data-stu-id="ff424-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="ff424-178">Para obtener una descripción de la asociación entre el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el tipo de archivo, vea "buscar el archivo dll de IFilter para un archivo" en [registrar controladores de filtro](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ff424-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="ff424-179">Puede usar la `META` característica de etiqueta de los documentos HTML para transmitir solicitudes de control especiales al [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML.</span><span class="sxs-lookup"><span data-stu-id="ff424-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="ff424-180">`META` las etiquetas se producen cerca del principio de un archivo HTML dentro de las `HEAD ... /HEAD` etiquetas, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ff424-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="ff424-181">Algunas `META` etiquetas HTML se asignan automáticamente a los valores del conjunto de propiedades y del identificador de propiedad (identificador de propiedad (PID)) de forma que las consultas en estas propiedades buscarán en el contenido asignado.</span><span class="sxs-lookup"><span data-stu-id="ff424-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="ff424-182">En la tabla siguiente se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="ff424-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="ff424-183">Para obtener una lista de las propiedades del sistema que puede usar para los formatos de archivo, consulte [propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="ff424-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="ff424-184">Ejemplo de propiedad</span><span class="sxs-lookup"><span data-stu-id="ff424-184">Property example</span></span>                              | <span data-ttu-id="ff424-185">Asignada a</span><span class="sxs-lookup"><span data-stu-id="ff424-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ff424-186">meta name = "author" Content = "Ruth"</span><span class="sxs-lookup"><span data-stu-id="ff424-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="ff424-187">Propiedad de autor del conjunto de propiedades de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="ff424-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="ff424-188">meta name = "Subject" Content = "procesamiento de texto"</span><span class="sxs-lookup"><span data-stu-id="ff424-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="ff424-189">Propiedad de asunto del conjunto de propiedades de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="ff424-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="ff424-190">meta name = "keywords" Content = "fuentes, Serif"</span><span class="sxs-lookup"><span data-stu-id="ff424-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="ff424-191">Propiedad de palabra clave en el conjunto de propiedades de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="ff424-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="ff424-192">meta name = "MS. Category" Content = "ficción"</span><span class="sxs-lookup"><span data-stu-id="ff424-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="ff424-193">Propiedad de categoría del conjunto de propiedades información de resumen del documento.</span><span class="sxs-lookup"><span data-stu-id="ff424-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="ff424-194">En la tabla siguiente se enumeran algunas características de HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="ff424-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Esta tabla debe ser HTML para que las muestras estén formateadas correctamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff424-196">Tarea</span><span class="sxs-lookup"><span data-stu-id="ff424-196">Task</span></span></th>
<th><span data-ttu-id="ff424-197">Acción</span><span class="sxs-lookup"><span data-stu-id="ff424-197">Action</span></span></th>
<th><span data-ttu-id="ff424-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff424-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff424-199">Crear resúmenes especiales de archivos</span><span class="sxs-lookup"><span data-stu-id="ff424-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="ff424-200">Use la <code>META NAME=&quot;DESCRIPTION&quot;...</code> etiqueta para indicar al <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> que use la cadena que sigue a la <code>CONTENT</code> palabra clave como resumen del documento.</span><span class="sxs-lookup"><span data-stu-id="ff424-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ff424-201">El proceso de filtrado puede generar resúmenes para cada archivo filtrado, que de forma predeterminada es un juego de caracteres al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff424-202">Impedir que se filtren archivos individuales</span><span class="sxs-lookup"><span data-stu-id="ff424-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="ff424-203">Agregue una <code>meta name</code> etiqueta al archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff424-204">Establecer el código de idioma de un archivo (para asegurarse de que el sistema elige los separadores de palabras de idioma correctos y los archivos de palabras irrelevantes)</span><span class="sxs-lookup"><span data-stu-id="ff424-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="ff424-205">Agregue la siguiente <code>meta name</code> etiqueta al archivo, donde el campo de contenido especifica el código de idioma adecuado (en caracteres o mediante el valor de configuración regional).</span><span class="sxs-lookup"><span data-stu-id="ff424-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="ff424-206">Controlador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="ff424-206">Document Filter Handler</span></span>

<span data-ttu-id="ff424-207">El controlador de filtro de documento (en offilt.dll) filtra los archivos de algunas extensiones de documentos en Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ff424-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="ff424-208">Estos archivos de inclusión con las extensiones. doc,. mdb,. ppt y. xlt, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ff424-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="ff424-209">Controlador de filtro de texto sin formato</span><span class="sxs-lookup"><span data-stu-id="ff424-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="ff424-210">En el caso de los archivos de texto sin formato, Windows Search utiliza el controlador de filtro de texto, que filtra las propiedades del sistema (por ejemplo, los nombres de archivo) y el contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="ff424-211">Cuando un tipo de archivo no tiene una asociación [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el registro, Windows Search solo indiza las propiedades del shell para el archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="ff424-212">Sin embargo, el usuario puede usar las **Opciones avanzadas** del panel de control **Opciones de indización** para **indizar propiedades** o **índices, así** como el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![captura de pantalla que muestra el cuadro de diálogo Opciones avanzadas](images/ifilteradvancedoptions.png)

<span data-ttu-id="ff424-214">Si el usuario elige esta opción para un tipo de archivo sin un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)asociado, el controlador de filtro de texto se utiliza para extraer el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="ff424-215">El controlador de filtro de texto no entiende ningún formato de documento; al filtrar el contenido de un archivo, trata el archivo como una secuencia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ff424-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="ff424-216">Comprueba la marca de orden de bytes Unicode al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ff424-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="ff424-217">Controlador de filtro binario o null</span><span class="sxs-lookup"><span data-stu-id="ff424-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="ff424-218">Cuando se encuentra un archivo binario registrado, se utiliza el controlador de filtro null.</span><span class="sxs-lookup"><span data-stu-id="ff424-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="ff424-219">El controlador de filtro null solo recupera las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="ff424-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="ff424-220">El contenido de un archivo binario no se filtra.</span><span class="sxs-lookup"><span data-stu-id="ff424-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="ff424-221">Ejemplos de propiedades del sistema son **filename**, **LastWriteTime**, **archivo** y **atributos**.</span><span class="sxs-lookup"><span data-stu-id="ff424-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff424-222">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ff424-222">Additional Resources</span></span>

- <span data-ttu-id="ff424-223">En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="ff424-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="ff424-224">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ff424-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="ff424-225">Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ff424-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="ff424-226">Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff424-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff424-227">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff424-227">Related topics</span></span>

[<span data-ttu-id="ff424-228">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="ff424-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="ff424-229">Acerca de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="ff424-230">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="ff424-231">Devolver propiedades de un controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="ff424-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="ff424-232">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="ff424-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="ff424-233">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="ff424-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="ff424-234">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="ff424-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

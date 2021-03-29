---
description: Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Prácticas recomendadas para los controladores de filtro en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540742"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="a6895-103">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6895-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="a6895-104">Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="a6895-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="a6895-105">Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo controladores de filtro para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.</span><span class="sxs-lookup"><span data-stu-id="a6895-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="a6895-106">Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="a6895-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="a6895-107">Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.</span><span class="sxs-lookup"><span data-stu-id="a6895-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="a6895-108">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="a6895-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a6895-109">Código nativo</span><span class="sxs-lookup"><span data-stu-id="a6895-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="a6895-110">Prácticas de código seguro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6895-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="a6895-111">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a6895-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a6895-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6895-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="a6895-113">Código nativo</span><span class="sxs-lookup"><span data-stu-id="a6895-113">Native Code</span></span>

<span data-ttu-id="a6895-114">En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente.</span><span class="sxs-lookup"><span data-stu-id="a6895-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="a6895-115">Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan varios complementos.</span><span class="sxs-lookup"><span data-stu-id="a6895-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="a6895-116">Prácticas de código seguro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6895-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="a6895-117">A continuación se indican los procedimientos para escribir aplicaciones seguras para su uso con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="a6895-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="a6895-118">**Para las aplicaciones de consulta:**</span><span class="sxs-lookup"><span data-stu-id="a6895-118">**For query applications:**</span></span>

-   <span data-ttu-id="a6895-119">Al escribir clientes de búsqueda, debe elegir la API que se ejecuta en un contexto de seguridad que permite al usuario el privilegio mínimo.</span><span class="sxs-lookup"><span data-stu-id="a6895-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="a6895-120">Por ejemplo, las páginas ASP pueden utilizar el objeto de consulta IXSSO, que se ejecuta como un proceso de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6895-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="a6895-121">**Para IFilters y recursos de idioma:**</span><span class="sxs-lookup"><span data-stu-id="a6895-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="a6895-122">Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="a6895-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="a6895-123">No hay ningún mecanismo para encadenar filtros.</span><span class="sxs-lookup"><span data-stu-id="a6895-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="a6895-124">Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.</span><span class="sxs-lookup"><span data-stu-id="a6895-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="a6895-125">Los IFilters, los separadores de palabras y lematizadores para Windows Search se ejecutan en el contexto de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="a6895-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="a6895-126">Se deben escribir para administrar los búferes y para apilarlos correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6895-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="a6895-127">Todas las copias de cadena deben tener comprobaciones explícitas para evitar las saturaciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="a6895-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="a6895-128">Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con respecto al tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="a6895-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="a6895-129">Las saturaciones de búfer son una técnica común para aprovechar el código que no impone restricciones de tamaño de búfer.</span><span class="sxs-lookup"><span data-stu-id="a6895-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="a6895-130">Los componentes de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palabras y lingüísticos nunca deben llamar a la función de [función ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o a una API similar que termine un proceso y todos sus subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a6895-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="a6895-131">No asigne ni libere recursos en el punto de entrada de DllMain.</span><span class="sxs-lookup"><span data-stu-id="a6895-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="a6895-132">Esto puede conducir a errores durante las pruebas de esfuerzo de recursos insuficientes.</span><span class="sxs-lookup"><span data-stu-id="a6895-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="a6895-133">Codifique todos los objetos para que sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a6895-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="a6895-134">Windows Search llama a cualquier instancia de un separador de palabras o un analizador lingüístico en un subproceso cada vez, pero puede llamar a varias instancias al mismo tiempo en varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a6895-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="a6895-135">Evite la creación de archivos temporales o la escritura en el registro.</span><span class="sxs-lookup"><span data-stu-id="a6895-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="a6895-136">Si usa el compilador Microsoft Visual C++, asegúrese de compilar la aplicación con la opción **/GS** .</span><span class="sxs-lookup"><span data-stu-id="a6895-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="a6895-137">La opción **/GS** se usa para detectar saturaciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="a6895-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="a6895-138">La opción/GS coloca las comprobaciones de seguridad en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="a6895-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="a6895-139">Para obtener más información, vea la [función de DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (comprobación de seguridad del búfer) en la sección de opciones del compilador Visual C++ del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a6895-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6895-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a6895-140">Additional Resources</span></span>

-   <span data-ttu-id="a6895-141">En el ejemplo [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a6895-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="a6895-142">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a6895-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="a6895-143">Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a6895-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="a6895-144">Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6895-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6895-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6895-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6895-146">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a6895-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="a6895-147">Acerca de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6895-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="a6895-148">Devolver propiedades de un controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="a6895-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="a6895-149">Controladores de filtro que se distribuyen con Windows</span><span class="sxs-lookup"><span data-stu-id="a6895-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="a6895-150">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a6895-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="a6895-151">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a6895-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="a6895-152">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a6895-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 

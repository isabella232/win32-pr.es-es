---
description: Obtenga información sobre los procedimientos recomendados para crear controladores de filtro en Windows Search. La búsqueda usa filtros para extraer elementos para su inclusión en un índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Procedimientos recomendados para los controladores de filtros en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a864cb2651d6236a212f3bf356eed3380869284
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989310"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="f5883-104">Procedimientos recomendados para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="f5883-104">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="f5883-105">Microsoft Windows Search filtros para extraer el contenido de los elementos para su inclusión en un índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="f5883-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="f5883-106">Puede ampliar Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo controladores de filtro para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.</span><span class="sxs-lookup"><span data-stu-id="f5883-106">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="f5883-107">Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLID).</span><span class="sxs-lookup"><span data-stu-id="f5883-107">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="f5883-108">Aunque un filtro puede controlar varios tipos de archivo, cada tipo funciona con un solo filtro.</span><span class="sxs-lookup"><span data-stu-id="f5883-108">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="f5883-109">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f5883-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f5883-110">Código nativo</span><span class="sxs-lookup"><span data-stu-id="f5883-110">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="f5883-111">Prácticas de código seguro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="f5883-111">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="f5883-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f5883-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="f5883-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5883-113">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="f5883-114">Código nativo</span><span class="sxs-lookup"><span data-stu-id="f5883-114">Native Code</span></span>

<span data-ttu-id="f5883-115">En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente.</span><span class="sxs-lookup"><span data-stu-id="f5883-115">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="f5883-116">Los filtros DEBEN escribirse en código nativo debido a posibles problemas de control de versiones clr con el proceso en el que se ejecutan varios complementos.</span><span class="sxs-lookup"><span data-stu-id="f5883-116">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="f5883-117">Prácticas de código seguro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="f5883-117">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="f5883-118">Estos son los procedimientos para escribir aplicaciones seguras para su uso con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="f5883-118">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="f5883-119">**Para aplicaciones de consulta:**</span><span class="sxs-lookup"><span data-stu-id="f5883-119">**For query applications:**</span></span>

-   <span data-ttu-id="f5883-120">Al escribir clientes de búsqueda, debe elegir la API que se ejecuta en un contexto de seguridad que permita al usuario tener menos privilegios.</span><span class="sxs-lookup"><span data-stu-id="f5883-120">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="f5883-121">Por ejemplo, las páginas ASP pueden usar el objeto de consulta IXSSO, que se ejecuta como un proceso de usuario.</span><span class="sxs-lookup"><span data-stu-id="f5883-121">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="f5883-122">**Para IFilters y recursos de lenguaje:**</span><span class="sxs-lookup"><span data-stu-id="f5883-122">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="f5883-123">Si se instala un nuevo controlador de filtro para un tipo de archivo como reemplazo de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5883-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="f5883-124">No hay ningún mecanismo para encadenar filtros.</span><span class="sxs-lookup"><span data-stu-id="f5883-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="f5883-125">Por lo tanto, el nuevo controlador de filtros es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.</span><span class="sxs-lookup"><span data-stu-id="f5883-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="f5883-126">Los IFilters, separadores de palabras y lematizadores Windows Search ejecutar en el contexto de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="f5883-126">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="f5883-127">Se deben escribir para administrar búferes y para apilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5883-127">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="f5883-128">Todas las copias de cadena deben tener comprobaciones explícitas para protegerse frente a saturaciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="f5883-128">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="f5883-129">Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="f5883-129">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="f5883-130">Las saturaciones de búfer son una técnica común para aprovechar el código que no aplica restricciones de tamaño de búfer.</span><span class="sxs-lookup"><span data-stu-id="f5883-130">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="f5883-131">[**Los componentes IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palabras y lematizador nunca deben llamar a la función [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ni a una API similar que finalice un proceso y todos sus subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f5883-131">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="f5883-132">No asigne ni libre recursos en el punto de entrada de DllMain.</span><span class="sxs-lookup"><span data-stu-id="f5883-132">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="f5883-133">Esto puede provocar errores durante las pruebas de esfuerzo de pocos recursos.</span><span class="sxs-lookup"><span data-stu-id="f5883-133">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="f5883-134">Codifie todos los objetos para que sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f5883-134">Code all objects to be thread-safe.</span></span> <span data-ttu-id="f5883-135">Windows Search llama a cualquier instancia de un separador de palabras o lematizador en un subproceso a la vez, pero puede llamar a varias instancias al mismo tiempo en varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f5883-135">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="f5883-136">Evite crear archivos temporales o escribir en el Registro.</span><span class="sxs-lookup"><span data-stu-id="f5883-136">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="f5883-137">Si usa la compilador de Microsoft Visual C++, asegúrese de compilar la aplicación mediante la **opción /GS.**</span><span class="sxs-lookup"><span data-stu-id="f5883-137">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="f5883-138">La **opción /GS** se usa para detectar saturaciones de búfer.</span><span class="sxs-lookup"><span data-stu-id="f5883-138">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="f5883-139">La opción /GS coloca las comprobaciones de seguridad en el código compilado.</span><span class="sxs-lookup"><span data-stu-id="f5883-139">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="f5883-140">Para obtener más información, vea [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / GS (Buffer Security Check) (DllGetClassObject Function **GS** [Comprobación de seguridad del búfer]) en la Visual C++ Opciones del compilador del SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="f5883-140">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5883-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f5883-141">Additional Resources</span></span>

-   <span data-ttu-id="f5883-142">En [el ejemplo IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) se muestra cómo crear una clase base IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="f5883-142">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="f5883-143">Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5883-143">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="f5883-144">Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f5883-144">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="f5883-145">Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Registro de aplicaciones.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5883-145">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5883-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5883-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5883-147">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="f5883-147">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="f5883-148">Acerca de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="f5883-148">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="f5883-149">Devolver propiedades de un controlador de filtros</span><span class="sxs-lookup"><span data-stu-id="f5883-149">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="f5883-150">Controladores de filtro que se envían con Windows</span><span class="sxs-lookup"><span data-stu-id="f5883-150">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="f5883-151">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="f5883-151">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="f5883-152">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="f5883-152">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="f5883-153">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="f5883-153">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 

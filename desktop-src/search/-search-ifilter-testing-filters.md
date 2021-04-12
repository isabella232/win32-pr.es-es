---
description: El conjunto de pruebas de IFilter valida los controladores de filtro.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Probar controladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153969"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="404f4-103">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="404f4-103">Testing Filter Handlers</span></span>

<span data-ttu-id="404f4-104">El conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valida los controladores de filtro.</span><span class="sxs-lookup"><span data-stu-id="404f4-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="404f4-105">El conjunto de pruebas lo hace mediante la llamada a métodos de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y la comprobación de los valores devueltos para la compatibilidad con la especificación de interfaz de **IFilter** ; y comprobar que los identificadores de fragmentos son únicos y aumentan, que la interfaz de **IFilter** se comporta de forma coherente después de la reinicialización, y que las llamadas a métodos de **IFilter** con parámetros no válidos devuelven los códigos de error esperados.</span><span class="sxs-lookup"><span data-stu-id="404f4-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="404f4-106">Los programas del conjunto de pruebas también vuelcan la salida de un archivo filtrado por un controlador de filtro y comprueban la información de registro de **IFilter** en el registro.</span><span class="sxs-lookup"><span data-stu-id="404f4-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="404f4-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="404f4-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="404f4-108">Invocación de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="404f4-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="404f4-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="404f4-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="404f4-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="404f4-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="404f4-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="404f4-113">Procedimiento de prueba de IFilter</span><span class="sxs-lookup"><span data-stu-id="404f4-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="404f4-114">Prueba de validación</span><span class="sxs-lookup"><span data-stu-id="404f4-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="404f4-115">Prueba de coherencia</span><span class="sxs-lookup"><span data-stu-id="404f4-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="404f4-116">Prueba de entrada no válida</span><span class="sxs-lookup"><span data-stu-id="404f4-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="404f4-117">Probar diferentes configuraciones de IFilter</span><span class="sxs-lookup"><span data-stu-id="404f4-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="404f4-118">Asegurarse de que los elementos registrados se indexan</span><span class="sxs-lookup"><span data-stu-id="404f4-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="404f4-119">Archivo de registro de ejemplo</span><span class="sxs-lookup"><span data-stu-id="404f4-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="404f4-120">Archivo de volcado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="404f4-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="404f4-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="404f4-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="404f4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="404f4-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="404f4-123">Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="404f4-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="404f4-124">No hay ningún mecanismo para encadenar filtros.</span><span class="sxs-lookup"><span data-stu-id="404f4-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="404f4-125">Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.</span><span class="sxs-lookup"><span data-stu-id="404f4-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="404f4-126">Invocación de Command-Line</span><span class="sxs-lookup"><span data-stu-id="404f4-126">Command-Line Invocation</span></span>

<span data-ttu-id="404f4-127">El conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) consta de tres aplicaciones de línea de comandos: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)y [filtreg.exe](#filtregexe) y un archivo de inicialización, [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="404f4-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="404f4-128">En Windows 7 y versiones posteriores, los filtros escritos en código administrado se bloquean explícitamente.</span><span class="sxs-lookup"><span data-stu-id="404f4-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="404f4-129">Los filtros se deben escribir en código nativo debido a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.</span><span class="sxs-lookup"><span data-stu-id="404f4-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="404f4-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-130">ifilttst.exe</span></span>

<span data-ttu-id="404f4-131">El programa ifilttst.exe ejecuta varias pruebas para validar un controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="404f4-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="404f4-132">En el ejemplo siguiente se muestra cómo invocar el programa ifilttst.exe desde la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="404f4-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="404f4-133">En el ejemplo se realizan las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="404f4-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="404f4-134">Indica al programa que filtre el archivo test.htm</span><span class="sxs-lookup"><span data-stu-id="404f4-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="404f4-135">Redirige los mensajes de registro a test.htm. log.</span><span class="sxs-lookup"><span data-stu-id="404f4-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="404f4-136">Redirige los mensajes de volcado a test.htm. DMP</span><span class="sxs-lookup"><span data-stu-id="404f4-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="404f4-137">Establece el nivel de detalle en 1</span><span class="sxs-lookup"><span data-stu-id="404f4-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="404f4-138">Para que el comando anterior funcione, se deben encontrar tres archivos en el directorio de trabajo actual: `test.htm` , [ifilttst.exe](#ifilttstexe)y [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="404f4-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="404f4-139">Los modificadores de la línea de comandos se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="404f4-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="404f4-140">Modificador y posibles variables</span><span class="sxs-lookup"><span data-stu-id="404f4-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="404f4-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="404f4-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="404f4-142"><strong>/i nombre de archivo</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="404f4-143">El archivo o directorio de entrada que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="404f4-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="404f4-144">El nombre de archivo puede contener los caracteres comodín <code>\*</code> y <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="404f4-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="404f4-145"><strong>l</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="404f4-146">Los mensajes de registro se dirigen a un archivo en lugar de a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="404f4-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="404f4-147">Los mensajes de registro describen las pruebas individuales realizadas y los resultados de superación y error de las pruebas.</span><span class="sxs-lookup"><span data-stu-id="404f4-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="404f4-148">El nombre del archivo de registro es el mismo que el nombre del archivo de entrada, pero con la extensión. log.</span><span class="sxs-lookup"><span data-stu-id="404f4-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="404f4-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="404f4-150">Los mensajes de volcado de memoria se dirigen a un archivo en lugar de a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="404f4-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="404f4-151">Los mensajes de volcado describen el contenido de los fragmentos.</span><span class="sxs-lookup"><span data-stu-id="404f4-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="404f4-152">La estructura de fragmentos se vuelca cuando el nivel de detalle es 3.</span><span class="sxs-lookup"><span data-stu-id="404f4-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="404f4-153">El nombre del archivo de volcado es el mismo que el nombre del archivo de entrada, pero con una extensión. DMP.</span><span class="sxs-lookup"><span data-stu-id="404f4-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="404f4-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="404f4-155">Deshabilitar el registro.</span><span class="sxs-lookup"><span data-stu-id="404f4-155">Disable logging.</span></span> <span data-ttu-id="404f4-156">Esta marca invalida el <code>/l</code> modificador.</span><span class="sxs-lookup"><span data-stu-id="404f4-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="404f4-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="404f4-158">Deshabilite el volcado.</span><span class="sxs-lookup"><span data-stu-id="404f4-158">Disable dumping.</span></span> <span data-ttu-id="404f4-159">Esta marca invalida el <code>/d</code> modificador.</span><span class="sxs-lookup"><span data-stu-id="404f4-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="404f4-160"><strong>/v (entero)</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="404f4-161">Nivel de detalle.</span><span class="sxs-lookup"><span data-stu-id="404f4-161">The verbosity level.</span></span> <span data-ttu-id="404f4-162">El valor predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="404f4-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="404f4-163">0: la prueba solo registra mensajes relativos a errores específicos de la interfaz de <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="404f4-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="404f4-164">La prueba vuelca el contenido del fragmento.</span><span class="sxs-lookup"><span data-stu-id="404f4-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="404f4-165">1-la prueba registra los mensajes de advertencia y los del nivel 0.</span><span class="sxs-lookup"><span data-stu-id="404f4-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="404f4-166">2-la prueba registra mensajes relativos a las pruebas superadas, así como a las de nivel 1.</span><span class="sxs-lookup"><span data-stu-id="404f4-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="404f4-167">3-la prueba registra los mensajes informativos, así como los de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="404f4-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="404f4-168">Además, la prueba vuelca la estructura del fragmento.</span><span class="sxs-lookup"><span data-stu-id="404f4-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="404f4-169"><strong>/t (entero)</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="404f4-170">Número de subprocesos que se van a iniciar.</span><span class="sxs-lookup"><span data-stu-id="404f4-170">The number of threads to launch.</span></span> <span data-ttu-id="404f4-171">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="404f4-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="404f4-172"><strong>/r (entero</strong>)]</span><span class="sxs-lookup"><span data-stu-id="404f4-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="404f4-173">Filtra subdirectorios de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="404f4-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="404f4-174">El parámetro de entero opcional especifica la profundidad a la que se debe ejercitar la recursividad.</span><span class="sxs-lookup"><span data-stu-id="404f4-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="404f4-175">Si no se especifica ningún entero, o si el entero es 0, se asume la recursividad completa.</span><span class="sxs-lookup"><span data-stu-id="404f4-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="404f4-176">De forma predeterminada, la profundidad de recursividad es 1.</span><span class="sxs-lookup"><span data-stu-id="404f4-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="404f4-177"><strong>/c entero</strong></span><span class="sxs-lookup"><span data-stu-id="404f4-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="404f4-178">Número de veces que se va a crear un bucle.</span><span class="sxs-lookup"><span data-stu-id="404f4-178">The number of times to loop.</span></span> <span data-ttu-id="404f4-179">Si el entero es 0, la prueba se repite infinitamente.</span><span class="sxs-lookup"><span data-stu-id="404f4-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="404f4-180">De forma predeterminada, la prueba se repite solo una vez.</span><span class="sxs-lookup"><span data-stu-id="404f4-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="404f4-181">Debe incluir un espacio entre el modificador de la línea de comandos y el valor.</span><span class="sxs-lookup"><span data-stu-id="404f4-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="404f4-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-182">filtdump.exe</span></span>

<span data-ttu-id="404f4-183">El programa filtdump.exe carga un controlador de filtro para un documento especificado e imprime el resultado generado por el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="404f4-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="404f4-184">En el ejemplo siguiente se muestra cómo invocar el programa filtdump.exe.</span><span class="sxs-lookup"><span data-stu-id="404f4-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="404f4-185">Filtdump.exe usa el método [ILoadFilter:: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) para cargar el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) adecuado para la extensión de nombre de archivo especificada e imprime los resultados.</span><span class="sxs-lookup"><span data-stu-id="404f4-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="404f4-186">Por ejemplo, el comando siguiente indica a filtdump.exe que cargue el controlador de filtro de smpfilt.dll para la extensión. SMP, extraiga todo el texto y las propiedades del archivo Perfile. SMP e imprima los resultados.</span><span class="sxs-lookup"><span data-stu-id="404f4-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="404f4-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="404f4-187">filtreg.exe</span></span>

<span data-ttu-id="404f4-188">El programa filtreg.exe inspecciona la información de instalación de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) en el registro.</span><span class="sxs-lookup"><span data-stu-id="404f4-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="404f4-189">Para invocar el programa filtreg.exe desde la línea de comandos, escriba su nombre, como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="404f4-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="404f4-190">En Filtreg.exe se enumeran todas las extensiones de nombre de archivo que tienen controladores de filtros asociados mediante la impresión de la extensión de nombre de archivo y el nombre del archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de la extensión.</span><span class="sxs-lookup"><span data-stu-id="404f4-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="404f4-191">Se trata de una manera sencilla de comprobar la instalación correcta de un **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="404f4-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="404f4-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="404f4-192">ifilttst.ini</span></span>

<span data-ttu-id="404f4-193">Una interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se inicializa llamando al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="404f4-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="404f4-194">El método **IFilter:: init** toma los cuatro parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="404f4-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="404f4-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="404f4-195">*grfFlags*</span></span>
2. <span data-ttu-id="404f4-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="404f4-196">*cAttributes*</span></span>
3. <span data-ttu-id="404f4-197">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="404f4-197">*aAttributes*</span></span>
4. <span data-ttu-id="404f4-198">*pdwFlags*</span><span class="sxs-lookup"><span data-stu-id="404f4-198">*pdwFlags*</span></span>

<span data-ttu-id="404f4-199">El usuario del programa ifilttst.exe del conjunto de pruebas de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) puede especificar los valores de estos parámetros en un archivo denominado ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="404f4-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="404f4-200">En la tabla siguiente se describen las entradas del archivo de ifilttst.ini que especifican los tres primeros parámetros (los parámetros de entrada).</span><span class="sxs-lookup"><span data-stu-id="404f4-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="404f4-201">Para obtener un archivo de ejemplo, vea [archivo de ifilttst.ini de ejemplo](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="404f4-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="404f4-202">No hay ninguna entrada de tabla para el parámetro *pdwFlags* porque es un parámetro de salida. no es necesario que tenga ningún valor especial antes de la llamada al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="404f4-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="404f4-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="404f4-203">Entry</span></span>         | <span data-ttu-id="404f4-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="404f4-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="404f4-205">Marcas</span><span class="sxs-lookup"><span data-stu-id="404f4-205">Flags</span></span>         | <span data-ttu-id="404f4-206">Los nombres de las marcas de [**\_ inicialización IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) que van a estar unidas por el operador o para formar el parámetro *grfFlags* del método [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="404f4-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="404f4-207">Los nombres de las marcas deben estar en mayúsculas y en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="404f4-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="404f4-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="404f4-208">*cAttributes*</span></span> | <span data-ttu-id="404f4-209">Entero decimal que representa el valor del parámetro *cAttributes* .</span><span class="sxs-lookup"><span data-stu-id="404f4-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="404f4-210">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="404f4-210">*aAttributes*</span></span> | <span data-ttu-id="404f4-211">Esta entrada debe comenzar con *aAttributes* y debe ser diferente de las demás entradas de *aAttributes* dentro de la sección.</span><span class="sxs-lookup"><span data-stu-id="404f4-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="404f4-212">Los nombres válidos para la entrada *aAttributes* son: *aAttributes*, *aAttributes1*, *aAttributes2*, etc.</span><span class="sxs-lookup"><span data-stu-id="404f4-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="404f4-213">El primer token debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="404f4-213">The first token must be a GUID.</span></span> <span data-ttu-id="404f4-214">Se debe dar formato al GUID exactamente como se muestra en la `[Test3]` sección del [archivo de ifilttst.ini de ejemplo](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="404f4-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="404f4-215">El segundo token puede ser un identificador de propiedad (PID) que consta de un número en notación hexadecimal o un puntero a una cadena de caracteres anchos (LPWStr).</span><span class="sxs-lookup"><span data-stu-id="404f4-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="404f4-216">Se puede especificar LPWStr mediante la inclusión de la cadena entre comillas dobles, como se muestra en la `[Test6]` sección del archivo de ifilttst.ini de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="404f4-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="404f4-217">Si no se especifican las entradas flags y *cAttributes* , el valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="404f4-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="404f4-218">Si establece *cAttributes* en 2, debe especificar dos nombres de *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="404f4-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="404f4-219">En la `[Test5]` sección del ejemplo, *cAttributes* es 1, pero no se ha especificado ningún *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="404f4-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="404f4-220">Después, la prueba llama al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) con *cAttributes* igual a 1 y *aAttributes* igual a **null**.</span><span class="sxs-lookup"><span data-stu-id="404f4-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="404f4-221">Este es un caso de prueba útil porque es probable que provoque una infracción de acceso en el método **IFilter:: init** .</span><span class="sxs-lookup"><span data-stu-id="404f4-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="404f4-222">Si ifilttst.exe no encuentra un archivo denominado ifilttst.ini en el directorio de trabajo, se usa una configuración predeterminada para inicializar el objeto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="404f4-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="404f4-223">En el ejemplo siguiente se muestra la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="404f4-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="404f4-224">Archivo de ifilttst.ini de ejemplo</span><span class="sxs-lookup"><span data-stu-id="404f4-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="404f4-225">El archivo ifilttst.ini se organiza en secciones, con el nombre de sección entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="404f4-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="404f4-226">En el ejemplo, las secciones se denominan `[Test1]` , `[Test2]` , y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="404f4-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="404f4-227">Todos los nombres de sección deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="404f4-227">All section names must be unique.</span></span> <span data-ttu-id="404f4-228">La prueba Lee los valores de la primera sección e inicializa el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con esos valores.</span><span class="sxs-lookup"><span data-stu-id="404f4-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="404f4-229">Después, todas las pruebas se ejecutan con esta configuración de **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="404f4-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="404f4-230">A continuación, se libera y se reinicializa el **IFilter** , con los parámetros que se enumeran anteriormente.</span><span class="sxs-lookup"><span data-stu-id="404f4-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="404f4-231">El proceso se repite hasta que se prueban todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="404f4-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="404f4-232">Procedimiento de prueba de IFilter</span><span class="sxs-lookup"><span data-stu-id="404f4-232">IFilter Test Procedure</span></span>

<span data-ttu-id="404f4-233">Una vez inicializado el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , el programa ifilttst.exe realiza una serie de pruebas en el **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="404f4-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="404f4-234">Además de seguir los procedimientos de prueba de **IFilter** , asegúrese de que la implementación de **IFilter** emplea prácticas de código seguro.</span><span class="sxs-lookup"><span data-stu-id="404f4-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="404f4-235">Consulte "prácticas de código seguro para Windows Search" en [implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="404f4-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="404f4-236">Prueba de validación</span><span class="sxs-lookup"><span data-stu-id="404f4-236">Validation Test</span></span>

<span data-ttu-id="404f4-237">La prueba de validación recorre el objeto un fragmento cada vez, comprobando cada fragmento individual y todos los códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="404f4-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="404f4-238">La prueba de validación guarda todas las estructuras de [**\_ fragmentos de estadísticas**](/windows/win32/api/filter/ns-filter-stat_chunk) devueltas en una lista.</span><span class="sxs-lookup"><span data-stu-id="404f4-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="404f4-239">La prueba de validación comprueba las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="404f4-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="404f4-240">[**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.\*\* los identificadores de fragmentos de idChunk deben ser únicos y aumentar.</span><span class="sxs-lookup"><span data-stu-id="404f4-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="404f4-241">[**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.*el parámetro flags* es un estado de fragmento reconocido, como [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), \_ texto de fragmento o \_ constantes de valor CenabledHUNK.</span><span class="sxs-lookup"><span data-stu-id="404f4-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="404f4-242">[**\_ Fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk)de la estadística.\*\* el parámetro breakType es un tipo de interrupción reconocido (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="404f4-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="404f4-243">Si los atributos de inicialización de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) especifican que el **IFilter** debe devolver solo fragmentos que contienen propiedades internas de tipo de valor, *idChunkSource* debe ser igual a 0.</span><span class="sxs-lookup"><span data-stu-id="404f4-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="404f4-244">Si el fragmento no se deriva, es decir, si no es una propiedad de tipo de valor interna, se [**declarará \_ fragmento**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* debe ser igual al **\_ fragmento STAT**.*idChunk*.</span><span class="sxs-lookup"><span data-stu-id="404f4-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="404f4-245">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S \_ o cualquier otro valor de retorno aceptable, como filtro \_ e \_ fin \_ de \_ fragmentos, filtro \_ e \_ vínculo \_ no disponible, etc.</span><span class="sxs-lookup"><span data-stu-id="404f4-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="404f4-246">Si el fragmento contiene texto, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve s \_ correcto, filtrar el \_ \_ último \_ texto o filtrar \_ E \_ no \_ más \_ texto.</span><span class="sxs-lookup"><span data-stu-id="404f4-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="404f4-247">Si [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve \_ \_ \_ el último texto del filtro, la siguiente llamada a **IFILTER:: gettext** devuelve el filtro \_ E \_ ningún \_ \_ texto más.</span><span class="sxs-lookup"><span data-stu-id="404f4-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="404f4-248">Si el fragmento contiene un valor, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve d \_ o el filtro \_ E \_ no tiene \_ más \_ valores.</span><span class="sxs-lookup"><span data-stu-id="404f4-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="404f4-249">Prueba de coherencia</span><span class="sxs-lookup"><span data-stu-id="404f4-249">Consistency Test</span></span>

<span data-ttu-id="404f4-250">El programa ifilttxt.exe reinicializa la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros que en la prueba de validación y realiza una prueba de coherencia.</span><span class="sxs-lookup"><span data-stu-id="404f4-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="404f4-251">Si la implementación de **IFilter** se ha inicializado con la marca [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ Indexing \_ Only, la prueba libera la interfaz **IFilter** y la vuelve a enlazar antes de realizar otra llamada al método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="404f4-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="404f4-252">La prueba de coherencia comprueba las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="404f4-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="404f4-253">Cada estructura de [**\_ fragmentos de estadísticas**](/windows/win32/api/filter/ns-filter-stat_chunk) devuelta por el método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) es idéntica **al \_ fragmento de STAT** correspondiente devuelto en la prueba de validación.</span><span class="sxs-lookup"><span data-stu-id="404f4-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="404f4-254">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve S \_ o cualquier otro valor de retorno aceptable, como filtro \_ e \_ fin \_ de \_ fragmentos, filtro \_ e \_ vínculo \_ no disponible, etc.</span><span class="sxs-lookup"><span data-stu-id="404f4-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="404f4-255">Prueba de entrada no válida</span><span class="sxs-lookup"><span data-stu-id="404f4-255">Invalid Input Test</span></span>

<span data-ttu-id="404f4-256">El programa ifilttst.exe reinicializa la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) con los mismos parámetros y realiza una prueba de entrada no válida.</span><span class="sxs-lookup"><span data-stu-id="404f4-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="404f4-257">En esta prueba se recorre el documento un fragmento cada vez que realiza llamadas a funciones incorrectamente, por ejemplo, al llamar al método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) cuando el campo Chuck actual contiene texto.</span><span class="sxs-lookup"><span data-stu-id="404f4-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="404f4-258">La prueba comprueba la compatibilidad de todos los códigos de retorno con la especificación **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="404f4-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="404f4-259">La prueba de entrada no válida comprueba las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="404f4-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="404f4-260">Si el fragmento actual contiene texto, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve \_ \_ los valores Filter e no \_ , y una llamada a [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="404f4-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="404f4-261">Si el fragmento actual contiene un valor, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devuelve Filter \_ E \_ no \_ Text y una llamada a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="404f4-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="404f4-262">Si la llamada anterior a [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) devolvió el filtro \_ e \_ no hay \_ más \_ texto, las llamadas sucesivas a **IFilter:: gettext** devuelven el filtro \_ e \_ no hay \_ más \_ texto.</span><span class="sxs-lookup"><span data-stu-id="404f4-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="404f4-263">Si la llamada anterior a [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devolvió el filtro \_ e \_ no hay \_ más \_ valores, las llamadas sucesivas a **IFilter:: GetValue** devuelven el filtro \_ e \_ ningún \_ \_ valor más.</span><span class="sxs-lookup"><span data-stu-id="404f4-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="404f4-264">Si la llamada anterior a [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devolvió el filtro \_ e \_ final \_ de \_ fragmentos, las sucesivas llamadas a **IFilter:: GetChunk** devuelven el filtro \_ de devolución e \_ final \_ de los \_ fragmentos.</span><span class="sxs-lookup"><span data-stu-id="404f4-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="404f4-265">La prueba de entrada no válida compara las estructuras de fragmentos actuales con las devueltas en la prueba de validación para asegurarse de que son idénticas.</span><span class="sxs-lookup"><span data-stu-id="404f4-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="404f4-266">Probar diferentes configuraciones de IFilter</span><span class="sxs-lookup"><span data-stu-id="404f4-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="404f4-267">El programa ifilttst.exe libera la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y vuelve a enlazar, esta vez inicializándose con el siguiente conjunto de parámetros.</span><span class="sxs-lookup"><span data-stu-id="404f4-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="404f4-268">La prueba repite el ciclo: prueba de validación, prueba de coherencia y prueba de entrada no válida, hasta que se hayan probado todas las configuraciones de **IFilter** deseadas especificadas en [ifilttst.ini](#ifilttstini) archivo.</span><span class="sxs-lookup"><span data-stu-id="404f4-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="404f4-269">Asegurarse de que los elementos registrados se indexan</span><span class="sxs-lookup"><span data-stu-id="404f4-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="404f4-270">La prueba final de su [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantiza que su **IFilter** está correctamente registrado y que se invoca para indexar los elementos que ha registrado para usarlos.</span><span class="sxs-lookup"><span data-stu-id="404f4-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="404f4-271">Puede usar el administrador de catálogos para iniciar la reindización o usar el administrador de ámbito de rastreo (CSM) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador.</span><span class="sxs-lookup"><span data-stu-id="404f4-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="404f4-272">Una vez completada la indexación, use la interfaz de usuario de búsqueda de Windows para buscar una cadena en el contenido o las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="404f4-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="404f4-273">Si los elementos se indexaron, aparecerán en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="404f4-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="404f4-274">Para obtener más información acerca de la reindización, consulte [uso del administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md) y [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="404f4-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="404f4-275">En el ejemplo de código ReindexMatchingUrls se muestran las maneras de especificar qué archivos se van a volver a indizar y cómo.</span><span class="sxs-lookup"><span data-stu-id="404f4-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="404f4-276">En el ejemplo de código CrawlScopeCommandLine se muestra cómo definir las opciones de la línea de comandos para las operaciones de indización del administrador de ámbito de rastreo (CSM).</span><span class="sxs-lookup"><span data-stu-id="404f4-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="404f4-277">Ambos ejemplos de código están disponibles en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="404f4-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="404f4-278">Archivo de registro de ejemplo</span><span class="sxs-lookup"><span data-stu-id="404f4-278">Sample Log File</span></span>

<span data-ttu-id="404f4-279">Previa solicitud, el programa de Ifilttst.exe puede generar un registro que contenga una descripción de los pasos que se realizan durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="404f4-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="404f4-280">Los ejemplos siguientes son fragmentos de un archivo de registro, con el nivel de detalle establecido en el valor 3 más alto.</span><span class="sxs-lookup"><span data-stu-id="404f4-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="404f4-281">La primera línea es un mensaje informativo, que indica que se ha cargado una nueva configuración del archivo de ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="404f4-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="404f4-282">La línea (3) indica el nombre de la sección en el ifilttst.ini archivo desde el que se ha leído la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="404f4-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="404f4-283">Las líneas (4) a (7) muestran los parámetros en [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span><span class="sxs-lookup"><span data-stu-id="404f4-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="404f4-284">Las líneas que comienzan con `INFO` son mensajes informativos sobre el enlace del [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y el inicio de la prueba de validación.</span><span class="sxs-lookup"><span data-stu-id="404f4-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="404f4-285">Las líneas que comienzan con `PASS` son mensajes relativos a las pruebas específicas que se han superado.</span><span class="sxs-lookup"><span data-stu-id="404f4-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="404f4-286">La línea del siguiente ejemplo de registro es una advertencia.</span><span class="sxs-lookup"><span data-stu-id="404f4-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="404f4-287">Las advertencias informan sobre el comportamiento de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que es problemático, aunque es legal.</span><span class="sxs-lookup"><span data-stu-id="404f4-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="404f4-288">Esta advertencia indica que el método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) ha devuelto un fragmento de texto que no contiene texto.</span><span class="sxs-lookup"><span data-stu-id="404f4-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="404f4-289">El mensaje de error de ejemplo siguiente indica que el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento que no se solicitó.</span><span class="sxs-lookup"><span data-stu-id="404f4-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="404f4-290">En el caso de este mensaje de error de ejemplo, el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitió un fragmento con un PID de `0x5` .</span><span class="sxs-lookup"><span data-stu-id="404f4-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="404f4-291">La inspección de `[Test1]` la sección en ifilttst.ini mostraría que el **IFilter** se configuró para no emitir fragmentos con este PID.</span><span class="sxs-lookup"><span data-stu-id="404f4-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="404f4-292">Por ejemplo, si \_ \_ no se especifican los atributos IFilter init Apply de \_ Índice \_ ni IFilter \_ init \_ \_ \_ , se han especificado otros atributos en la entrada flags y, si *cAttributes* eran 0, **IFILTER** solo emitirá fragmentos con un PID de `0x13` y correspondiente al contenido de PID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="404f4-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="404f4-293">Archivo de volcado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="404f4-293">Sample Dump File</span></span>

<span data-ttu-id="404f4-294">Previa solicitud, el programa de Ifilttst.exe puede generar un volcado de memoria que contiene los fragmentos que encuentra y su contenido.</span><span class="sxs-lookup"><span data-stu-id="404f4-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="404f4-295">El ejemplo siguiente es un extracto de este archivo de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="404f4-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="404f4-296">Las nueve primeras líneas describen la estructura de fragmentos actual.</span><span class="sxs-lookup"><span data-stu-id="404f4-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="404f4-297">El GUID y el PID se corresponden con el contenido de PSGUID \_ Storage/PID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="404f4-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="404f4-298">Se trata de un fragmento que contiene texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="404f4-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="404f4-299">El texto está en la siguiente estructura de fragmentos:</span><span class="sxs-lookup"><span data-stu-id="404f4-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="404f4-300">El siguiente fragmento, a partir de la línea 11, tiene un GUID diferente, que corresponde a `HTML IFilter` , y un PID diferente, que corresponde a un elemento HTML href.</span><span class="sxs-lookup"><span data-stu-id="404f4-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="404f4-301">Se trata de una propiedad de tipo de valor interna, exportada por `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="404f4-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="404f4-302">El siguiente fragmento, a partir de la línea 21, tiene el mismo GUID y el mismo PID, pero su estado de fragmento es `VALUE` en lugar de `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="404f4-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="404f4-303">Tenga en cuenta que el texto de estos dos últimos fragmentos es el mismo que el del primer fragmento.</span><span class="sxs-lookup"><span data-stu-id="404f4-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="404f4-304">Pero como el [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) está diseñado para tres atributos (texto sin formato, HTML href como texto y HTML href como valor) para que se aplique a esta frase, los resultados se emiten en tres fragmentos independientes.</span><span class="sxs-lookup"><span data-stu-id="404f4-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="404f4-305">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="404f4-305">Additional Resources</span></span>

- <span data-ttu-id="404f4-306">En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="404f4-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="404f4-307">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="404f4-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="404f4-308">Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="404f4-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="404f4-309">Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="404f4-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="404f4-310">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="404f4-310">Related topics</span></span>

[<span data-ttu-id="404f4-311">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="404f4-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="404f4-312">Acerca de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="404f4-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="404f4-313">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="404f4-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="404f4-314">Devolver propiedades de un controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="404f4-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="404f4-315">Controladores de filtro que se distribuyen con Windows</span><span class="sxs-lookup"><span data-stu-id="404f4-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="404f4-316">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="404f4-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="404f4-317">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="404f4-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

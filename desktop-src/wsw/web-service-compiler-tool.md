---
title: Herramienta de compilador de servicio Web
description: Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se va a usar tanto en el cliente como en el servicio. Genera el archivo de proxy de C para el lado cliente y el archivo de código auxiliar de C para el servicio, según sea necesario.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Servicios Web de herramienta del compilador de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421650"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="ff4fc-107">Herramienta de compilador de servicio Web</span><span class="sxs-lookup"><span data-stu-id="ff4fc-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="ff4fc-108">Para admitir el modelo de servicio, wsutil.exe genera el encabezado que se va a usar tanto en el cliente como en el servicio.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="ff4fc-109">Genera el archivo de proxy de C para el lado cliente y el archivo de código auxiliar de C para el servicio, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="ff4fc-110">Para admitir la [serialización](serialization.md), el compilador genera encabezados para las descripciones de elementos de las definiciones de elementos globales y toda la información de definición de tipos en el archivo de proxy que va a consumir el motor de serialización.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="ff4fc-111">Uso</span><span class="sxs-lookup"><span data-stu-id="ff4fc-111">Usage</span></span>

<span data-ttu-id="ff4fc-112">**Modificador de la línea de comandos deWsUtil.exe- \[ \[ opciones \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="ff4fc-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="ff4fc-113">modificadores de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ff4fc-113">command-line-switches</span></span>

<span data-ttu-id="ff4fc-114">Especifica WsUtil.exe opciones del compilador.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="ff4fc-115">Los modificadores pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-115">Switches can appear in any order.</span></span> <span data-ttu-id="ff4fc-116">Los guiones ('-') y la barra diagonal ('/') se tratan como los mismos.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="ff4fc-117">Lista de opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ff4fc-117">List of command line options</span></span>

-   <span data-ttu-id="ff4fc-118">@filename Especifica que el archivo de entrada debe tratarse como un archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="ff4fc-119">Esta opción se puede usar varias veces en cualquier lugar de la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="ff4fc-120">/WSDL: <filename> : <\_ dirección url opcional> especifica que el archivo de entrada debe tratarse como un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="ff4fc-121">Se permiten varias entradas de WSDL y se procesan todos los archivos WSDL especificados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="ff4fc-122">La \_ dirección URL opcional especifica la ubicación desde la que se recuperaron los metadatos.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="ff4fc-123">Si no \_ se especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="ff4fc-124">Vea también [compatibilidad con directivas](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="ff4fc-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="ff4fc-125">/xsd: <filename> especifica que el nombre de archivo de entrada debe tratarse como un archivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="ff4fc-126">Se permiten varias entradas XSD y se procesan todos los archivos de esquema especificados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="ff4fc-127">/WSP: <filename> : <\_ dirección url opcional> especifica que el nombre de archivo de entrada debe tratarse como metadatos de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="ff4fc-128">Se permiten varias entradas WSP y se procesan todos los archivos de directivas especificados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="ff4fc-129">La \_ dirección URL opcional especifica la ubicación desde la que se recuperaron los metadatos.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="ff4fc-130">Si no \_ se especifica ninguna dirección URL opcional, Wsutil genera una dirección URL única internamente.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="ff4fc-131">Los archivos de Directiva se omiten si se especifica la marca/nopolicy.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="ff4fc-132">Vea también [compatibilidad con directivas](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="ff4fc-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="ff4fc-133">/nopolicy deshabilite el procesamiento de directivas.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="ff4fc-134">/out: <dirname> especifica el nombre de directorio para los archivos de salida</span><span class="sxs-lookup"><span data-stu-id="ff4fc-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="ff4fc-135">/noclient no generan el código auxiliar del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="ff4fc-136">/noservice no generan el código auxiliar del lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="ff4fc-137">/prefix: <string> antepone la cadena especificada a todos los identificadores generados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="ff4fc-138">/FullName antepone el nombre de archivo normalizado a los identificadores generados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="ff4fc-139">De forma predeterminada, solo se utilizará el nombre especificado en el atributo "Name" para generar identificadores para las descripciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="ff4fc-140">/String: <\_ cadena WS>\|<WCHAR \*> de forma predeterminada, wsutil genera WCHAR \* para el tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="ff4fc-141">La aplicación puede usar esta marca para sobrescribir ese comportamiento y genera una \_ cadena WS para xsd: Type en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="ff4fc-142">/Help Mostrar mensaje de ayuda</span><span class="sxs-lookup"><span data-stu-id="ff4fc-142">/help Display help message</span></span>
-   <span data-ttu-id="ff4fc-143">/?</span><span class="sxs-lookup"><span data-stu-id="ff4fc-143">/?</span></span> <span data-ttu-id="ff4fc-144">Igual que/Help</span><span class="sxs-lookup"><span data-stu-id="ff4fc-144">Same as /help</span></span>
-   <span data-ttu-id="ff4fc-145">Opciones de control de errores/w: x.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-145">/W:x Error handling options.</span></span> <span data-ttu-id="ff4fc-146">Puede ser W:0-W: 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="ff4fc-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="ff4fc-147">/nologo no generar información específica del compilador en la salida de la consola.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="ff4fc-148">/nostamp no generan información específica del compilador en los archivos generados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="ff4fc-149">De forma predeterminada, el compilador genera los siguientes archivos para el archivo WSDL o el WSDL que devuelve el intercambio de metadatos:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="ff4fc-150">Proxy de cliente ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="ff4fc-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="ff4fc-151">Código auxiliar de servicio ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="ff4fc-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="ff4fc-152">Archivo de encabezado ({InputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="ff4fc-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="ff4fc-153">La raíz del nombre de archivo generado es el nombre del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="ff4fc-154">Las extensiones de archivo de entrada originales se conservan para evitar la colisión de nombres de archivo para los archivos generados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="ff4fc-155">De forma predeterminada, los códigos auxiliares de cliente y servicio se generan en el mismo archivo, con código auxiliar de servicio generado después del código de proxy.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="ff4fc-156">De forma predeterminada, el compilador genera los siguientes archivos para un archivo XSD para el esquema devuelto desde el intercambio de metadatos:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="ff4fc-157">descripciones de serialización ({InputFilename}. c)</span><span class="sxs-lookup"><span data-stu-id="ff4fc-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="ff4fc-158">Archivo de encabezado ({InputFilename}. h)</span><span class="sxs-lookup"><span data-stu-id="ff4fc-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="ff4fc-159">La raíz del nombre de archivo es el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="ff4fc-160">Wsutil.exe genera una sección "Stamp" al principio de todos los archivos generados, lo que indica la opción del compilador, la versión de herramienta, la opción de línea de comandos aplicable, etc. Esta sección se puede desactivar mediante la opción/nostamp para evitar el ruido con la comparación de archivos generados.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="ff4fc-161">Wsutil no admite la descarga de metadatos</span><span class="sxs-lookup"><span data-stu-id="ff4fc-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="ff4fc-162">El compilador Wsutil solo funciona desde un archivo de metadatos local.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="ff4fc-163">La herramienta no admite la descarga de metadatos de servicios web en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="ff4fc-164">Los desarrolladores pueden usar otras herramientas de WebService compatibles, como SvcUtil, para descargar los metadatos en la máquina local, inspeccionar los archivos guardados y pasarlos a wsutil.exe para su compilación.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="ff4fc-165">Compatibilidad con varios archivos de entrada y salida</span><span class="sxs-lookup"><span data-stu-id="ff4fc-165">Multiple input/output file support</span></span>

<span data-ttu-id="ff4fc-166">WSDL y el esquema XML permiten incluir o importar definiciones de otros espacios de nombres especificados en otros archivos o ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="ff4fc-167">Wsutil admite varias entradas de esquema/WSDL/Directiva y genera un conjunto de código auxiliar/encabezado para cada archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="ff4fc-168">Wsutil no sigue las instrucciones include e import.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="ff4fc-169">En su lugar, la aplicación debe pasar archivos que contengan todos los espacios de nombres necesarios a wsutil de modo que la herramienta pueda resolver todas las dependencias durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="ff4fc-170">**WsUtil.exe/xsd: stockquote. xsd/WSDL: stockquote. wsdl/WSDL: stockquoteservice. wsdl**</span><span class="sxs-lookup"><span data-stu-id="ff4fc-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="ff4fc-171">wsutil genera tres conjuntos de archivos de salida:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="ff4fc-172">stockquote. xsd. c stockquote. xsd. h</span><span class="sxs-lookup"><span data-stu-id="ff4fc-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="ff4fc-173">stockquote. wsdl. c stockquote. wsdl. h</span><span class="sxs-lookup"><span data-stu-id="ff4fc-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="ff4fc-174">stockquoteservice. wsdl. h stockquoteservices. wsdl. c</span><span class="sxs-lookup"><span data-stu-id="ff4fc-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="ff4fc-175">Formato del archivo de salida</span><span class="sxs-lookup"><span data-stu-id="ff4fc-175">Output file format</span></span>

<span data-ttu-id="ff4fc-176">Para cada archivo de salida, wsutil genera definiciones externamente disponibles en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="ff4fc-177">Aparte de las definiciones de la estructura de C y los prototipos de función de código auxiliar, todas las demás definiciones relacionadas con servicios web se encapsulan en una estructura global denominada con un nombre de archivo normalizado.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="ff4fc-178">Tenga en cuenta que no todos los campos se generan para la estructura global.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="ff4fc-179">Solo se genera un campo de nivel superior cuando las definiciones relacionadas se especifican en el archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="ff4fc-180">Por ejemplo, no se generan campos de mensajes, operaciones y contratos para los archivos xsd.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="ff4fc-181">Niveles de advertencia y nivel de error</span><span class="sxs-lookup"><span data-stu-id="ff4fc-181">Warning Levels and error level</span></span>

<span data-ttu-id="ff4fc-182">Del mismo modo que el compilador de C, WsUtil.exe admite cuatro niveles de advertencia y un nivel de error:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="ff4fc-183">WsUtil.exe genera errores con errores irrecuperables, como un archivo WSDL no válido, opciones de compilador no válidas, etc.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="ff4fc-184">WsUtil genera advertencias W1 con problemas recuperables graves.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="ff4fc-185">El compilador puede continuar, pero el usuario debe ser consciente del problema.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="ff4fc-186">Por ejemplo, se generará una advertencia W1 si hay atributos no compatibles, como algunas de las figuras de WSDL, en WSDL que no afecten a la generación de código.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="ff4fc-187">WsUtil genera advertencias de W2 con problemas menos graves.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="ff4fc-188">No se pierde la funcionalidad, pero es posible que el desarrollador de aplicaciones desee saberlo.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="ff4fc-189">Como los comportamientos que pueden ser diferentes de otras plataformas.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="ff4fc-190">WsUtil genera advertencias de W3 con un impacto mínimo en el código generado.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="ff4fc-191">Por ejemplo, wsutil.exe genera una advertencia de W3 cuando la cadena normalizada es diferente de la cadena original.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="ff4fc-192">La advertencia de W4 es más similar a las advertencias "informativas" y WsUtil emite W4 en casos como omitir el atributo de documentación en WSDL.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="ff4fc-193">WX indica que el compilador trata la advertencia como un error.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="ff4fc-194">Por ejemplo, wsutil genera un error para todas las advertencias de W1 si se especifica/W: 1/WX.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="ff4fc-195">/W: {N} especifique el nivel de mensaje de advertencia que debe generarse.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="ff4fc-196">/W: 1 significa que se deben generar advertencias de nivel de ADVERTENCIA 1 y las advertencias del nivel de ADVERTENCIA 2 e inferior deben enmascararse y no generarse con la herramienta.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="ff4fc-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="ff4fc-197">/fullname</span></span>

<span data-ttu-id="ff4fc-198">Esta opción indica que WsUtil.exe genera un nombre completo para los identificadores con el fin de evitar posibles conflictos de nombres.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="ff4fc-199">Por ejemplo, en el ejemplo. xsd tenemos:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="ff4fc-200">De forma predeterminada WsUtil.exe genera:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="ff4fc-201">Pero si se especifica la opción de línea de comandos/FullName, WsUtil.exe genera en su lugar la siguiente definición de estructura:</span><span class="sxs-lookup"><span data-stu-id="ff4fc-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="ff4fc-202">Globalización</span><span class="sxs-lookup"><span data-stu-id="ff4fc-202">Globalization</span></span>

<span data-ttu-id="ff4fc-203">La herramienta es independiente del idioma y se puede localizar en distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="ff4fc-204">Se pueden localizar todos los mensajes de error y la salida de la consola.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="ff4fc-205">Sin embargo, las opciones de la línea de comandos permanecen en inglés.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="ff4fc-206">Variable de entorno</span><span class="sxs-lookup"><span data-stu-id="ff4fc-206">Environment Variable</span></span>

<span data-ttu-id="ff4fc-207">WsUtil.exe no usa ninguna variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="ff4fc-208">Independiente de la plataforma</span><span class="sxs-lookup"><span data-stu-id="ff4fc-208">Platform independent</span></span>

<span data-ttu-id="ff4fc-209">Los archivos de salida de WsUtil.exe son independientes de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="ff4fc-210">No se ha generado ningún código dependiente de la arquitectura en el código auxiliar; el compilador de C se ocupará de cualquier arquitectura específica.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="ff4fc-211">El código auxiliar se puede usar en todas las plataformas admitidas.</span><span class="sxs-lookup"><span data-stu-id="ff4fc-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="ff4fc-212">La descripción de la salida de wsutil.exe se puede encontrar en la parte compatibilidad de [WSDL](wsdl-support.md) y en el [esquema](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4fc-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 





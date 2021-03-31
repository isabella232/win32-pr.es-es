---
title: Herramienta del compilador WsUtil
description: La herramienta compilador de servicios Web de Windows, WsUtil.exe, admite el modelo de servicio y la serialización de tipos de datos. Procesa WSDL, esquemas XML y documentos de Directiva, y genera encabezados y archivos de código fuente de C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servicios Web de la herramienta compilador de WsUtil para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995749"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="bf579-107">Herramienta del compilador WsUtil</span><span class="sxs-lookup"><span data-stu-id="bf579-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="bf579-108">La herramienta compilador de servicios Web de Windows, WsUtil.exe, admite el [modelo de servicio](service-model-layer-overview.md) y la [serialización](serialization.md) de tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="bf579-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="bf579-109">Procesa WSDL, esquemas XML y documentos de Directiva, y genera encabezados y archivos de código fuente de C.</span><span class="sxs-lookup"><span data-stu-id="bf579-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="bf579-110">Esta herramienta es similar a la herramienta de compilación WSDL para código administrado, pero está destinada a código nativo.</span><span class="sxs-lookup"><span data-stu-id="bf579-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="bf579-111">Para admitir el [modelo de servicio](service-model-layer-overview.md), WsUtil.exe genera encabezados que se usarán tanto para el cliente como para el servicio.</span><span class="sxs-lookup"><span data-stu-id="bf579-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="bf579-112">Genera un archivo de proxy de C para el lado cliente y archivos de código auxiliar de C para el servicio, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bf579-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="bf579-113">Para admitir la [serialización](serialization.md), el compilador genera encabezados para las descripciones de elementos de las definiciones de elementos globales y toda la información de definición de tipos en los archivos de proxy que usa el motor de serialización.</span><span class="sxs-lookup"><span data-stu-id="bf579-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="bf579-114">Para ver las opciones de línea de comandos para procesar archivos WSDL, archivos de esquema XML y archivos de directiva de servicio Web, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf579-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="bf579-115">Herramienta de compilador de servicio Web</span><span class="sxs-lookup"><span data-stu-id="bf579-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="bf579-116">WSDL y contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="bf579-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="bf579-117">Compatibilidad con esquemas</span><span class="sxs-lookup"><span data-stu-id="bf579-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="bf579-118">Compatibilidad con directivas</span><span class="sxs-lookup"><span data-stu-id="bf579-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="bf579-119">Seguridad</span><span class="sxs-lookup"><span data-stu-id="bf579-119">Security</span></span>

<span data-ttu-id="bf579-120">Cuando use WsUtil, tenga en cuenta los siguientes problemas y observe las precauciones adecuadas:</span><span class="sxs-lookup"><span data-stu-id="bf579-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="bf579-121">Wsutil no recupera metadatos XML a través de la red y Wsutil no resuelve instrucciones Import ni include en los archivos de metadatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf579-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="bf579-122">Wsutil abre y lee archivos WSDL, XSD y de directivas.</span><span class="sxs-lookup"><span data-stu-id="bf579-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="bf579-123">Los metadatos XML no son resistentes contra alteraciones.</span><span class="sxs-lookup"><span data-stu-id="bf579-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="bf579-124">Asegúrese de que solo se utilizan WSDL, XSD y archivos de directivas desde el origen de confianza y asegúrese de proteger los archivos contra la manipulación antes y después de usarlos.</span><span class="sxs-lookup"><span data-stu-id="bf579-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="bf579-125">Revise cuidadosamente el contenido de los archivos de entrada y compruebe que el contenido de los archivos es seguro para su uso en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf579-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="bf579-126">Wsutil.exe no realiza ninguna comprobación de la autenticidad de los archivos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="bf579-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="bf579-127">Wsutil genera archivos de encabezado y de código auxiliar, que no son resistentes contra alteraciones.</span><span class="sxs-lookup"><span data-stu-id="bf579-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="bf579-128">Debe establecer los derechos de acceso de nivel correctos en los archivos de código fuente generados por wsutil.exe para impedir el acceso de unauthoritized a esos archivos.</span><span class="sxs-lookup"><span data-stu-id="bf579-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="bf579-129">Wsutil usa System. IO. StreamWriter para crear los archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="bf579-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="bf579-130">Los usuarios deben tener en cuenta que Wsutil puede sobrescribir sus archivos locales y deben tener cuidado de especificar nombres de archivo y directorios seguros para los archivos de salida mediante el modificador/out.</span><span class="sxs-lookup"><span data-stu-id="bf579-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="bf579-131">Wsutil o wsutilhelper.dll se cargan en wsutil.exe, pueden finalizar de forma inesperada o consumir una gran cantidad de recursos del sistema cuando están en ataque o en el procesamiento de una cantidad muy grande de metadatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf579-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="bf579-132">La herramienta está diseñada para usarse solo durante el desarrollo. esta herramienta solo se debe usar como herramienta de tiempo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="bf579-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="bf579-133">Puede que no sea seguro usarlo en el nivel intermedio para procesar la información de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="bf579-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="bf579-134">Wsutilhelper.dll archivo DLL de la aplicación auxiliar se carga en wsutil.exe administrados para procesar la información de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="bf579-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="bf579-135">El usuario debe asegurarse de que no existe ningún binario malintencionado con el mismo nombre de archivo en la ruta de acceso binaria.</span><span class="sxs-lookup"><span data-stu-id="bf579-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="bf579-136">Del mismo modo, el usuario debe asegurarse de que en el entorno de compilación, la ruta de acceso binaria está configurada correctamente y que no existe ningún binario malintencionado con el mismo nombre de "wsutil.exe".</span><span class="sxs-lookup"><span data-stu-id="bf579-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="bf579-137">Wsutil genera una anotación SAL para las operaciones y los campos de estructura siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="bf579-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="bf579-138">El usuario de los archivos generados por wsutil debe seguir el requisito especificado a través de la anotación SAL.</span><span class="sxs-lookup"><span data-stu-id="bf579-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf579-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf579-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf579-140">Información general sobre la capa de modelo de servicio</span><span class="sxs-lookup"><span data-stu-id="bf579-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="bf579-141">Serialización</span><span class="sxs-lookup"><span data-stu-id="bf579-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="bf579-142">Herramienta de compilador de servicio Web</span><span class="sxs-lookup"><span data-stu-id="bf579-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="bf579-143">Compatibilidad con WSDL</span><span class="sxs-lookup"><span data-stu-id="bf579-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="bf579-144">Compatibilidad con esquemas</span><span class="sxs-lookup"><span data-stu-id="bf579-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="bf579-145">Compatibilidad con directivas</span><span class="sxs-lookup"><span data-stu-id="bf579-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 





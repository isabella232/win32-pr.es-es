---
description: Muestra cómo implementar una extensión de espacio de nombres de Shell, incluido el comportamiento del menú contextual y las tareas personalizadas en el explorador.
title: Ejemplo del proveedor de datos de Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278868"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="87a56-103">Ejemplo del proveedor de datos de Explorer</span><span class="sxs-lookup"><span data-stu-id="87a56-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="87a56-104">Muestra cómo implementar una extensión de espacio de nombres de Shell, incluido el comportamiento del menú contextual y las tareas personalizadas en el explorador.</span><span class="sxs-lookup"><span data-stu-id="87a56-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="87a56-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="87a56-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="87a56-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a56-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="87a56-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="87a56-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="87a56-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="87a56-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a56-110">Requirements</span></span>



| <span data-ttu-id="87a56-111">Producto</span><span class="sxs-lookup"><span data-stu-id="87a56-111">Product</span></span>                                | <span data-ttu-id="87a56-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="87a56-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="87a56-113">Windows</span><span class="sxs-lookup"><span data-stu-id="87a56-113">Windows</span></span>                                | <span data-ttu-id="87a56-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87a56-114">Windows Vista</span></span>           |
| <span data-ttu-id="87a56-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="87a56-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="87a56-116">6.1</span><span class="sxs-lookup"><span data-stu-id="87a56-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="87a56-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-117">Downloading the Sample</span></span>

| <span data-ttu-id="87a56-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="87a56-118">Location</span></span>      | <span data-ttu-id="87a56-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="87a56-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a56-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="87a56-120">GitHub</span></span>  | [<span data-ttu-id="87a56-121">Ejemplo de ExplorerDataProvider</span><span class="sxs-lookup"><span data-stu-id="87a56-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="87a56-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-122">Building the Sample</span></span>

<span data-ttu-id="87a56-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="87a56-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="87a56-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="87a56-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="87a56-125">Escriba `msbuild ExplorerDataProvider.sln`.</span><span class="sxs-lookup"><span data-stu-id="87a56-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="87a56-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="87a56-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="87a56-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="87a56-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="87a56-128">Haga doble clic en el icono del archivo ExplorerDataProvider. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="87a56-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="87a56-129">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="87a56-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="87a56-130">El archivo DLL se generará en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="87a56-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="87a56-131">En la versión de este ejemplo incluida en el Windows SDK, la configuración de la compilación de la versión de 64 bits no incluye el archivo ExplorerDataProvider. def en la opción de **archivo de definición de módulo** del enlazador.</span><span class="sxs-lookup"><span data-stu-id="87a56-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="87a56-132">Debe especificar ese archivo antes de compilar en un entorno de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="87a56-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="87a56-133">Agregue la línea `ModuleDefinitionFile="ExplorerDataProvider.def"` a la sección VCLinkerTool (comienza en la línea 329) del archivo ExplorerDataProvider. vcproj como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="87a56-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="87a56-134">La versión de este ejemplo descargable de la galería de código se ha corregido para este problema y no se requiere ninguna acción adicional por su parte.</span><span class="sxs-lookup"><span data-stu-id="87a56-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="87a56-135">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="87a56-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="87a56-136">Navegue hasta el directorio que contiene el nuevo archivo. dll y. propDesc, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="87a56-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="87a56-137">En la línea de comandos, escriba `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="87a56-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="87a56-138">Si ejecuta este comando desde un símbolo del sistema con privilegios elevados, el registro automático también registrará automáticamente el archivo. propDesc.</span><span class="sxs-lookup"><span data-stu-id="87a56-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="87a56-139">Si se ejecuta desde un símbolo del sistema sin privilegios elevados, la extensión de espacio de nombres funcionará, pero sin la funcionalidad de propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="87a56-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="87a56-140">Abra la carpeta **mi PC** y examine la nueva extensión de espacio de nombres presente allí.</span><span class="sxs-lookup"><span data-stu-id="87a56-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>



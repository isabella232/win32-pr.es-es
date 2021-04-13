---
title: Compilar marcado de cinta
description: Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Cinta de Windows, compilar marcado
- Cinta, compilar marcado
- Cinta de Windows, flujo de trabajo del compilador
- Cinta, flujo de trabajo del compilador
- Cinta de Windows, compilador de comandos de la interfaz de usuario (UICC.exe)
- Cinta, compilador de comandos de la interfaz de usuario (UICC.exe)
- Compilador de comandos de IU (UICC.exe)
- UICC.exe (compilador de comandos de IU)
- compilar el marcado de la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532332"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="3efae-112">Compilar marcado de cinta</span><span class="sxs-lookup"><span data-stu-id="3efae-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="3efae-113">Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la [cinta](windowsribbon-schema.md) de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.</span><span class="sxs-lookup"><span data-stu-id="3efae-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="3efae-114">Un compilador de marcado dedicado, el compilador de comandos de la interfaz de usuario (UICC), se incluye con el kit de desarrollo de software (SDK) de Windows (7,0 o posterior) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="3efae-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="3efae-115">Además de compilar la versión binaria del marcado, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="3efae-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="3efae-116">Flujo de trabajo compilador</span><span class="sxs-lookup"><span data-stu-id="3efae-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="3efae-117">Sintaxis de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3efae-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="3efae-118">Argumentos y opciones</span><span class="sxs-lookup"><span data-stu-id="3efae-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="3efae-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3efae-119">Example</span></span>](#example)
-   [<span data-ttu-id="3efae-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3efae-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="3efae-121">Flujo de trabajo compilador</span><span class="sxs-lookup"><span data-stu-id="3efae-121">Compiler Workflow</span></span>

<span data-ttu-id="3efae-122">El flujo de trabajo del compilador de marcado de la cinta se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="3efae-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![diagrama que muestra el flujo de trabajo del compilador de marcado de cinta.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="3efae-124">Sintaxis de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3efae-124">Command-Line Syntax</span></span>

<span data-ttu-id="3efae-125">En el ejemplo siguiente se muestra la sintaxis de línea de comandos para el compilador de marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="3efae-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="3efae-126">Argumentos y opciones</span><span class="sxs-lookup"><span data-stu-id="3efae-126">Arguments and Options</span></span>

<span data-ttu-id="3efae-127">En la tabla siguiente se describen los argumentos y las opciones de esta herramienta.</span><span class="sxs-lookup"><span data-stu-id="3efae-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="3efae-128">Las opciones de línea de comandos que se muestran deben especificarse en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="3efae-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3efae-129">Opción</span><span class="sxs-lookup"><span data-stu-id="3efae-129">Option</span></span></th>
<th><span data-ttu-id="3efae-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3efae-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3efae-131">encabezado<headerFile></span><span class="sxs-lookup"><span data-stu-id="3efae-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="3efae-132">Genere un archivo de encabezado denominado <headerFile> que contenga los símbolos de recursos de identificador de comando de marcado.</span><span class="sxs-lookup"><span data-stu-id="3efae-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="3efae-133">Si se omite, no se genera un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3efae-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3efae-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="3efae-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="3efae-135">Genere un archivo de recursos denominado <resourceFile> que vincule todos los recursos de imagen y cadena, el archivo de marcado binario y el archivo de encabezado a la aplicación host en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="3efae-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="3efae-136">Si se omite, no se genera un archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3efae-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3efae-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="3efae-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="3efae-138">Nombre del recurso para el archivo de marcado binario registrado en el <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="3efae-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="3efae-139">El valor predeterminado es APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="3efae-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3efae-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="3efae-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="3efae-141">Filtre los mensajes de eventos en función de la gravedad.</span><span class="sxs-lookup"><span data-stu-id="3efae-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3efae-142">0</span><span class="sxs-lookup"><span data-stu-id="3efae-142">0</span></span><br/></td>
<td><span data-ttu-id="3efae-143">Solo mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="3efae-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3efae-144">1</span><span class="sxs-lookup"><span data-stu-id="3efae-144">1</span></span><br/></td>
<td><span data-ttu-id="3efae-145">Solo mensajes de error y ADVERTENCIA.</span><span class="sxs-lookup"><span data-stu-id="3efae-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3efae-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="3efae-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="3efae-147">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3efae-147">Default.</span></span> <br/> <span data-ttu-id="3efae-148">Mensajes de error, de advertencia e informativos.</span><span class="sxs-lookup"><span data-stu-id="3efae-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="3efae-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3efae-149">Example</span></span>

<span data-ttu-id="3efae-150">En el ejemplo siguiente se muestra cómo utilizar el compilador de marcado de la cinta de opciones para generar un conjunto típico de archivos de recursos para una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="3efae-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="3efae-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3efae-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efae-152">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="3efae-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="3efae-153">Crear una aplicación de cinta</span><span class="sxs-lookup"><span data-stu-id="3efae-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 






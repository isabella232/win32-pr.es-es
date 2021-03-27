---
title: " include (Directiva)"
description: Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la Directiva.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- incluir la Directiva HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997085"
---
# <a name="include-directive"></a><span data-ttu-id="51b39-104">\#include (Directiva)</span><span class="sxs-lookup"><span data-stu-id="51b39-104">\#include Directive</span></span>

<span data-ttu-id="51b39-105">Directiva de preprocesador que inserta el contenido del archivo especificado en el programa de origen en el punto donde aparece la Directiva.</span><span class="sxs-lookup"><span data-stu-id="51b39-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="51b39-106">\#incluir "*filename*"</span><span class="sxs-lookup"><span data-stu-id="51b39-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="51b39-107">\#incluir <*nombre de archivo*></span><span class="sxs-lookup"><span data-stu-id="51b39-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="51b39-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51b39-108">Parameters</span></span>

| <span data-ttu-id="51b39-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="51b39-109">Item</span></span> | <span data-ttu-id="51b39-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="51b39-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="51b39-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="51b39-111">*filename*</span></span> | <span data-ttu-id="51b39-112">Nombre del archivo que se va a incluir, opcionalmente precedido por una especificación de directorio.</span><span class="sxs-lookup"><span data-stu-id="51b39-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="51b39-113">El nombre de archivo debe especificar un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="51b39-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="51b39-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51b39-114">Remarks</span></span>

<span data-ttu-id="51b39-115">La \# directiva Include provoca el reemplazo de la Directiva por todo el contenido del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="51b39-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="51b39-116">El preprocesador detiene la búsqueda en cuanto encuentra un archivo con el nombre especificado; Si especifica una especificación de ruta de acceso completa y no ambigua para el archivo, el preprocesador busca solo la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="51b39-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="51b39-117">La [herramienta de compilador de efecto](/windows/desktop/direct3dtools/fxc) tiene un controlador de inclusión integrado mediante el modificador/i.</span><span class="sxs-lookup"><span data-stu-id="51b39-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="51b39-118">Sin embargo, al ejecutar el compilador desde la API, puede proporcionar un controlador de inclusión personalizado implementando la interfaz ID3DXInclude.</span><span class="sxs-lookup"><span data-stu-id="51b39-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="51b39-119">La diferencia entre las dos formas de sintaxis es el orden en el que el preprocesador busca los archivos de encabezado cuando la ruta de acceso se especifica incompletamente, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="51b39-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51b39-120">Forma de sintaxis</span><span class="sxs-lookup"><span data-stu-id="51b39-120">Syntax form</span></span></th>
<th><span data-ttu-id="51b39-121">Patrón de búsqueda del preprocesador</span><span class="sxs-lookup"><span data-stu-id="51b39-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51b39-122">#incluir <b>&quot;</b> <em>nombre de archivo</em><b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="51b39-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="51b39-123">Busca el archivo de inclusión:</span><span class="sxs-lookup"><span data-stu-id="51b39-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="51b39-124">en el mismo directorio que el archivo que contiene la Directiva #include.</span><span class="sxs-lookup"><span data-stu-id="51b39-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="51b39-125">en los directorios de los archivos que contienen una directiva #include para el archivo que contiene la Directiva #include.</span><span class="sxs-lookup"><span data-stu-id="51b39-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="51b39-126">en las rutas de acceso especificadas por la opción del compilador/I, en el orden en que aparecen.</span><span class="sxs-lookup"><span data-stu-id="51b39-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="51b39-127">en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que aparecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="51b39-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="51b39-128">La variable de entorno INCLUDE se omite en un entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="51b39-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="51b39-129">Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de inclusión para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="51b39-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b39-130">#incluir <b><</b> <em>nombre de archivo</em><b>></b></span><span class="sxs-lookup"><span data-stu-id="51b39-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="51b39-131">Busca el archivo de inclusión:</span><span class="sxs-lookup"><span data-stu-id="51b39-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="51b39-132">en las rutas de acceso especificadas por la opción del compilador/I, en el orden en que aparecen.</span><span class="sxs-lookup"><span data-stu-id="51b39-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="51b39-133">en las rutas de acceso especificadas por la variable de entorno INCLUDE, en el orden en que aparecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="51b39-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="51b39-134">La variable de entorno INCLUDE se omite en un entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="51b39-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="51b39-135">Consulte la documentación del entorno de desarrollo para obtener información sobre cómo establecer las rutas de acceso de inclusión para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="51b39-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="51b39-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51b39-136">Examples</span></span>

<span data-ttu-id="51b39-137">En el ejemplo siguiente se hace que el preprocesador Reemplace la \# directiva Include por el contenido de stdio. h.</span><span class="sxs-lookup"><span data-stu-id="51b39-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="51b39-138">Dado que en el ejemplo se usa el formato de corchete angular, el preprocesador buscará el archivo solo en los directorios enumerados por la opción del compilador/I y la variable de entorno INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="51b39-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="51b39-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="51b39-139">See also</span></span>

- [<span data-ttu-id="51b39-140">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="51b39-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="51b39-141">[Interfaz ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51b39-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="51b39-142">Efecto: herramienta de compilador</span><span class="sxs-lookup"><span data-stu-id="51b39-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
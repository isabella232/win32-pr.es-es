---
description: Coloca una instrucción include de C o IDL en el código generado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706455"
---
# <a name="literalinclude-element"></a><span data-ttu-id="7efef-103">elemento literalInclude</span><span class="sxs-lookup"><span data-stu-id="7efef-103">literalInclude element</span></span>

<span data-ttu-id="7efef-104">Coloca una instrucción include de C o IDL en el código generado.</span><span class="sxs-lookup"><span data-stu-id="7efef-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="7efef-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7efef-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="7efef-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7efef-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7efef-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="7efef-107">Attribute</span></span></th>
<th><span data-ttu-id="7efef-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7efef-108">Type</span></span></th>
<th><span data-ttu-id="7efef-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7efef-109">Required</span></span></th>
<th><span data-ttu-id="7efef-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7efef-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7efef-111"><strong>Lenguaje</strong></span><span class="sxs-lookup"><span data-stu-id="7efef-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="7efef-112">cadena de idioma</span><span class="sxs-lookup"><span data-stu-id="7efef-112">language string</span></span><br/></td>
<td><span data-ttu-id="7efef-113">No</span><span class="sxs-lookup"><span data-stu-id="7efef-113">No</span></span><br/></td>
<td><span data-ttu-id="7efef-114">Tipo de archivo de encabezado que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="7efef-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="7efef-115">
<dt><strong>Unidad</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7efef-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="7efef-116">Incluya un archivo de encabezado de C.</span><span class="sxs-lookup"><span data-stu-id="7efef-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="7efef-117"><dt><strong>IDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7efef-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="7efef-118">Incluya un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7efef-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7efef-119"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="7efef-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="7efef-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="7efef-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="7efef-121">No</span><span class="sxs-lookup"><span data-stu-id="7efef-121">No</span></span><br/></td>
<td><span data-ttu-id="7efef-122">Este atributo solo se utiliza cuando el <strong>idioma</strong> está establecido en &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="7efef-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="7efef-123">
<dt><strong>Reales</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7efef-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="7efef-124">Busca el encabezado con nombre en el directorio actual antes de buscar en los directorios del sistema.</span><span class="sxs-lookup"><span data-stu-id="7efef-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="7efef-125"><dt><strong>Es</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7efef-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="7efef-126">Solo busca en los directorios de sistema del encabezado con nombre.</span><span class="sxs-lookup"><span data-stu-id="7efef-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7efef-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7efef-127">Child elements</span></span>

<span data-ttu-id="7efef-128">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7efef-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7efef-129">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7efef-129">Parent elements</span></span>



| <span data-ttu-id="7efef-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="7efef-130">Element</span></span>                         | <span data-ttu-id="7efef-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7efef-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7efef-132">**archivo**</span><span class="sxs-lookup"><span data-stu-id="7efef-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7efef-133">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="7efef-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7efef-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7efef-134">Remarks</span></span>

<span data-ttu-id="7efef-135">En los siguientes ejemplos se muestra el código generado a partir de distintos elementos **literalInclude** .</span><span class="sxs-lookup"><span data-stu-id="7efef-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="7efef-136">Ejemplo 1: generar una instrucción include de C</span><span class="sxs-lookup"><span data-stu-id="7efef-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="7efef-137">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="7efef-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="7efef-138">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="7efef-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="7efef-139">Ejemplo 2: generar una instrucción include de C</span><span class="sxs-lookup"><span data-stu-id="7efef-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="7efef-140">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="7efef-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="7efef-141">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="7efef-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="7efef-142">Ejemplo 3: generación de una instrucción de importación IDL</span><span class="sxs-lookup"><span data-stu-id="7efef-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="7efef-143">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="7efef-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="7efef-144">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="7efef-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="7efef-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7efef-145">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7efef-146">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7efef-146">Minimum supported system</span></span><br/> | <span data-ttu-id="7efef-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7efef-147">Windows Vista</span></span> |
| <span data-ttu-id="7efef-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7efef-148">Can be empty</span></span>                        | <span data-ttu-id="7efef-149">Sí</span><span class="sxs-lookup"><span data-stu-id="7efef-149">Yes</span></span>           |



 

 





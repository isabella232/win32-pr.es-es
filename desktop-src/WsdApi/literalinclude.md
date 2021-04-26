---
description: Coloca una instrucción include de C o IDL en el código generado.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: literalInclude, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995132"
---
# <a name="literalinclude-element"></a><span data-ttu-id="fb8e4-103">literalInclude, elemento</span><span class="sxs-lookup"><span data-stu-id="fb8e4-103">literalInclude element</span></span>

<span data-ttu-id="fb8e4-104">Coloca una instrucción include de C o IDL en el código generado.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="fb8e4-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fb8e4-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="fb8e4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb8e4-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb8e4-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="fb8e4-107">Attribute</span></span></th>
<th><span data-ttu-id="fb8e4-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb8e4-108">Type</span></span></th>
<th><span data-ttu-id="fb8e4-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb8e4-109">Required</span></span></th>
<th><span data-ttu-id="fb8e4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8e4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb8e4-111"><strong>Lenguaje</strong></span><span class="sxs-lookup"><span data-stu-id="fb8e4-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="fb8e4-112">cadena de idioma</span><span class="sxs-lookup"><span data-stu-id="fb8e4-112">language string</span></span><br/></td>
<td><span data-ttu-id="fb8e4-113">No</span><span class="sxs-lookup"><span data-stu-id="fb8e4-113">No</span></span><br/></td>
<td><span data-ttu-id="fb8e4-114">Tipo de archivo de encabezado que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="fb8e4-115">
<dt><strong>C</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fb8e4-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="fb8e4-116">Incluya un archivo de encabezado de C.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="fb8e4-117"><dt><strong>Idl</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fb8e4-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="fb8e4-118">Incluya un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb8e4-119"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="fb8e4-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="fb8e4-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb8e4-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="fb8e4-121">No</span><span class="sxs-lookup"><span data-stu-id="fb8e4-121">No</span></span><br/></td>
<td><span data-ttu-id="fb8e4-122">Este atributo solo se usa cuando <strong>Language</strong> se establece en &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="fb8e4-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="fb8e4-123">
<dt><strong>Verdad</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fb8e4-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="fb8e4-124">Busca en el directorio actual el encabezado con nombre antes de buscar en los directorios del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="fb8e4-125"><dt><strong>Falso</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fb8e4-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="fb8e4-126">Busque solo los directorios del sistema para el encabezado con nombre.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fb8e4-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb8e4-127">Child elements</span></span>

<span data-ttu-id="fb8e4-128">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fb8e4-129">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fb8e4-129">Parent elements</span></span>



| <span data-ttu-id="fb8e4-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="fb8e4-130">Element</span></span>                         | <span data-ttu-id="fb8e4-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb8e4-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fb8e4-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fb8e4-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fb8e4-133">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="fb8e4-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fb8e4-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb8e4-134">Remarks</span></span>

<span data-ttu-id="fb8e4-135">En los ejemplos siguientes se muestra el código generado a partir de diferentes **elementos literalesInclude.**</span><span class="sxs-lookup"><span data-stu-id="fb8e4-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="fb8e4-136">Ejemplo 1: Generación de una instrucción include de C</span><span class="sxs-lookup"><span data-stu-id="fb8e4-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="fb8e4-137">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="fb8e4-138">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="fb8e4-139">Ejemplo 2: Generación de una instrucción include de C</span><span class="sxs-lookup"><span data-stu-id="fb8e4-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="fb8e4-140">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="fb8e4-141">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="fb8e4-142">Ejemplo 3: Generación de una instrucción de importación de IDL</span><span class="sxs-lookup"><span data-stu-id="fb8e4-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="fb8e4-143">XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="fb8e4-144">Código de salida:</span><span class="sxs-lookup"><span data-stu-id="fb8e4-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="fb8e4-145">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fb8e4-145">Element information</span></span>



| <span data-ttu-id="fb8e4-146">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="fb8e4-146">Label</span></span> | <span data-ttu-id="fb8e4-147">Value</span><span class="sxs-lookup"><span data-stu-id="fb8e4-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="fb8e4-148">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb8e4-148">Minimum supported system</span></span><br/> | <span data-ttu-id="fb8e4-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb8e4-149">Windows Vista</span></span> |
| <span data-ttu-id="fb8e4-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fb8e4-150">Can be empty</span></span>                        | <span data-ttu-id="fb8e4-151">Sí</span><span class="sxs-lookup"><span data-stu-id="fb8e4-151">Yes</span></span>           |



 

 





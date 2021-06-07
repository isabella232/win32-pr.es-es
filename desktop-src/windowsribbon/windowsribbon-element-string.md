---
title: Elemento String
description: Representa un recurso de cadena.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Cinta de opciones de Windows del elemento String
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b0dab5d7ce1485aad5fe1e15442069c488933aa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443906"
---
# <a name="string-element"></a><span data-ttu-id="89f1c-104">Elemento String</span><span class="sxs-lookup"><span data-stu-id="89f1c-104">String element</span></span>

<span data-ttu-id="89f1c-105">Representa un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="89f1c-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="89f1c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="89f1c-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="89f1c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="89f1c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89f1c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="89f1c-108">Attribute</span></span></th>
<th><span data-ttu-id="89f1c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="89f1c-109">Type</span></span></th>
<th><span data-ttu-id="89f1c-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="89f1c-110">Required</span></span></th>
<th><span data-ttu-id="89f1c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="89f1c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89f1c-112"><strong>Contenido</strong></span><span class="sxs-lookup"><span data-stu-id="89f1c-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="89f1c-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="89f1c-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="89f1c-114">No</span><span class="sxs-lookup"><span data-stu-id="89f1c-114">No</span></span><br/></td>
<td><span data-ttu-id="89f1c-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="89f1c-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89f1c-116">Cadena compuesta de cualquier secuencia de caracteres, incluidos los espacios en blanco y los caracteres de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="89f1c-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89f1c-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="89f1c-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="89f1c-118">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="89f1c-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="89f1c-119">No</span><span class="sxs-lookup"><span data-stu-id="89f1c-119">No</span></span><br/></td>
<td><span data-ttu-id="89f1c-120">Identificador de recurso único.</span><span class="sxs-lookup"><span data-stu-id="89f1c-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="89f1c-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="89f1c-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89f1c-122">Valor entero comprendido entre 2 y 59999, ambos incluidos, o 0x2 y 0xea5f en hexadecimal, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="89f1c-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="89f1c-123">La longitud máxima es de 10 caracteres, incluidos ceros iniciales opcionales.</span><span class="sxs-lookup"><span data-stu-id="89f1c-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89f1c-124"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="89f1c-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="89f1c-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="89f1c-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="89f1c-126">No</span><span class="sxs-lookup"><span data-stu-id="89f1c-126">No</span></span><br/></td>
<td><span data-ttu-id="89f1c-127">Símbolo de recurso para la cadena.</span><span class="sxs-lookup"><span data-stu-id="89f1c-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="89f1c-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="89f1c-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89f1c-129">Una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="89f1c-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="89f1c-130">La longitud máxima es de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="89f1c-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="89f1c-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89f1c-131">Child elements</span></span>



| <span data-ttu-id="89f1c-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="89f1c-132">Element</span></span>                                                                   | <span data-ttu-id="89f1c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="89f1c-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="89f1c-134">**String.Content**</span><span class="sxs-lookup"><span data-stu-id="89f1c-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="89f1c-135">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="89f1c-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="89f1c-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="89f1c-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="89f1c-137">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="89f1c-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="89f1c-138">**String.Symbol**</span><span class="sxs-lookup"><span data-stu-id="89f1c-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="89f1c-139">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="89f1c-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="89f1c-140">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="89f1c-140">Parent elements</span></span>



| <span data-ttu-id="89f1c-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="89f1c-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89f1c-142">**Command.Keytip**</span><span class="sxs-lookup"><span data-stu-id="89f1c-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="89f1c-143">**Command.LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="89f1c-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="89f1c-144">**Command.LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="89f1c-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="89f1c-145">**Command.TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="89f1c-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="89f1c-146">**Command.TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="89f1c-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="89f1c-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89f1c-147">Remarks</span></span>

<span data-ttu-id="89f1c-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="89f1c-148">Optional.</span></span>

<span data-ttu-id="89f1c-149">Puede producirse como máximo una vez para cada [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip,**](windowsribbon-element-command-keytip.md) [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) [**o Command.TooltipDescription.**](windowsribbon-element-command-tooltipdescription.md)</span><span class="sxs-lookup"><span data-stu-id="89f1c-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="89f1c-150">La definición de cadena se agrega al archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="89f1c-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="89f1c-151">La cadena se agrega a una tabla de cadenas en el archivo de recursos de la cinta de opciones donde el marco de la cinta de opciones genera un nombre e identificador si no se declara ninguno.</span><span class="sxs-lookup"><span data-stu-id="89f1c-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="89f1c-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="89f1c-152">Examples</span></span>

<span data-ttu-id="89f1c-153">En el ejemplo siguiente se muestra el marcado de un [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **declaración String.**</span><span class="sxs-lookup"><span data-stu-id="89f1c-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="89f1c-154">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="89f1c-154">Element information</span></span>

- <span data-ttu-id="89f1c-155">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="89f1c-155">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="89f1c-156">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="89f1c-156">**Can be empty**: No</span></span>



 

 






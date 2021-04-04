---
title: Elemento String
description: Representa un recurso de cadena.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Elemento de cadena cinta de Windows
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076808"
---
# <a name="string-element"></a><span data-ttu-id="0102c-104">Elemento String</span><span class="sxs-lookup"><span data-stu-id="0102c-104">String element</span></span>

<span data-ttu-id="0102c-105">Representa un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="0102c-105">Represents a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="0102c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0102c-106">Usage</span></span>

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a><span data-ttu-id="0102c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0102c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0102c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="0102c-108">Attribute</span></span></th>
<th><span data-ttu-id="0102c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0102c-109">Type</span></span></th>
<th><span data-ttu-id="0102c-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0102c-110">Required</span></span></th>
<th><span data-ttu-id="0102c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0102c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0102c-112"><strong>Contenido</strong></span><span class="sxs-lookup"><span data-stu-id="0102c-112"><strong>Content</strong></span></span><br/></td>
<td><span data-ttu-id="0102c-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="0102c-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="0102c-114">No</span><span class="sxs-lookup"><span data-stu-id="0102c-114">No</span></span><br/></td>
<td><span data-ttu-id="0102c-115"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="0102c-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0102c-116">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="0102c-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0102c-117"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="0102c-117"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="0102c-118">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="0102c-118">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0102c-119">No</span><span class="sxs-lookup"><span data-stu-id="0102c-119">No</span></span><br/></td>
<td><span data-ttu-id="0102c-120">IDENTIFICADOR de recurso único.</span><span class="sxs-lookup"><span data-stu-id="0102c-120">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="0102c-121">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="0102c-121">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0102c-122">Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="0102c-122">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="0102c-123">La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales.</span><span class="sxs-lookup"><span data-stu-id="0102c-123">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0102c-124"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="0102c-124"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="0102c-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="0102c-125">xs:string</span></span><br/></td>
<td><span data-ttu-id="0102c-126">No</span><span class="sxs-lookup"><span data-stu-id="0102c-126">No</span></span><br/></td>
<td><span data-ttu-id="0102c-127">Símbolo de recurso de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0102c-127">The resource symbol for the string.</span></span><br/> <br/><span data-ttu-id="0102c-128">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="0102c-128">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0102c-129">Una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="0102c-129">A letter or underscore followed by any sequence of letters, digits, or underscores.</span></span><br/> <span data-ttu-id="0102c-130">La longitud máxima es de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0102c-130">The maximum length is 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0102c-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0102c-131">Child elements</span></span>



| <span data-ttu-id="0102c-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="0102c-132">Element</span></span>                                                                   | <span data-ttu-id="0102c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="0102c-133">Description</span></span>                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0102c-134">**Cadena. contenido**</span><span class="sxs-lookup"><span data-stu-id="0102c-134">**String.Content**</span></span>](windowsribbon-element-string-content.md)<br/> | <span data-ttu-id="0102c-135">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="0102c-135">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="0102c-136">**String.Id**</span><span class="sxs-lookup"><span data-stu-id="0102c-136">**String.Id**</span></span>](windowsribbon-element-string-id.md)<br/>           | <span data-ttu-id="0102c-137">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="0102c-137">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="0102c-138">**String. Symbol**</span><span class="sxs-lookup"><span data-stu-id="0102c-138">**String.Symbol**</span></span>](windowsribbon-element-string-symbol.md)<br/>   | <span data-ttu-id="0102c-139">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="0102c-139">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0102c-140">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0102c-140">Parent elements</span></span>



| <span data-ttu-id="0102c-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="0102c-141">Element</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0102c-142">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="0102c-142">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                         |
| [<span data-ttu-id="0102c-143">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="0102c-143">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>     |
| [<span data-ttu-id="0102c-144">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="0102c-144">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [<span data-ttu-id="0102c-145">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="0102c-145">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [<span data-ttu-id="0102c-146">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="0102c-146">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a><span data-ttu-id="0102c-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0102c-147">Remarks</span></span>

<span data-ttu-id="0102c-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0102c-148">Optional.</span></span>

<span data-ttu-id="0102c-149">Puede producirse como máximo una vez para cada [**comando Command. LabelTitle**](windowsribbon-element-command-labeltitle.md), Command [**. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .</span><span class="sxs-lookup"><span data-stu-id="0102c-149">May occur at most once for each [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command.Keytip**](windowsribbon-element-command-keytip.md), [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), or [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) element.</span></span>

<span data-ttu-id="0102c-150">La definición de cadena se agrega al archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="0102c-150">The string definition is added to the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="0102c-151">La cadena se agrega a una tabla de cadenas en el archivo de recursos de la cinta de opciones, donde el marco de la cinta de opciones genera un nombre y un ID. Si no se declara ninguno.</span><span class="sxs-lookup"><span data-stu-id="0102c-151">The string is added to a string table in the Ribbon resource file where a name and ID are generated by the Ribbon framework if none are declared.</span></span>

## <a name="examples"></a><span data-ttu-id="0102c-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0102c-152">Examples</span></span>

<span data-ttu-id="0102c-153">En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración de **cadena** .</span><span class="sxs-lookup"><span data-stu-id="0102c-153">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a><span data-ttu-id="0102c-154">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0102c-154">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0102c-155">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0102c-155">Minimum supported system</span></span><br/> | <span data-ttu-id="0102c-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0102c-156">Windows 7</span></span> |
| <span data-ttu-id="0102c-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0102c-157">Can be empty</span></span>                        | <span data-ttu-id="0102c-158">No</span><span class="sxs-lookup"><span data-stu-id="0102c-158">No</span></span>        |



 

 






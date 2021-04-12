---
title: Command, elemento
description: Representa una definición de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Elemento Command de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359308"
---
# <a name="command-element"></a><span data-ttu-id="a0e83-104">Command, elemento</span><span class="sxs-lookup"><span data-stu-id="a0e83-104">Command element</span></span>

<span data-ttu-id="a0e83-105">Representa una definición de comando.</span><span class="sxs-lookup"><span data-stu-id="a0e83-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="a0e83-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a0e83-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="a0e83-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0e83-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0e83-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a0e83-108">Attribute</span></span></th>
<th><span data-ttu-id="a0e83-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0e83-109">Type</span></span></th>
<th><span data-ttu-id="a0e83-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0e83-110">Required</span></span></th>
<th><span data-ttu-id="a0e83-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e83-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0e83-112"><strong>Comentario</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-114">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-114">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-115">Se utiliza para anotar el elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="a0e83-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-117">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0e83-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="a0e83-118">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0e83-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0e83-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-120">XS: positiveInteger Union XS: String</span><span class="sxs-lookup"><span data-stu-id="a0e83-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-121">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-121">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-122">IDENTIFICADOR de recurso único.</span><span class="sxs-lookup"><span data-stu-id="a0e83-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="a0e83-123">
<dt><span></span><span></span><strong></strong> (La Unión de XS: positiveInteger y XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-124">Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a0e83-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="a0e83-125">La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales.</span><span class="sxs-lookup"><span data-stu-id="a0e83-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0e83-126"><strong>KeyTip</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-128">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-128">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-129">Cadena que representa el método abreviado de teclado de un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="a0e83-130">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-131">Cadena formada por una secuencia de caracteres, incluido el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="a0e83-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0e83-132"><strong>LabelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-134">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-134">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-135">Cadena que representa el texto que se muestra en un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="a0e83-136">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-137">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0e83-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0e83-138"><strong>LabelTitle</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-140">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-140">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-141">Cadena que representa el texto que se muestra en un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="a0e83-142">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-143">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0e83-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0e83-144"><strong>Nombre</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-146">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-146">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-147"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-148">Una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="a0e83-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="a0e83-149">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0e83-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0e83-150"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-152">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-152">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-153"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-154">Una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="a0e83-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="a0e83-155">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0e83-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0e83-156"><strong>TooltipDescription</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-158">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-158">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-159">Cadena que representa el texto que se muestra en un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="a0e83-160">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-161">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0e83-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0e83-162"><strong>TooltipTitle</strong></span><span class="sxs-lookup"><span data-stu-id="a0e83-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="a0e83-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0e83-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0e83-164">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-164">No</span></span><br/></td>
<td><span data-ttu-id="a0e83-165">Cadena que representa el texto que se muestra en un elemento Command.</span><span class="sxs-lookup"><span data-stu-id="a0e83-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="a0e83-166">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0e83-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0e83-167">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a0e83-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a0e83-168">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0e83-168">Child elements</span></span>



| <span data-ttu-id="a0e83-169">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0e83-169">Element</span></span>                                                                                                     | <span data-ttu-id="a0e83-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e83-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="a0e83-171">**Comando. Comment**</span><span class="sxs-lookup"><span data-stu-id="a0e83-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="a0e83-172">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="a0e83-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="a0e83-174">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-175">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="a0e83-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="a0e83-176">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-177">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="a0e83-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="a0e83-178">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-179">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="a0e83-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="a0e83-180">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-181">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="a0e83-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="a0e83-182">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-183">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="a0e83-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="a0e83-184">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="a0e83-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="a0e83-186">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-187">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="a0e83-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="a0e83-188">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-189">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="a0e83-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="a0e83-190">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-191">**Comando. Symbol**</span><span class="sxs-lookup"><span data-stu-id="a0e83-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="a0e83-192">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-193">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="a0e83-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="a0e83-194">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="a0e83-195">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="a0e83-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="a0e83-196">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a0e83-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a0e83-197">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a0e83-197">Parent elements</span></span>



| <span data-ttu-id="a0e83-198">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0e83-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0e83-199">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="a0e83-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a0e83-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0e83-200">Remarks</span></span>

<span data-ttu-id="a0e83-201">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e83-201">Required.</span></span>

<span data-ttu-id="a0e83-202">Puede producirse una o varias veces para cada elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e83-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="a0e83-203">Los elementos secundarios del elemento **Command** pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="a0e83-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="a0e83-204">Normalmente, los recursos de comando se declaran en el marcado de la cinta de opciones, pero también se pueden establecer en tiempo de ejecución con una llamada a [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="a0e83-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="a0e83-205">Por ejemplo, es posible establecer la propiedad [ \_ \_ KeyTip PKEY](windowsribbon-reference-properties-uipkey-keytip.md) de la interfaz de usuario para un comando en lugar de declarar un valor en el marcado con el elemento [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e83-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="a0e83-206">En los casos en los que las propiedades de comando, como etiquetas e imágenes, no se pueden establecer con [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , se pueden invalidar con una llamada a [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="a0e83-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="a0e83-207">Después de la invalidación, el marco de trabajo consulta la aplicación host para ver los detalles del recurso.</span><span class="sxs-lookup"><span data-stu-id="a0e83-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="a0e83-208">Un recurso no se puede restablecer desde la tabla de recursos de marcado una vez que se ha invalidado.</span><span class="sxs-lookup"><span data-stu-id="a0e83-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="a0e83-209">Una definición de comando se agrega al archivo de encabezado de marca de la cinta de opciones para cada **comando** declarado en el marcado.</span><span class="sxs-lookup"><span data-stu-id="a0e83-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="a0e83-210">El valor de *KeyTip* actúa como la tecla de aceleración para un comando, a menos que ese comando se exponga a través de un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="a0e83-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="a0e83-211">En este caso, el marco de trabajo omite el valor de *KeyTip* y, en su lugar, usa un carácter precedido por una y comercial según lo especificado por *LabelTitle* o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a0e83-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="a0e83-212">Si el *LabelTitle* o la etiqueta PKEY de IU no especifican el carácter de y comercial \_ \_ , no se expone ningún KeyTip ni tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="a0e83-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="a0e83-213">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a0e83-213">Examples</span></span>

<span data-ttu-id="a0e83-214">En el ejemplo siguiente se muestra un manifiesto de elementos **Command** para una pestaña **Home** .</span><span class="sxs-lookup"><span data-stu-id="a0e83-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="a0e83-215">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a0e83-215">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a0e83-216">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0e83-216">Minimum supported system</span></span><br/> | <span data-ttu-id="a0e83-217">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0e83-217">Windows 7</span></span> |
| <span data-ttu-id="a0e83-218">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a0e83-218">Can be empty</span></span>                        | <span data-ttu-id="a0e83-219">No</span><span class="sxs-lookup"><span data-stu-id="a0e83-219">No</span></span>        |



 


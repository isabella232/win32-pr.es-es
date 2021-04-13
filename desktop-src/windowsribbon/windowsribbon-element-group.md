---
title: Group, elemento
description: Representa un control de grupo que funciona como un contenedor para un grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Cinta de opciones de Windows elemento de grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421039"
---
# <a name="group-element"></a><span data-ttu-id="975ca-104">Group, elemento</span><span class="sxs-lookup"><span data-stu-id="975ca-104">Group element</span></span>

<span data-ttu-id="975ca-105">Representa un control de [Grupo](windowsribbon-controls-group.md) que funciona como un contenedor para un grupo de elementos.</span><span class="sxs-lookup"><span data-stu-id="975ca-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="975ca-106">Uso</span><span class="sxs-lookup"><span data-stu-id="975ca-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="975ca-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="975ca-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="975ca-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="975ca-108">Attribute</span></span></th>
<th><span data-ttu-id="975ca-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="975ca-109">Type</span></span></th>
<th><span data-ttu-id="975ca-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="975ca-110">Required</span></span></th>
<th><span data-ttu-id="975ca-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="975ca-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="975ca-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="975ca-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="975ca-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="975ca-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="975ca-114">No</span><span class="sxs-lookup"><span data-stu-id="975ca-114">No</span></span><br/></td>
<td><span data-ttu-id="975ca-115"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="975ca-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="975ca-116">Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="975ca-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="975ca-117">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="975ca-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="975ca-118">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="975ca-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="975ca-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="975ca-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="975ca-120">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="975ca-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="975ca-121">No</span><span class="sxs-lookup"><span data-stu-id="975ca-121">No</span></span><br/></td>
<td><span data-ttu-id="975ca-122">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="975ca-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="975ca-123">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="975ca-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="975ca-124">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="975ca-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="975ca-125">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="975ca-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="975ca-126">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="975ca-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="975ca-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="975ca-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="975ca-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="975ca-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="975ca-129">No</span><span class="sxs-lookup"><span data-stu-id="975ca-129">No</span></span><br/></td>
<td><span data-ttu-id="975ca-130">Cuando se especifica, el valor de <em>SizeDefinition</em> está restringido a una de las <a href="windowsribbon-templates.md">plantillas de diseño</a> definidas por el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="975ca-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="975ca-131">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="975ca-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="975ca-132">Cualquier secuencia de cero o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="975ca-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="975ca-133">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="975ca-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="975ca-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="975ca-134">Child elements</span></span>



| <span data-ttu-id="975ca-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="975ca-135">Element</span></span>                                                                             | <span data-ttu-id="975ca-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="975ca-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="975ca-137">**Botón**</span><span class="sxs-lookup"><span data-stu-id="975ca-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="975ca-138">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-139">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="975ca-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="975ca-140">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="975ca-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="975ca-142">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="975ca-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="975ca-144">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="975ca-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="975ca-146">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="975ca-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="975ca-148">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="975ca-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="975ca-150">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="975ca-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="975ca-152">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="975ca-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="975ca-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="975ca-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="975ca-154">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="975ca-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="975ca-156">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="975ca-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="975ca-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="975ca-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="975ca-158">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="975ca-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="975ca-160">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="975ca-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="975ca-162">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="975ca-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="975ca-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="975ca-164">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="975ca-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="975ca-165">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="975ca-165">Parent elements</span></span>



| <span data-ttu-id="975ca-166">Elemento</span><span class="sxs-lookup"><span data-stu-id="975ca-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="975ca-167">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="975ca-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="975ca-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="975ca-168">Remarks</span></span>

<span data-ttu-id="975ca-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="975ca-169">Optional.</span></span>

<span data-ttu-id="975ca-170">Puede producirse una o varias veces para cada elemento de [**ficha**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="975ca-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="975ca-171">La [**pestaña**](windowsribbon-element-tab.md) admite los [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="975ca-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="975ca-172">El marcado de la cinta de opciones solo es válido cuando los elementos secundarios del **Grupo** corresponden a la plantilla especificada para *SizeDefinition*.</span><span class="sxs-lookup"><span data-stu-id="975ca-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="975ca-173">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="975ca-173">Examples</span></span>

<span data-ttu-id="975ca-174">En el ejemplo de código siguiente se muestra el uso de una plantilla personalizada en un **Grupo**.</span><span class="sxs-lookup"><span data-stu-id="975ca-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="975ca-175">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="975ca-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="975ca-176">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="975ca-176">Minimum supported system</span></span><br/> | <span data-ttu-id="975ca-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="975ca-177">Windows 7</span></span> |
| <span data-ttu-id="975ca-178">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="975ca-178">Can be empty</span></span>                        | <span data-ttu-id="975ca-179">No</span><span class="sxs-lookup"><span data-stu-id="975ca-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="975ca-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="975ca-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975ca-181">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="975ca-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="975ca-182">Control de grupo</span><span class="sxs-lookup"><span data-stu-id="975ca-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="975ca-183">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="975ca-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


---
title: Elemento MenuGroup
description: Representa un contenedor de controles que se van a mostrar en una galería, un menú o una barra de herramientas.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup cinta de opciones de Windows
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103787485"
---
# <a name="menugroup-element"></a><span data-ttu-id="47133-104">Elemento MenuGroup</span><span class="sxs-lookup"><span data-stu-id="47133-104">MenuGroup element</span></span>

<span data-ttu-id="47133-105">Representa un contenedor de controles que se van a mostrar en una galería, un menú o una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="47133-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="47133-106">Uso</span><span class="sxs-lookup"><span data-stu-id="47133-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="47133-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="47133-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47133-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="47133-108">Attribute</span></span></th>
<th><span data-ttu-id="47133-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="47133-109">Type</span></span></th>
<th><span data-ttu-id="47133-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="47133-110">Required</span></span></th>
<th><span data-ttu-id="47133-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="47133-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="47133-112"><strong>Clase</strong></span><span class="sxs-lookup"><span data-stu-id="47133-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="47133-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="47133-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="47133-114">No</span><span class="sxs-lookup"><span data-stu-id="47133-114">No</span></span><br/></td>
<td><span data-ttu-id="47133-115">Especifica el tamaño y el estilo de diseño de los elementos de la interfaz de usuario del menú.</span><span class="sxs-lookup"><span data-stu-id="47133-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="47133-116">Un recurso de imagen se puede proporcionar en dos tamaños (grande y pequeño) y asociarse al elemento en el marcado mediante los elementos de propiedad <a href="windowsribbon-element-command-largeimages.md"><strong>Command. LargeImages</strong></a> y <a href="windowsribbon-element-command-smallimages.md"><strong>Command. SmallImages</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="47133-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="47133-117">Si solo se proporciona una imagen, el marco de trabajo lo cambia según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="47133-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="47133-118">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="47133-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="47133-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span><span class="sxs-lookup"><span data-stu-id="47133-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="47133-120">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="47133-120">Default.</span></span> <br/> <span data-ttu-id="47133-121">Estilo: imagen pequeña y texto desacentuado.</span><span class="sxs-lookup"><span data-stu-id="47133-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="47133-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span><span class="sxs-lookup"><span data-stu-id="47133-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="47133-123">Estilo: imagen grande y texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="47133-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="47133-124">Si <strong>MenuGroup</strong> es un elemento secundario de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, se omite el atributo de <em>clase</em> y <code>MajorItems</code> el marco de trabajo aplica un estilo de.</span><span class="sxs-lookup"><span data-stu-id="47133-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47133-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="47133-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="47133-126">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="47133-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="47133-127">No</span><span class="sxs-lookup"><span data-stu-id="47133-127">No</span></span><br/></td>
<td><span data-ttu-id="47133-128">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="47133-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="47133-129">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="47133-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="47133-130">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="47133-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="47133-131">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="47133-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="47133-132">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47133-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="47133-133">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47133-133">Child elements</span></span>



| <span data-ttu-id="47133-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="47133-134">Element</span></span>                                                                             | <span data-ttu-id="47133-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="47133-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="47133-136">**Botón**</span><span class="sxs-lookup"><span data-stu-id="47133-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="47133-137">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-138">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="47133-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="47133-139">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="47133-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="47133-141">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="47133-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="47133-143">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="47133-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="47133-145">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="47133-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="47133-147">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-148">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="47133-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="47133-149">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="47133-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="47133-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="47133-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="47133-151">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="47133-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="47133-153">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="47133-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="47133-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="47133-155">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="47133-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="47133-156">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="47133-156">Parent elements</span></span>



| <span data-ttu-id="47133-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="47133-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47133-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="47133-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="47133-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="47133-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="47133-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="47133-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="47133-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="47133-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="47133-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="47133-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="47133-163">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="47133-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="47133-164">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="47133-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="47133-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="47133-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="47133-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47133-166">Remarks</span></span>

<span data-ttu-id="47133-167">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="47133-167">Required.</span></span>

<span data-ttu-id="47133-168">Debe producirse al menos una vez para cada elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**splitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)o [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) .</span><span class="sxs-lookup"><span data-stu-id="47133-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="47133-169">Si [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario, **MenuGroup** está restringido a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="47133-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="47133-170">Si [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery. MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery. MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**splitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)o [**SplitButtonGallery. MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) es el elemento principal, entonces **MenuGroup** está restringido a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**splitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="47133-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="47133-171">Si [**MiniToolbar**](windowsribbon-element-minitoolbar.md) es el elemento primario, **MenuGroup** está restringido a los siguientes elementos secundarios: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**splitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="47133-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="47133-172">El atributo class no es necesario cuando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="47133-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="47133-173">El marco de trabajo aplica un valor de MajorItems para el atributo de clase.</span><span class="sxs-lookup"><span data-stu-id="47133-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="47133-174">Cuando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) es el elemento primario, el atributo de clase no es necesario.</span><span class="sxs-lookup"><span data-stu-id="47133-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="47133-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47133-175">Examples</span></span>

<span data-ttu-id="47133-176">En el ejemplo siguiente se muestra el marcado básico para [**splitButton**](windowsribbon-element-splitbutton.md) con un elemento **MenuGroup** .</span><span class="sxs-lookup"><span data-stu-id="47133-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="47133-177">En esta sección de código se muestran las declaraciones de comandos [**splitButton**](windowsribbon-element-splitbutton.md) y **MenuGroup** con un recurso de imagen grande y pequeño.</span><span class="sxs-lookup"><span data-stu-id="47133-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="47133-178">También se declara un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="47133-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="47133-179">En esta sección de código se muestran las declaraciones de control [**splitButton**](windowsribbon-element-splitbutton.md) y **MenuGroup** con `StandardItems` y `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="47133-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="47133-180">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="47133-180">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="47133-181">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47133-181">Minimum supported system</span></span><br/> | <span data-ttu-id="47133-182">Windows 7</span><span class="sxs-lookup"><span data-stu-id="47133-182">Windows 7</span></span> |
| <span data-ttu-id="47133-183">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="47133-183">Can be empty</span></span>                        | <span data-ttu-id="47133-184">No</span><span class="sxs-lookup"><span data-stu-id="47133-184">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="47133-185">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47133-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47133-186">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="47133-186">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="47133-187">Grupo de menús</span><span class="sxs-lookup"><span data-stu-id="47133-187">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 






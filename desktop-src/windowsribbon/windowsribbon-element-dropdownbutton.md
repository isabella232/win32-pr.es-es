---
title: Elemento DropDownButton
description: Representa un control de botón de Drop-Down estándar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- DropDownButton cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793066"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="a0a2f-104">Elemento DropDownButton</span><span class="sxs-lookup"><span data-stu-id="a0a2f-104">DropDownButton element</span></span>

<span data-ttu-id="a0a2f-105">Representa un control de [botón de lista](windowsribbon-controls-dropdownbutton.md) desplegable estándar.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a0a2f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a0a2f-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="a0a2f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0a2f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0a2f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a0a2f-108">Attribute</span></span></th>
<th><span data-ttu-id="a0a2f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0a2f-109">Type</span></span></th>
<th><span data-ttu-id="a0a2f-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0a2f-110">Required</span></span></th>
<th><span data-ttu-id="a0a2f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0a2f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0a2f-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="a0a2f-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="a0a2f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0a2f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0a2f-114">No</span><span class="sxs-lookup"><span data-stu-id="a0a2f-114">No</span></span><br/></td>
<td><span data-ttu-id="a0a2f-115">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="a0a2f-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0a2f-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0a2f-117">Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="a0a2f-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="a0a2f-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0a2f-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a0a2f-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a0a2f-121">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="a0a2f-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a0a2f-122">No</span><span class="sxs-lookup"><span data-stu-id="a0a2f-122">No</span></span><br/></td>
<td><span data-ttu-id="a0a2f-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a0a2f-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="a0a2f-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0a2f-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a0a2f-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a0a2f-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a0a2f-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0a2f-128">Child elements</span></span>



| <span data-ttu-id="a0a2f-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0a2f-129">Element</span></span>                                                                             | <span data-ttu-id="a0a2f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0a2f-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a0a2f-131">**Botón**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="a0a2f-132">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-133">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="a0a2f-134">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="a0a2f-136">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="a0a2f-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="a0a2f-138">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="a0a2f-140">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="a0a2f-142">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="a0a2f-144">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="a0a2f-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="a0a2f-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="a0a2f-146">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="a0a2f-148">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0a2f-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="a0a2f-150">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a0a2f-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a0a2f-151">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a0a2f-151">Parent elements</span></span>



| <span data-ttu-id="a0a2f-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0a2f-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a0a2f-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="a0a2f-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="a0a2f-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="a0a2f-156">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="a0a2f-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="a0a2f-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="a0a2f-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a0a2f-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0a2f-160">Remarks</span></span>

<span data-ttu-id="a0a2f-161">Opcional o obligatorio, dependiendo del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="a0a2f-162">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="a0a2f-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="a0a2f-163">**DropDownButton** admite los [modos de aplicación](ribbon-applicationmodes.md) cuando se hospeda en la columna izquierda del menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="a0a2f-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) y [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) no son elementos secundarios válidos de **DropDownButton** cuando **DropDownButton** es un descendiente de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="a0a2f-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0a2f-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a0a2f-165">Examples</span></span>

<span data-ttu-id="a0a2f-166">En el ejemplo siguiente se muestra el marcado básico para **DropDownButton**.</span><span class="sxs-lookup"><span data-stu-id="a0a2f-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="a0a2f-167">En esta sección de código se muestran las declaraciones de comandos de **DropDownButton** , con un [**Grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario para el elemento **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="a0a2f-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="a0a2f-168">En esta sección de código se muestran las declaraciones de control de **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="a0a2f-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="a0a2f-169">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a0a2f-169">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a0a2f-170">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0a2f-170">Minimum supported system</span></span><br/> | <span data-ttu-id="a0a2f-171">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0a2f-171">Windows 7</span></span> |
| <span data-ttu-id="a0a2f-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a0a2f-172">Can be empty</span></span>                        | <span data-ttu-id="a0a2f-173">No</span><span class="sxs-lookup"><span data-stu-id="a0a2f-173">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="a0a2f-174">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a0a2f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a2f-175">Control de botón desplegable</span><span class="sxs-lookup"><span data-stu-id="a0a2f-175">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="a0a2f-176">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="a0a2f-176">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 


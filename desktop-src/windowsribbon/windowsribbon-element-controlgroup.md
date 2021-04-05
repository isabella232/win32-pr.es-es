---
title: Elemento ControlGroup
description: Representa un grupo de controles en una plantilla de diseño SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- ControlGroup cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420177"
---
# <a name="controlgroup-element"></a><span data-ttu-id="1c67d-104">Elemento ControlGroup</span><span class="sxs-lookup"><span data-stu-id="1c67d-104">ControlGroup element</span></span>

<span data-ttu-id="1c67d-105">Representa un grupo de controles en una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="1c67d-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="1c67d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="1c67d-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="1c67d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c67d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c67d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="1c67d-108">Attribute</span></span></th>
<th><span data-ttu-id="1c67d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c67d-109">Type</span></span></th>
<th><span data-ttu-id="1c67d-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1c67d-110">Required</span></span></th>
<th><span data-ttu-id="1c67d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c67d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c67d-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="1c67d-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="1c67d-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="1c67d-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="1c67d-114">No</span><span class="sxs-lookup"><span data-stu-id="1c67d-114">No</span></span><br/></td>
<td><span data-ttu-id="1c67d-115">Solo es válido cuando <a href="windowsribbon-element-group.md"><strong>Group</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1c67d-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="1c67d-116">Cada <em>SequenceNumber</em> debe ser único dentro de un elemento <a href="windowsribbon-element-group.md"><strong>Group</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c67d-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="1c67d-117">Los valores de <em>SequenceNumber</em> deben aumentar para cada elemento <strong>Group</strong> , pero no es necesario que sean secuenciales.</span><span class="sxs-lookup"><span data-stu-id="1c67d-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="1c67d-118">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="1c67d-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="1c67d-119">Cualquier valor entero positivo comprendido entre 1000 y 59999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="1c67d-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1c67d-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c67d-120">Child elements</span></span>



| <span data-ttu-id="1c67d-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c67d-121">Element</span></span>                                                                                 | <span data-ttu-id="1c67d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c67d-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="1c67d-123">**Botón**</span><span class="sxs-lookup"><span data-stu-id="1c67d-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="1c67d-124">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-125">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="1c67d-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="1c67d-126">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="1c67d-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="1c67d-128">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="1c67d-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="1c67d-130">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="1c67d-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="1c67d-132">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="1c67d-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="1c67d-134">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="1c67d-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="1c67d-136">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="1c67d-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="1c67d-138">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="1c67d-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="1c67d-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="1c67d-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="1c67d-140">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="1c67d-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="1c67d-142">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1c67d-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="1c67d-144">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="1c67d-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="1c67d-146">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="1c67d-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="1c67d-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="1c67d-148">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="1c67d-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1c67d-149">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1c67d-149">Parent elements</span></span>



| <span data-ttu-id="1c67d-150">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c67d-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c67d-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="1c67d-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="1c67d-152">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="1c67d-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="1c67d-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="1c67d-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="1c67d-154">**Row**</span><span class="sxs-lookup"><span data-stu-id="1c67d-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="1c67d-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c67d-155">Remarks</span></span>

<span data-ttu-id="1c67d-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1c67d-156">Optional.</span></span>

<span data-ttu-id="1c67d-157">Puede producirse una o varias veces para cada [**Grupo**](windowsribbon-element-group.md) o elemento **ControlGroup** .</span><span class="sxs-lookup"><span data-stu-id="1c67d-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="1c67d-158">Si no se proporciona ningún número de secuencia, los elementos se representan en el orden especificado en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="1c67d-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="1c67d-159">Si [**Group**](windowsribbon-element-group.md) o **ControlGroup** es el elemento primario, **ControlGroup** está restringido a los siguientes elementos secundarios posibles: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**splitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="1c67d-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="1c67d-160">De lo contrario, cuando [**Row**](windowsribbon-element-row.md) o [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) es el elemento primario, el [**Grupo**](windowsribbon-element-group.md) está restringido al siguiente elemento secundario posible: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="1c67d-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1c67d-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c67d-161">Examples</span></span>

<span data-ttu-id="1c67d-162">En el ejemplo de código siguiente se muestra el marcado básico de una plantilla personalizada de diseño de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de cuatro botones con varios elementos de [**Grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="1c67d-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="1c67d-163">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1c67d-163">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="1c67d-164">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c67d-164">Minimum supported system</span></span><br/> | <span data-ttu-id="1c67d-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c67d-165">Windows 7</span></span> |
| <span data-ttu-id="1c67d-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1c67d-166">Can be empty</span></span>                        | <span data-ttu-id="1c67d-167">No</span><span class="sxs-lookup"><span data-stu-id="1c67d-167">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="1c67d-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c67d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c67d-169">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="1c67d-169">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






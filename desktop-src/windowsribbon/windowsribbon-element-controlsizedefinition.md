---
title: Elemento ControlSizeDefinition
description: Representa el estilo de diseño de un grupo de controles en una plantilla personalizada.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- ControlSizeDefinition, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff5217c08b4ea6da1931b0c65501f912f2cc5dc
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443416"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="2cc35-104">Elemento ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="2cc35-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="2cc35-105">Representa el estilo de diseño de un grupo de controles en una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="2cc35-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="2cc35-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2cc35-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="2cc35-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2cc35-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cc35-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cc35-108">Attribute</span></span></th>
<th><span data-ttu-id="2cc35-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cc35-109">Type</span></span></th>
<th><span data-ttu-id="2cc35-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="2cc35-110">Required</span></span></th>
<th><span data-ttu-id="2cc35-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cc35-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cc35-112"><strong>ControlName</strong></span><span class="sxs-lookup"><span data-stu-id="2cc35-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="2cc35-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="2cc35-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2cc35-114">No</span><span class="sxs-lookup"><span data-stu-id="2cc35-114">No</span></span><br/></td>
<td><span data-ttu-id="2cc35-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="2cc35-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2cc35-116">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2cc35-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2cc35-117">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2cc35-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2cc35-118">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2cc35-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cc35-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="2cc35-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="2cc35-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="2cc35-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="2cc35-121">No</span><span class="sxs-lookup"><span data-stu-id="2cc35-121">No</span></span><br/></td>
<td><span data-ttu-id="2cc35-122">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2cc35-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2cc35-123">
<dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="2cc35-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2cc35-124"><dt><span></span><span></span><strong></strong> (Pequeño)</span><span class="sxs-lookup"><span data-stu-id="2cc35-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="2cc35-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cc35-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cc35-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="2cc35-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="2cc35-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="2cc35-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="2cc35-128">No</span><span class="sxs-lookup"><span data-stu-id="2cc35-128">No</span></span><br/></td>
<td><span data-ttu-id="2cc35-129">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="2cc35-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2cc35-130">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="2cc35-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2cc35-131">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cc35-131">Default.</span></span> <br/> </dd> <span data-ttu-id="2cc35-132"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="2cc35-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cc35-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="2cc35-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="2cc35-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="2cc35-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="2cc35-135">No</span><span class="sxs-lookup"><span data-stu-id="2cc35-135">No</span></span><br/></td>
<td><span data-ttu-id="2cc35-136">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="2cc35-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2cc35-137">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="2cc35-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2cc35-138">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cc35-138">Default.</span></span> <br/> </dd> <span data-ttu-id="2cc35-139"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="2cc35-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cc35-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="2cc35-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="2cc35-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="2cc35-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="2cc35-142">No</span><span class="sxs-lookup"><span data-stu-id="2cc35-142">No</span></span><br/></td>
<td><span data-ttu-id="2cc35-143">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="2cc35-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2cc35-144">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="2cc35-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2cc35-145"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="2cc35-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2cc35-146">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2cc35-146">Child elements</span></span>

<span data-ttu-id="2cc35-147">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="2cc35-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2cc35-148">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2cc35-148">Parent elements</span></span>



| <span data-ttu-id="2cc35-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="2cc35-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cc35-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="2cc35-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="2cc35-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2cc35-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="2cc35-152">**Fila**</span><span class="sxs-lookup"><span data-stu-id="2cc35-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="2cc35-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cc35-153">Remarks</span></span>

<span data-ttu-id="2cc35-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cc35-154">Optional.</span></span>

<span data-ttu-id="2cc35-155">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md)o [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2cc35-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2cc35-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2cc35-156">Examples</span></span>

<span data-ttu-id="2cc35-157">En el ejemplo de código siguiente se muestra el marcado básico para una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con varios **elementos ControlSizeDefinition.**</span><span class="sxs-lookup"><span data-stu-id="2cc35-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2cc35-158">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2cc35-158">Element information</span></span>

* <span data-ttu-id="2cc35-159">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cc35-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="2cc35-160">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="2cc35-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="2cc35-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cc35-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc35-162">Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="2cc35-162">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






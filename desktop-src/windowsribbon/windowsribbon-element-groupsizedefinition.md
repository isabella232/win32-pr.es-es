---
title: Elemento GroupSizeDefinition
description: Representa un tamaño de diseño de un grupo de controles en una plantilla personalizada.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition cinta de opciones de Windows
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cf166dbf428c9d17beb148887cc94be73dc11a0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704869"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="5884e-104">Elemento GroupSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="5884e-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="5884e-105">Representa un tamaño de diseño de un grupo de controles en una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="5884e-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="5884e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="5884e-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="5884e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5884e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5884e-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="5884e-108">Attribute</span></span></th>
<th><span data-ttu-id="5884e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5884e-109">Type</span></span></th>
<th><span data-ttu-id="5884e-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5884e-110">Required</span></span></th>
<th><span data-ttu-id="5884e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5884e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5884e-112"><strong>Tamaño</strong></span><span class="sxs-lookup"><span data-stu-id="5884e-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="5884e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="5884e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="5884e-114">No</span><span class="sxs-lookup"><span data-stu-id="5884e-114">No</span></span><br/></td>
<td><span data-ttu-id="5884e-115">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5884e-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="5884e-116">
<dt><span></span><span></span><strong></strong> Amplíe</span><span class="sxs-lookup"><span data-stu-id="5884e-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="5884e-117">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5884e-117">Default.</span></span> <br/> </dd> <span data-ttu-id="5884e-118"><dt><span></span><span></span><strong></strong> Medio</span><span class="sxs-lookup"><span data-stu-id="5884e-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5884e-119"><dt><span></span><span></span><strong></strong> Pequeño</span><span class="sxs-lookup"><span data-stu-id="5884e-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5884e-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5884e-120">Child elements</span></span>



| <span data-ttu-id="5884e-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="5884e-121">Element</span></span>                                                                                 | <span data-ttu-id="5884e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5884e-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5884e-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="5884e-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="5884e-124">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5884e-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5884e-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="5884e-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="5884e-126">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5884e-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5884e-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="5884e-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="5884e-128">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5884e-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5884e-129">**Row**</span><span class="sxs-lookup"><span data-stu-id="5884e-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="5884e-130">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5884e-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5884e-131">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5884e-131">Parent elements</span></span>



| <span data-ttu-id="5884e-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="5884e-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="5884e-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="5884e-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5884e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5884e-134">Remarks</span></span>

<span data-ttu-id="5884e-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5884e-135">Optional.</span></span>

<span data-ttu-id="5884e-136">Puede producirse hasta tres veces para cada elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) (una vez por cada *tamaño*).</span><span class="sxs-lookup"><span data-stu-id="5884e-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="5884e-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5884e-137">Examples</span></span>

<span data-ttu-id="5884e-138">En el ejemplo de código siguiente se muestra una plantilla personalizada básica que incluye los tres tamaños de diseño de grupo que se deben definir con el elemento **GroupSizeDefinition** al crear una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="5884e-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5884e-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5884e-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5884e-140">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5884e-140">Minimum supported system</span></span><br/> | <span data-ttu-id="5884e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5884e-141">Windows 7</span></span> |
| <span data-ttu-id="5884e-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5884e-142">Can be empty</span></span>                        | <span data-ttu-id="5884e-143">No</span><span class="sxs-lookup"><span data-stu-id="5884e-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="5884e-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5884e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5884e-145">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="5884e-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






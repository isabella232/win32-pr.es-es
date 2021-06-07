---
title: Elemento GroupSizeDefinition
description: Representa un tamaño de diseño para un grupo de controles en una plantilla personalizada.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- GroupSizeDefinition, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 650301a29ace2c6df9316a315d4cdbad448e5573
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443386"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="e668f-104">Elemento GroupSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="e668f-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="e668f-105">Representa un tamaño de diseño para un grupo de controles en una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="e668f-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="e668f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e668f-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="e668f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e668f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e668f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="e668f-108">Attribute</span></span></th>
<th><span data-ttu-id="e668f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e668f-109">Type</span></span></th>
<th><span data-ttu-id="e668f-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="e668f-110">Required</span></span></th>
<th><span data-ttu-id="e668f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e668f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e668f-112"><strong>Tamaño</strong></span><span class="sxs-lookup"><span data-stu-id="e668f-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="e668f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e668f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e668f-114">No</span><span class="sxs-lookup"><span data-stu-id="e668f-114">No</span></span><br/></td>
<td><span data-ttu-id="e668f-115">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e668f-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="e668f-116">
<dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="e668f-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="e668f-117">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e668f-117">Default.</span></span> <br/> </dd> <span data-ttu-id="e668f-118"><dt><span></span><span></span><strong></strong> (Medio)</span><span class="sxs-lookup"><span data-stu-id="e668f-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="e668f-119"><dt><span></span><span></span><strong></strong> (Pequeño)</span><span class="sxs-lookup"><span data-stu-id="e668f-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e668f-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e668f-120">Child elements</span></span>



| <span data-ttu-id="e668f-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="e668f-121">Element</span></span>                                                                                 | <span data-ttu-id="e668f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e668f-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e668f-123">**ColumnBreak**</span><span class="sxs-lookup"><span data-stu-id="e668f-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="e668f-124">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="e668f-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e668f-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="e668f-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="e668f-126">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="e668f-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e668f-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="e668f-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="e668f-128">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="e668f-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e668f-129">**Fila**</span><span class="sxs-lookup"><span data-stu-id="e668f-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="e668f-130">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="e668f-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e668f-131">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e668f-131">Parent elements</span></span>



| <span data-ttu-id="e668f-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="e668f-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="e668f-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="e668f-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e668f-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e668f-134">Remarks</span></span>

<span data-ttu-id="e668f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e668f-135">Optional.</span></span>

<span data-ttu-id="e668f-136">Puede producirse hasta tres veces para cada [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) (una vez para cada *size*).</span><span class="sxs-lookup"><span data-stu-id="e668f-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="e668f-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e668f-137">Examples</span></span>

<span data-ttu-id="e668f-138">En el ejemplo de código siguiente se muestra una plantilla personalizada básica que incluye los tres tamaños de diseño de grupo que se deben definir con el **elemento GroupSizeDefinition** al crear una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="e668f-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e668f-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e668f-139">Element information</span></span>

* <span data-ttu-id="e668f-140">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="e668f-140">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e668f-141">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="e668f-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="e668f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e668f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e668f-143">Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="e668f-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






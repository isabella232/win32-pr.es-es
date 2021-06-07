---
title: Elemento ColumnBreak
description: Representa un separador vertical (visible u oculto) en plantillas de diseño SizeDefinition personalizadas.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Cinta de opciones de Windows del elemento ColumnBreak
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5bff1682cdf55b44092a176abd6dc7e935220a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444846"
---
# <a name="columnbreak-element"></a><span data-ttu-id="0cbf5-104">Elemento ColumnBreak</span><span class="sxs-lookup"><span data-stu-id="0cbf5-104">ColumnBreak element</span></span>

<span data-ttu-id="0cbf5-105">Representa un separador vertical (visible u oculto) en plantillas [**de diseño SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="0cbf5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0cbf5-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="0cbf5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cbf5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0cbf5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="0cbf5-108">Attribute</span></span></th>
<th><span data-ttu-id="0cbf5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cbf5-109">Type</span></span></th>
<th><span data-ttu-id="0cbf5-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="0cbf5-110">Required</span></span></th>
<th><span data-ttu-id="0cbf5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cbf5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0cbf5-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="0cbf5-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="0cbf5-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="0cbf5-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="0cbf5-114">No</span><span class="sxs-lookup"><span data-stu-id="0cbf5-114">No</span></span><br/></td>
<td><span data-ttu-id="0cbf5-115">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="0cbf5-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="0cbf5-116">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="0cbf5-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="0cbf5-117">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-117">Default.</span></span> <br/> </dd> <span data-ttu-id="0cbf5-118"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="0cbf5-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0cbf5-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0cbf5-119">Child elements</span></span>

<span data-ttu-id="0cbf5-120">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0cbf5-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0cbf5-121">Parent elements</span></span>



| <span data-ttu-id="0cbf5-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="0cbf5-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cbf5-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="0cbf5-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0cbf5-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cbf5-124">Remarks</span></span>

<span data-ttu-id="0cbf5-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-125">Optional.</span></span>

<span data-ttu-id="0cbf5-126">Puede producirse una o varias veces para cada [**elemento GroupSizeDefinition.**](windowsribbon-element-groupsizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0cbf5-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="0cbf5-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0cbf5-127">Examples</span></span>

<span data-ttu-id="0cbf5-128">En el ejemplo siguiente se muestra el marcado básico para un **elemento ColumnBreak** en una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="0cbf5-129">**ColumnBreak** solo se especifica para la `Large` plantilla.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0cbf5-130">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0cbf5-130">Element information</span></span>

* <span data-ttu-id="0cbf5-131">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="0cbf5-131">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0cbf5-132">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="0cbf5-132">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="0cbf5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cbf5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbf5-134">Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="0cbf5-134">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






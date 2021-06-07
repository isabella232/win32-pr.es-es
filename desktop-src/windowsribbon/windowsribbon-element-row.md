---
title: Elemento Row
description: Representa una fila de controles en una plantilla de diseño SizeDefinition personalizada.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Cinta de opciones de Windows del elemento Row
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445026"
---
# <a name="row-element"></a><span data-ttu-id="bf6be-104">Elemento Row</span><span class="sxs-lookup"><span data-stu-id="bf6be-104">Row element</span></span>

<span data-ttu-id="bf6be-105">Representa una fila de controles en una plantilla de diseño SizeDefinition personalizada.</span><span class="sxs-lookup"><span data-stu-id="bf6be-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="bf6be-106">Uso</span><span class="sxs-lookup"><span data-stu-id="bf6be-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="bf6be-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf6be-107">Attributes</span></span>

<span data-ttu-id="bf6be-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="bf6be-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bf6be-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf6be-109">Child elements</span></span>



| <span data-ttu-id="bf6be-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf6be-110">Element</span></span>                                                                                 | <span data-ttu-id="bf6be-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf6be-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bf6be-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="bf6be-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="bf6be-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="bf6be-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bf6be-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="bf6be-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="bf6be-115">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="bf6be-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bf6be-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="bf6be-116">Parent elements</span></span>



| <span data-ttu-id="bf6be-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf6be-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf6be-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="bf6be-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bf6be-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf6be-119">Remarks</span></span>

<span data-ttu-id="bf6be-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bf6be-120">Optional.</span></span>

<span data-ttu-id="bf6be-121">Puede producirse una o varias veces para cada [**elemento GroupSizeDefinition.**](windowsribbon-element-groupsizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="bf6be-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="bf6be-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf6be-122">Examples</span></span>

<span data-ttu-id="bf6be-123">En el ejemplo de código siguiente se muestra el marcado básico para una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con varios **elementos Row.**</span><span class="sxs-lookup"><span data-stu-id="bf6be-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="bf6be-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bf6be-124">Element information</span></span>




* <span data-ttu-id="bf6be-125">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf6be-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="bf6be-126">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="bf6be-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="bf6be-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf6be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6be-128">Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="bf6be-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






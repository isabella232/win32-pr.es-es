---
title: Elemento ControlNameDefinition
description: Representa un nombre de un control en una plantilla de diseño SizeDefinition personalizada.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- ControlNameDefinition cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14ec269ce51b0074b9a03f78aea218b482955d1b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358148"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="8f96c-104">Elemento ControlNameDefinition</span><span class="sxs-lookup"><span data-stu-id="8f96c-104">ControlNameDefinition element</span></span>

<span data-ttu-id="8f96c-105">Representa un nombre de un control en una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada.</span><span class="sxs-lookup"><span data-stu-id="8f96c-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="8f96c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8f96c-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="8f96c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f96c-107">Attributes</span></span>



| <span data-ttu-id="8f96c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="8f96c-108">Attribute</span></span>           | <span data-ttu-id="8f96c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f96c-109">Type</span></span>                                       | <span data-ttu-id="8f96c-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f96c-110">Required</span></span>      | <span data-ttu-id="8f96c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f96c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f96c-112">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8f96c-112">**Name**</span></span><br/> | <span data-ttu-id="8f96c-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="8f96c-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="8f96c-114">No</span><span class="sxs-lookup"><span data-stu-id="8f96c-114">No</span></span><br/> | <span data-ttu-id="8f96c-115"><dt> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="8f96c-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8f96c-116">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="8f96c-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8f96c-117">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="8f96c-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8f96c-118">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8f96c-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="8f96c-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f96c-119">Child elements</span></span>



| <span data-ttu-id="8f96c-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f96c-120">Element</span></span>                              | <span data-ttu-id="8f96c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f96c-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="8f96c-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="8f96c-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="8f96c-123">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="8f96c-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8f96c-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8f96c-124">Parent elements</span></span>



| <span data-ttu-id="8f96c-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f96c-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="8f96c-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="8f96c-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8f96c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f96c-127">Remarks</span></span>

<span data-ttu-id="8f96c-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f96c-128">Optional.</span></span>

<span data-ttu-id="8f96c-129">Puede producirse una o varias veces para cada elemento [**ControlNameMap**](windowsribbon-element-controlnamemap.md) .</span><span class="sxs-lookup"><span data-stu-id="8f96c-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="8f96c-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f96c-130">Examples</span></span>

<span data-ttu-id="8f96c-131">En el ejemplo de código siguiente se muestra el marcado básico de una plantilla de diseño [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizada de cuatro botones con cuatro elementos **ControlNameDefinition** .</span><span class="sxs-lookup"><span data-stu-id="8f96c-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8f96c-132">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8f96c-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8f96c-133">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f96c-133">Minimum supported system</span></span><br/> | <span data-ttu-id="8f96c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f96c-134">Windows 7</span></span> |
| <span data-ttu-id="8f96c-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8f96c-135">Can be empty</span></span>                        | <span data-ttu-id="8f96c-136">No</span><span class="sxs-lookup"><span data-stu-id="8f96c-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="8f96c-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f96c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f96c-138">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="8f96c-138">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






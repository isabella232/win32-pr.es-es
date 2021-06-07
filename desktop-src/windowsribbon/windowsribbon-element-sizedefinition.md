---
title: Elemento SizeDefinition
description: Representa una plantilla de diseño personalizada de controles de cinta de opciones.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Cinta de opciones de Windows del elemento SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444806"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="8bfc0-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="8bfc0-104">SizeDefinition element</span></span>

<span data-ttu-id="8bfc0-105">Representa una plantilla de diseño personalizada de controles de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="8bfc0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8bfc0-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="8bfc0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8bfc0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bfc0-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="8bfc0-108">Attribute</span></span></th>
<th><span data-ttu-id="8bfc0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8bfc0-109">Type</span></span></th>
<th><span data-ttu-id="8bfc0-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="8bfc0-110">Required</span></span></th>
<th><span data-ttu-id="8bfc0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bfc0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bfc0-112"><strong>Nombre</strong></span><span class="sxs-lookup"><span data-stu-id="8bfc0-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="8bfc0-113">xs:positiveInteger o xs:string o xs:token</span><span class="sxs-lookup"><span data-stu-id="8bfc0-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="8bfc0-114">Sí</span><span class="sxs-lookup"><span data-stu-id="8bfc0-114">Yes</span></span><br/></td>
<td><span data-ttu-id="8bfc0-115">Cuando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> es el elemento primario; de lo contrario, es opcional.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="8bfc0-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string o xs:token)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="8bfc0-117">Una cadena o un valor entero entre 2 y 59999, ambos incluidos, o 0x2 y 0xea5f en hexadecimal, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="8bfc0-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8bfc0-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8bfc0-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8bfc0-120">Child elements</span></span>



| <span data-ttu-id="8bfc0-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="8bfc0-121">Element</span></span>                                                                             | <span data-ttu-id="8bfc0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bfc0-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8bfc0-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="8bfc0-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="8bfc0-124">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="8bfc0-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="8bfc0-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="8bfc0-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="8bfc0-126">Debe producirse al menos una vez</span><span class="sxs-lookup"><span data-stu-id="8bfc0-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8bfc0-127">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8bfc0-127">Parent elements</span></span>



| <span data-ttu-id="8bfc0-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="8bfc0-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bfc0-129">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="8bfc0-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="8bfc0-130">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8bfc0-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8bfc0-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bfc0-131">Remarks</span></span>

<span data-ttu-id="8bfc0-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-132">Optional.</span></span>

<span data-ttu-id="8bfc0-133">Puede producirse como máximo una vez para cada [**elemento Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="8bfc0-134">Puede producirse una o varias veces para cada [**elemento Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="8bfc0-135">Las plantillas de diseño del marco de [la](windowsribbon-templates.md) cinta predefinidas se especifican con el *atributo SizeDefinition* del [**elemento Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="8bfc0-136">Si no se [**declara un elemento ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondiente para cada elemento [**Group**](windowsribbon-element-group.md) de un elemento [**Tab,**](windowsribbon-element-tab.md) se producirá un error de validación.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="8bfc0-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8bfc0-137">Examples</span></span>

<span data-ttu-id="8bfc0-138">En el ejemplo de código siguiente se muestra una plantilla personalizada básica.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8bfc0-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8bfc0-139">Element information</span></span>


- <span data-ttu-id="8bfc0-140">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bfc0-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="8bfc0-141">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="8bfc0-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="8bfc0-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bfc0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfc0-143">Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="8bfc0-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






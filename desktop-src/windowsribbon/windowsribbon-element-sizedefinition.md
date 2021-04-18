---
title: Elemento SizeDefinition
description: Representa una plantilla de diseño personalizado de controles de la cinta de opciones.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- SizeDefinition cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105704891"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="2d1e7-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="2d1e7-104">SizeDefinition element</span></span>

<span data-ttu-id="2d1e7-105">Representa una plantilla de diseño personalizado de controles de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="2d1e7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2d1e7-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="2d1e7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d1e7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d1e7-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2d1e7-108">Attribute</span></span></th>
<th><span data-ttu-id="2d1e7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d1e7-109">Type</span></span></th>
<th><span data-ttu-id="2d1e7-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2d1e7-110">Required</span></span></th>
<th><span data-ttu-id="2d1e7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d1e7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2d1e7-112"><strong>Nombre</strong></span><span class="sxs-lookup"><span data-stu-id="2d1e7-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="2d1e7-113">XS: positiveInteger o XS: String o XS: token</span><span class="sxs-lookup"><span data-stu-id="2d1e7-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="2d1e7-114">Sí</span><span class="sxs-lookup"><span data-stu-id="2d1e7-114">Yes</span></span><br/></td>
<td><span data-ttu-id="2d1e7-115">Cuando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> es el elemento primario; de lo contrario, es opcional.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="2d1e7-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String o XS: token)</span><span class="sxs-lookup"><span data-stu-id="2d1e7-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="2d1e7-117">Una cadena o un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="2d1e7-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2d1e7-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2d1e7-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d1e7-120">Child elements</span></span>



| <span data-ttu-id="2d1e7-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d1e7-121">Element</span></span>                                                                             | <span data-ttu-id="2d1e7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d1e7-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2d1e7-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="2d1e7-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="2d1e7-124">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="2d1e7-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="2d1e7-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2d1e7-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="2d1e7-126">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="2d1e7-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2d1e7-127">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2d1e7-127">Parent elements</span></span>



| <span data-ttu-id="2d1e7-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d1e7-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d1e7-129">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="2d1e7-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="2d1e7-130">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2d1e7-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2d1e7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d1e7-131">Remarks</span></span>

<span data-ttu-id="2d1e7-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-132">Optional.</span></span>

<span data-ttu-id="2d1e7-133">Puede aparecer como máximo una vez para cada elemento de [**Grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="2d1e7-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2d1e7-134">Puede producirse una o varias veces para cada elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="2d1e7-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="2d1e7-135">Las plantillas predefinidas de [diseño](windowsribbon-templates.md) del marco de cinta se especifican con el atributo *SizeDefinition* del elemento de [**Grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="2d1e7-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2d1e7-136">Si no se declara un elemento [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) correspondiente para cada elemento [**Group**](windowsribbon-element-group.md) de un elemento [**Tab**](windowsribbon-element-tab.md) , se producirá un error de validación.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="2d1e7-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2d1e7-137">Examples</span></span>

<span data-ttu-id="2d1e7-138">En el ejemplo de código siguiente se muestra una plantilla personalizada básica.</span><span class="sxs-lookup"><span data-stu-id="2d1e7-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2d1e7-139">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2d1e7-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2d1e7-140">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d1e7-140">Minimum supported system</span></span><br/> | <span data-ttu-id="2d1e7-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d1e7-141">Windows 7</span></span> |
| <span data-ttu-id="2d1e7-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2d1e7-142">Can be empty</span></span>                        | <span data-ttu-id="2d1e7-143">No</span><span class="sxs-lookup"><span data-stu-id="2d1e7-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="2d1e7-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2d1e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d1e7-145">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="2d1e7-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






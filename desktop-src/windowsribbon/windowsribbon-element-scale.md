---
title: Elemento Scale
description: Representa la preferencia de tamaño y diseño de un grupo de controles a través de un par Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Escala de elementos de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445016"
---
# <a name="scale-element"></a><span data-ttu-id="e6a6d-104">Elemento Scale</span><span class="sxs-lookup"><span data-stu-id="e6a6d-104">Scale element</span></span>

<span data-ttu-id="e6a6d-105">Representa el tamaño y la preferencia de diseño de [**un grupo de**](windowsribbon-element-group.md) controles a través de un par {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="e6a6d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e6a6d-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="e6a6d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6a6d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6a6d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="e6a6d-108">Attribute</span></span></th>
<th><span data-ttu-id="e6a6d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6a6d-109">Type</span></span></th>
<th><span data-ttu-id="e6a6d-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="e6a6d-110">Required</span></span></th>
<th><span data-ttu-id="e6a6d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6a6d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6a6d-112"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="e6a6d-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="e6a6d-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="e6a6d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e6a6d-114">Sí</span><span class="sxs-lookup"><span data-stu-id="e6a6d-114">Yes</span></span><br/></td>
<td><span data-ttu-id="e6a6d-115">Debe corresponder a un <a href="windowsribbon-element-group.md"><strong>elemento Group</strong></a> <em>CommandName existente.</em></span><span class="sxs-lookup"><span data-stu-id="e6a6d-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="e6a6d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e6a6d-117">Una cadena o un valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e6a6d-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e6a6d-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6a6d-120"><strong>Tamaño</strong></span><span class="sxs-lookup"><span data-stu-id="e6a6d-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="e6a6d-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e6a6d-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="e6a6d-122">Sí</span><span class="sxs-lookup"><span data-stu-id="e6a6d-122">Yes</span></span><br/></td>
<td><span data-ttu-id="e6a6d-123">Este valor debe corresponder a uno de los tamaños <a href="windowsribbon-element-group.md"><strong></strong></a> válidos para el <em>atributo SizeDefinition</em> del grupo de controles asociado especificado en <em>group</em>.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="e6a6d-124">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e6a6d-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="e6a6d-125">
<dt><span></span><span></span><strong></strong> (Popup)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="e6a6d-126">Diseño de control idéntico a pero hospedado en un panel emergente o <code>Large</code> desplegable.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="e6a6d-127"><dt><span></span><span></span><strong></strong> (Pequeño)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="e6a6d-128">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeña.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="e6a6d-129"><dt><span></span><span></span><strong></strong> (Medio)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="e6a6d-130">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>Tamaño medioDefinición.</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6a6d-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="e6a6d-131"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="e6a6d-132">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e6a6d-133">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6a6d-133">Child elements</span></span>

<span data-ttu-id="e6a6d-134">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e6a6d-135">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e6a6d-135">Parent elements</span></span>



| <span data-ttu-id="e6a6d-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="e6a6d-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6a6d-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="e6a6d-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="e6a6d-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="e6a6d-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e6a6d-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6a6d-139">Remarks</span></span>

<span data-ttu-id="e6a6d-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-140">Optional.</span></span>

<span data-ttu-id="e6a6d-141">Puede producirse una o varias veces para [**cada ScalingPolicy**](windowsribbon-element-scalingpolicy.md) o [**ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)</span><span class="sxs-lookup"><span data-stu-id="e6a6d-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="e6a6d-142">Cada par de atributos *(Group*, *Size)* debe ser único.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="e6a6d-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e6a6d-143">Examples</span></span>

<span data-ttu-id="e6a6d-144">En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un grupo [**mediante**](windowsribbon-element-group.md) la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition de**](windowsribbon-element-sizedefinition.md) la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="e6a6d-145">El [**manifiesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, los **elementos Scale** se especifican para influir en el comportamiento de conserción, en orden descendente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="e6a6d-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="e6a6d-146">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e6a6d-146">Element information</span></span>



* <span data-ttu-id="e6a6d-147">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6a6d-147">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e6a6d-148">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="e6a6d-148">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="e6a6d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6a6d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a6d-150">Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="e6a6d-150">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






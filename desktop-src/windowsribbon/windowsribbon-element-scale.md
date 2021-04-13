---
title: Elemento Scale
description: Representa el tamaño y la preferencia de diseño de un grupo de controles a través de un par de grupo, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Cinta de opciones de ventanas de elementos de escala
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3832d36a48b330b036fa287499f9db387335f87b
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420198"
---
# <a name="scale-element"></a><span data-ttu-id="a35ab-104">Elemento Scale</span><span class="sxs-lookup"><span data-stu-id="a35ab-104">Scale element</span></span>

<span data-ttu-id="a35ab-105">Representa el tamaño y la preferencia de diseño de un [**Grupo**](windowsribbon-element-group.md) de controles a través de un par {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="a35ab-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="a35ab-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a35ab-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="a35ab-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a35ab-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a35ab-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a35ab-108">Attribute</span></span></th>
<th><span data-ttu-id="a35ab-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a35ab-109">Type</span></span></th>
<th><span data-ttu-id="a35ab-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a35ab-110">Required</span></span></th>
<th><span data-ttu-id="a35ab-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35ab-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a35ab-112"><strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="a35ab-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="a35ab-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="a35ab-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a35ab-114">Sí</span><span class="sxs-lookup"><span data-stu-id="a35ab-114">Yes</span></span><br/></td>
<td><span data-ttu-id="a35ab-115">Debe corresponder a un <a href="windowsribbon-element-group.md"><strong>Grupo</strong></a> <em>CommandName</em>existente.</span><span class="sxs-lookup"><span data-stu-id="a35ab-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="a35ab-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="a35ab-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a35ab-117">Una cadena o un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a35ab-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="a35ab-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a35ab-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a35ab-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a35ab-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35ab-120"><strong>Tamaño</strong></span><span class="sxs-lookup"><span data-stu-id="a35ab-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="a35ab-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="a35ab-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="a35ab-122">Sí</span><span class="sxs-lookup"><span data-stu-id="a35ab-122">Yes</span></span><br/></td>
<td><span data-ttu-id="a35ab-123">Este valor debe corresponder a uno de los tamaños válidos para el atributo <em>SizeDefinition</em> del <a href="windowsribbon-element-group.md"><strong>Grupo</strong></a> de controles asociado especificado en <em>Group</em>.</span><span class="sxs-lookup"><span data-stu-id="a35ab-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="a35ab-124">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a35ab-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="a35ab-125">
<dt><span></span><span></span><strong></strong> Emergente</span><span class="sxs-lookup"><span data-stu-id="a35ab-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="a35ab-126">Diseño de control idéntico al que se <code>Large</code> hospeda en un panel desplegable o un elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="a35ab-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="a35ab-127"><dt><span></span><span></span><strong></strong> Pequeño</span><span class="sxs-lookup"><span data-stu-id="a35ab-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="a35ab-128">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeña.</span><span class="sxs-lookup"><span data-stu-id="a35ab-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="a35ab-129"><dt><span></span><span></span><strong></strong> Medio</span><span class="sxs-lookup"><span data-stu-id="a35ab-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="a35ab-130">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> mediana.</span><span class="sxs-lookup"><span data-stu-id="a35ab-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="a35ab-131"><dt><span></span><span></span><strong></strong> Amplíe</span><span class="sxs-lookup"><span data-stu-id="a35ab-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="a35ab-132">Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.</span><span class="sxs-lookup"><span data-stu-id="a35ab-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a35ab-133">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a35ab-133">Child elements</span></span>

<span data-ttu-id="a35ab-134">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a35ab-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a35ab-135">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a35ab-135">Parent elements</span></span>



| <span data-ttu-id="a35ab-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="a35ab-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a35ab-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="a35ab-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="a35ab-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="a35ab-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a35ab-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a35ab-139">Remarks</span></span>

<span data-ttu-id="a35ab-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a35ab-140">Optional.</span></span>

<span data-ttu-id="a35ab-141">Puede producirse una o varias veces para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) o [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span><span class="sxs-lookup"><span data-stu-id="a35ab-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="a35ab-142">Cada par de atributo (*Grupo*, *tamaño*) debe ser único.</span><span class="sxs-lookup"><span data-stu-id="a35ab-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="a35ab-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a35ab-143">Examples</span></span>

<span data-ttu-id="a35ab-144">En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un [**Grupo**](windowsribbon-element-group.md) mediante la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de la cinta.</span><span class="sxs-lookup"><span data-stu-id="a35ab-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="a35ab-145">El manifiesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de **escala** se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="a35ab-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a35ab-146">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a35ab-146">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a35ab-147">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a35ab-147">Minimum supported system</span></span><br/> | <span data-ttu-id="a35ab-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a35ab-148">Windows 7</span></span> |
| <span data-ttu-id="a35ab-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a35ab-149">Can be empty</span></span>                        | <span data-ttu-id="a35ab-150">Sí</span><span class="sxs-lookup"><span data-stu-id="a35ab-150">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="a35ab-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a35ab-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35ab-152">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="a35ab-152">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






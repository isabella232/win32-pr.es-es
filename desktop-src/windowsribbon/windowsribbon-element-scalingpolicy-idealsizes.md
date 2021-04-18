---
title: Propiedad ScalingPolicy. IdealSizes
description: Representa un contenedor de especificaciones de escala para la plantilla de SizeDefinition preferida, en función del tamaño de la cinta de opciones.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- ScalingPolicy. IdealSizes (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705167"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="a2d2c-104">Propiedad ScalingPolicy. IdealSizes</span><span class="sxs-lookup"><span data-stu-id="a2d2c-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="a2d2c-105">Representa un contenedor de especificaciones de escala para la plantilla de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferida, en función del tamaño de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="a2d2c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a2d2c-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="a2d2c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2d2c-107">Attributes</span></span>

<span data-ttu-id="a2d2c-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a2d2c-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a2d2c-109">Child elements</span></span>



| <span data-ttu-id="a2d2c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a2d2c-110">Element</span></span>                                                 | <span data-ttu-id="a2d2c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2d2c-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a2d2c-112">**Escala**</span><span class="sxs-lookup"><span data-stu-id="a2d2c-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="a2d2c-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a2d2c-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a2d2c-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a2d2c-114">Parent elements</span></span>



| <span data-ttu-id="a2d2c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="a2d2c-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="a2d2c-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="a2d2c-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a2d2c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2d2c-117">Remarks</span></span>

<span data-ttu-id="a2d2c-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-118">Optional.</span></span>

<span data-ttu-id="a2d2c-119">Puede producirse al menos una vez para cada [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a2d2c-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="a2d2c-120">Si se define **ScalingPolicy. IdealSizes** , debe haber una entrada de [**escala**](windowsribbon-element-scale.md) para cada elemento de [**Grupo**](windowsribbon-element-group.md) de un elemento de [**ficha**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="a2d2c-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="a2d2c-121">**ScalingPolicy. IdealSizes** son los diseños de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferidos para un [**Grupo**](windowsribbon-element-group.md) de controles.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="a2d2c-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a2d2c-122">Examples</span></span>

<span data-ttu-id="a2d2c-123">En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un [**Grupo**](windowsribbon-element-group.md) mediante la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) de la cinta.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="a2d2c-124">El manifiesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de [**escala**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="a2d2c-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="a2d2c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2d2c-125">Requirements</span></span>



| <span data-ttu-id="a2d2c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2d2c-126">Requirement</span></span> | <span data-ttu-id="a2d2c-127">Value</span><span class="sxs-lookup"><span data-stu-id="a2d2c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a2d2c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d2c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d2c-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2d2c-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a2d2c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2d2c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d2c-131">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2d2c-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2d2c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2d2c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d2c-133">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="a2d2c-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






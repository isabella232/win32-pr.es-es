---
title: Elemento ScalingPolicy
description: Representa un contenedor para las especificaciones de escalado.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Cinta de opciones de Windows del elemento ScalingPolicy
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444996"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="ffa97-104">Elemento ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="ffa97-104">ScalingPolicy element</span></span>

<span data-ttu-id="ffa97-105">Representa un contenedor para las especificaciones de escalado.</span><span class="sxs-lookup"><span data-stu-id="ffa97-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="ffa97-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ffa97-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="ffa97-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffa97-107">Attributes</span></span>

<span data-ttu-id="ffa97-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ffa97-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ffa97-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ffa97-109">Child elements</span></span>



| <span data-ttu-id="ffa97-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffa97-110">Element</span></span>                                                                                       | <span data-ttu-id="ffa97-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffa97-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="ffa97-112">**Escala**</span><span class="sxs-lookup"><span data-stu-id="ffa97-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="ffa97-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="ffa97-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="ffa97-114">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="ffa97-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="ffa97-115">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="ffa97-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="ffa97-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ffa97-116">Parent elements</span></span>



| <span data-ttu-id="ffa97-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffa97-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ffa97-118">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="ffa97-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ffa97-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffa97-119">Remarks</span></span>

<span data-ttu-id="ffa97-120">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ffa97-120">Required.</span></span>

<span data-ttu-id="ffa97-121">Debe producirse una vez para [**cada Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ffa97-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="ffa97-122">El **elemento ScalingPolicy** contiene un manifiesto de declaraciones [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) y [**Scale**](windowsribbon-element-scale.md) que especifican preferencias de diseño adaptable para uno o varios elementos [**Group**](windowsribbon-element-group.md) cuando se cambia el tamaño de la cinta.</span><span class="sxs-lookup"><span data-stu-id="ffa97-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="ffa97-123">La lista de [**declaraciones de**](windowsribbon-element-scale.md) escala debe estar en orden descendente de tamaños válidos (grande, mediano, pequeño, emergente) para el [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) asociado al [**elemento Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="ffa97-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ffa97-124">Se recomienda encarecidamente que se especifiquen los detalles adecuados de la directiva de escalado para que una cinta de opciones pueda representarse sin barras de desplazamiento al cambiar el tamaño a un ancho de 300 píxeles a 96 puntos por pulgada (ppp).</span><span class="sxs-lookup"><span data-stu-id="ffa97-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="ffa97-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ffa97-125">Examples</span></span>

<span data-ttu-id="ffa97-126">En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un grupo [**a**](windowsribbon-element-group.md) través de la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition de**](windowsribbon-element-sizedefinition.md) la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="ffa97-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="ffa97-127">El **manifiesto ScalingPolicy** de este ejemplo especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, los [**elementos Scale**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de conserción, en orden descendente de tamaño, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="ffa97-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ffa97-128">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ffa97-128">Element information</span></span>

- <span data-ttu-id="ffa97-129">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffa97-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="ffa97-130">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="ffa97-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ffa97-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffa97-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa97-132">Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="ffa97-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






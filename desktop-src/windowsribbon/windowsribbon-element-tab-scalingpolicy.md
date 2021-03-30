---
title: Propiedad Tab. ScalingPolicy
description: Representa un contenedor para las especificaciones de escala de tabulación.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- TAB. ScalingPolicy (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492497"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="c0a77-104">Propiedad Tab. ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="c0a77-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="c0a77-105">Representa un contenedor para las especificaciones de escala de [tabulación](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a77-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="c0a77-106">Uso</span><span class="sxs-lookup"><span data-stu-id="c0a77-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="c0a77-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0a77-107">Attributes</span></span>

<span data-ttu-id="c0a77-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="c0a77-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c0a77-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0a77-109">Child elements</span></span>



| <span data-ttu-id="c0a77-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0a77-110">Element</span></span>                                                                 | <span data-ttu-id="c0a77-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a77-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="c0a77-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="c0a77-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="c0a77-113">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="c0a77-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c0a77-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c0a77-114">Parent elements</span></span>



| <span data-ttu-id="c0a77-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0a77-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="c0a77-116">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="c0a77-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c0a77-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0a77-117">Remarks</span></span>

<span data-ttu-id="c0a77-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0a77-118">Optional.</span></span>

<span data-ttu-id="c0a77-119">Puede producirse al menos una vez para cada [**pestaña**](windowsribbon-element-tab.md).</span><span class="sxs-lookup"><span data-stu-id="c0a77-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="c0a77-120">Las especificaciones de escalado describen el tamaño y el comportamiento de diseño de los controles en una [pestaña](windowsribbon-controls-tab.md) cuando se cambia el tamaño de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="c0a77-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="c0a77-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c0a77-121">Examples</span></span>

<span data-ttu-id="c0a77-122">En el ejemplo de código siguiente se muestra un manifiesto de [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica una preferencia [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de cuatro grupos de controles en una pestaña **Inicio** . Además, los elementos de [**escala**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de contracción, en orden de tamaño descendente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="c0a77-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c0a77-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a77-123">Requirements</span></span>



| <span data-ttu-id="c0a77-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a77-124">Requirement</span></span> | <span data-ttu-id="c0a77-125">Value</span><span class="sxs-lookup"><span data-stu-id="c0a77-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c0a77-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a77-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a77-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a77-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c0a77-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a77-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a77-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a77-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0a77-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0a77-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a77-131">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="c0a77-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






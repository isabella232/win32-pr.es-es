---
title: Propiedad Ribbon. SizeDefinitions
description: Representa un contenedor para plantillas de diseño personalizado de controles de la cinta de opciones.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Ribbon. SizeDefinitions (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078954"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="90a2e-104">Propiedad Ribbon. SizeDefinitions</span><span class="sxs-lookup"><span data-stu-id="90a2e-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="90a2e-105">Representa un contenedor para plantillas de diseño personalizado de controles de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="90a2e-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="90a2e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="90a2e-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="90a2e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="90a2e-107">Attributes</span></span>

<span data-ttu-id="90a2e-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="90a2e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="90a2e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90a2e-109">Child elements</span></span>



| <span data-ttu-id="90a2e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="90a2e-110">Element</span></span>                                                                   | <span data-ttu-id="90a2e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a2e-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="90a2e-112">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="90a2e-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="90a2e-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="90a2e-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="90a2e-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="90a2e-114">Parent elements</span></span>



| <span data-ttu-id="90a2e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="90a2e-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="90a2e-116">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="90a2e-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="90a2e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90a2e-117">Remarks</span></span>

<span data-ttu-id="90a2e-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90a2e-118">Optional.</span></span>

<span data-ttu-id="90a2e-119">Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="90a2e-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="90a2e-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="90a2e-120">Examples</span></span>

<span data-ttu-id="90a2e-121">En el ejemplo de código siguiente se muestra una plantilla personalizada básica.</span><span class="sxs-lookup"><span data-stu-id="90a2e-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="90a2e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a2e-122">Requirements</span></span>



| <span data-ttu-id="90a2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a2e-123">Requirement</span></span> | <span data-ttu-id="90a2e-124">Value</span><span class="sxs-lookup"><span data-stu-id="90a2e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="90a2e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90a2e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="90a2e-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="90a2e-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="90a2e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90a2e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="90a2e-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="90a2e-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90a2e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="90a2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a2e-130">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="90a2e-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






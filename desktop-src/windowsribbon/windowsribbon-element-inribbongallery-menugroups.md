---
title: Propiedad InRibbonGallery. MenuGroups
description: Representa un contenedor para el conjunto de elementos de menú desplegable de un control Galería de In-Ribbon.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- InRibbonGallery. MenuGroups (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079432"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="dac20-104">Propiedad InRibbonGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="dac20-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="dac20-105">Representa un contenedor para el conjunto de elementos de menú desplegable de un control [de la galería de la cinta de](windowsribbon-controls-inribbongallery.md) opciones.</span><span class="sxs-lookup"><span data-stu-id="dac20-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="dac20-106">Uso</span><span class="sxs-lookup"><span data-stu-id="dac20-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="dac20-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="dac20-107">Attributes</span></span>

<span data-ttu-id="dac20-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="dac20-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="dac20-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dac20-109">Child elements</span></span>



| <span data-ttu-id="dac20-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="dac20-110">Element</span></span>                                                         | <span data-ttu-id="dac20-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac20-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="dac20-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="dac20-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="dac20-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="dac20-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="dac20-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="dac20-114">Parent elements</span></span>



| <span data-ttu-id="dac20-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="dac20-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="dac20-116">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="dac20-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="dac20-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dac20-117">Remarks</span></span>

<span data-ttu-id="dac20-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dac20-118">Optional.</span></span>

<span data-ttu-id="dac20-119">Puede aparecer como máximo una vez por cada elemento [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="dac20-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="dac20-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dac20-120">Examples</span></span>

<span data-ttu-id="dac20-121">En el ejemplo siguiente se muestra el marcado básico de un control [de la galería de la cinta de](windowsribbon-controls-inribbongallery.md) opciones.</span><span class="sxs-lookup"><span data-stu-id="dac20-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="dac20-122">En esta sección de código se muestra la declaración de control **InRibbonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="dac20-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="dac20-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac20-123">Requirements</span></span>



| <span data-ttu-id="dac20-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac20-124">Requirement</span></span> | <span data-ttu-id="dac20-125">Value</span><span class="sxs-lookup"><span data-stu-id="dac20-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="dac20-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac20-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dac20-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac20-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="dac20-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dac20-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dac20-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dac20-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dac20-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dac20-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac20-131">Control de la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="dac20-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="dac20-132">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="dac20-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="dac20-133">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="dac20-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 






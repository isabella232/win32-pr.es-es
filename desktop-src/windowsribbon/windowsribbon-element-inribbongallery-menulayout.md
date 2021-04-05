---
title: Propiedad InRibbonGallery. MenuLayout
description: Representa un contenedor para los diseños del menú desplegable de la galería de In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- InRibbonGallery. MenuLayout (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078956"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="f7e3e-104">Propiedad InRibbonGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="f7e3e-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="f7e3e-105">Representa un contenedor para los diseños de menú desplegable [de la galería de la cinta de](windowsribbon-controls-inribbongallery.md) opciones.</span><span class="sxs-lookup"><span data-stu-id="f7e3e-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="f7e3e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f7e3e-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="f7e3e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7e3e-107">Attributes</span></span>

<span data-ttu-id="f7e3e-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="f7e3e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f7e3e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7e3e-109">Child elements</span></span>



| <span data-ttu-id="f7e3e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7e3e-110">Element</span></span>                                                                           | <span data-ttu-id="f7e3e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7e3e-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="f7e3e-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="f7e3e-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="f7e3e-113">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="f7e3e-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="f7e3e-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="f7e3e-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="f7e3e-115">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="f7e3e-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f7e3e-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f7e3e-116">Parent elements</span></span>



| <span data-ttu-id="f7e3e-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7e3e-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f7e3e-118">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="f7e3e-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f7e3e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7e3e-119">Remarks</span></span>

<span data-ttu-id="f7e3e-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f7e3e-120">Optional.</span></span>

<span data-ttu-id="f7e3e-121">Puede aparecer como máximo una vez por cada elemento [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e3e-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="f7e3e-122">Se permite un máximo de un elemento secundario ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="f7e3e-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f7e3e-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f7e3e-123">Examples</span></span>

<span data-ttu-id="f7e3e-124">En el ejemplo siguiente se muestra el marcado básico de la [Galería de la cinta de](windowsribbon-controls-inribbongallery.md)opciones.</span><span class="sxs-lookup"><span data-stu-id="f7e3e-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="f7e3e-125">En esta sección de código se muestra la declaración de control **InRibbonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="f7e3e-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f7e3e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7e3e-126">Requirements</span></span>



| <span data-ttu-id="f7e3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7e3e-127">Requirement</span></span> | <span data-ttu-id="f7e3e-128">Value</span><span class="sxs-lookup"><span data-stu-id="f7e3e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f7e3e-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7e3e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e3e-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7e3e-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f7e3e-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7e3e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e3e-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7e3e-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7e3e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7e3e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e3e-134">Control de la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f7e3e-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="f7e3e-135">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="f7e3e-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 






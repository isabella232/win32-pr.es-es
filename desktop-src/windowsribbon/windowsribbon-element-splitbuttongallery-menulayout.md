---
title: Propiedad SplitButtonGallery. MenuLayout
description: Representa un contenedor para los diseños de menú desplegable de la galería de botones de expansión.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- SplitButtonGallery. MenuLayout (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705121"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="eb204-104">Propiedad SplitButtonGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="eb204-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="eb204-105">Representa un contenedor para los diseños de menú desplegable de la [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="eb204-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="eb204-106">Uso</span><span class="sxs-lookup"><span data-stu-id="eb204-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="eb204-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb204-107">Attributes</span></span>

<span data-ttu-id="eb204-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="eb204-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eb204-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb204-109">Child elements</span></span>



| <span data-ttu-id="eb204-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb204-110">Element</span></span>                                                                           | <span data-ttu-id="eb204-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb204-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="eb204-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="eb204-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="eb204-113">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="eb204-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="eb204-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="eb204-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="eb204-115">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="eb204-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="eb204-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="eb204-116">Parent elements</span></span>



| <span data-ttu-id="eb204-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="eb204-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="eb204-118">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="eb204-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="eb204-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb204-119">Remarks</span></span>

<span data-ttu-id="eb204-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb204-120">Optional.</span></span>

<span data-ttu-id="eb204-121">Puede aparecer como máximo una vez por cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="eb204-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="eb204-122">Se permite un máximo de un elemento secundario ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="eb204-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="eb204-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eb204-123">Examples</span></span>

<span data-ttu-id="eb204-124">En el ejemplo siguiente se muestra el marcado básico de la [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="eb204-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="eb204-125">En esta sección de código se muestra la declaración de control **SplitButtonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="eb204-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="eb204-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb204-126">Requirements</span></span>



| <span data-ttu-id="eb204-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb204-127">Requirement</span></span> | <span data-ttu-id="eb204-128">Value</span><span class="sxs-lookup"><span data-stu-id="eb204-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="eb204-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb204-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eb204-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb204-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="eb204-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb204-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eb204-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb204-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb204-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb204-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb204-134">Control Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="eb204-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="eb204-135">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="eb204-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 






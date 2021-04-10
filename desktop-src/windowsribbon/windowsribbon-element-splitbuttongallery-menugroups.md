---
title: Propiedad SplitButtonGallery. MenuGroups
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- SplitButtonGallery. MenuGroups (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150273"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="97a9b-104">Propiedad SplitButtonGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="97a9b-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="97a9b-105">Representa un contenedor para un conjunto de elementos de menú desplegable en un control [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="97a9b-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="97a9b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="97a9b-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="97a9b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="97a9b-107">Attributes</span></span>

<span data-ttu-id="97a9b-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="97a9b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="97a9b-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="97a9b-109">Child elements</span></span>



| <span data-ttu-id="97a9b-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="97a9b-110">Element</span></span>                                                         | <span data-ttu-id="97a9b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="97a9b-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="97a9b-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="97a9b-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="97a9b-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="97a9b-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="97a9b-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="97a9b-114">Parent elements</span></span>



| <span data-ttu-id="97a9b-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="97a9b-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="97a9b-116">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="97a9b-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="97a9b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97a9b-117">Remarks</span></span>

<span data-ttu-id="97a9b-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="97a9b-118">Required.</span></span>

<span data-ttu-id="97a9b-119">Debe aparecer exactamente una vez para cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="97a9b-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="97a9b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="97a9b-120">Examples</span></span>

<span data-ttu-id="97a9b-121">En el ejemplo siguiente se muestra el marcado básico para el elemento **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="97a9b-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="97a9b-122">En esta sección de código se muestra la declaración de control **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="97a9b-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="97a9b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97a9b-123">Requirements</span></span>



| <span data-ttu-id="97a9b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97a9b-124">Requirement</span></span> | <span data-ttu-id="97a9b-125">Value</span><span class="sxs-lookup"><span data-stu-id="97a9b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="97a9b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97a9b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97a9b-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="97a9b-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="97a9b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97a9b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97a9b-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="97a9b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97a9b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="97a9b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a9b-131">Control Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="97a9b-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="97a9b-132">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="97a9b-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 






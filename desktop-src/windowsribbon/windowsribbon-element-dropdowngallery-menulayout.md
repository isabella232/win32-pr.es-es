---
title: Propiedad DropDownGallery. MenuLayout
description: Representa un contenedor para los diseños del menú desplegable DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- DropDownGallery. MenuLayout (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714619"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="ebef5-104">Propiedad DropDownGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="ebef5-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="ebef5-105">Representa un contenedor para los diseños del menú desplegable [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ebef5-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="ebef5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ebef5-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="ebef5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebef5-107">Attributes</span></span>

<span data-ttu-id="ebef5-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ebef5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ebef5-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebef5-109">Child elements</span></span>



| <span data-ttu-id="ebef5-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebef5-110">Element</span></span>                                                                           | <span data-ttu-id="ebef5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebef5-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ebef5-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ebef5-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="ebef5-113">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="ebef5-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="ebef5-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ebef5-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="ebef5-115">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="ebef5-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ebef5-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ebef5-116">Parent elements</span></span>



| <span data-ttu-id="ebef5-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebef5-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ebef5-118">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="ebef5-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ebef5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebef5-119">Remarks</span></span>

<span data-ttu-id="ebef5-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ebef5-120">Optional.</span></span>

<span data-ttu-id="ebef5-121">Puede aparecer como máximo una vez por cada elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ebef5-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ebef5-122">Se permite un máximo de un elemento secundario ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="ebef5-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ebef5-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ebef5-123">Examples</span></span>

<span data-ttu-id="ebef5-124">En el ejemplo siguiente se muestra el marcado básico para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="ebef5-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="ebef5-125">En esta sección de código se muestra la declaración de control **DropDownGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="ebef5-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="ebef5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebef5-126">Requirements</span></span>



| <span data-ttu-id="ebef5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebef5-127">Requirement</span></span> | <span data-ttu-id="ebef5-128">Value</span><span class="sxs-lookup"><span data-stu-id="ebef5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ebef5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebef5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ebef5-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebef5-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ebef5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebef5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ebef5-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebef5-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebef5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebef5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebef5-134">**Control Galería desplegable**</span><span class="sxs-lookup"><span data-stu-id="ebef5-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="ebef5-135">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="ebef5-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 






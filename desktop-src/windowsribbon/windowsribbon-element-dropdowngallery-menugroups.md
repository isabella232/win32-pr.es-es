---
title: Propiedad DropDownGallery. MenuGroups
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control de la galería de Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery. MenuGroups (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720230"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="3bbdb-104">Propiedad DropDownGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="3bbdb-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="3bbdb-105">Representa un contenedor para un conjunto de elementos de menú desplegable en un control de la [Galería](windowsribbon-controls-dropdowngallery.md) desplegable.</span><span class="sxs-lookup"><span data-stu-id="3bbdb-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="3bbdb-106">Uso</span><span class="sxs-lookup"><span data-stu-id="3bbdb-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="3bbdb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3bbdb-107">Attributes</span></span>

<span data-ttu-id="3bbdb-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="3bbdb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3bbdb-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3bbdb-109">Child elements</span></span>



| <span data-ttu-id="3bbdb-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3bbdb-110">Element</span></span>                                                         | <span data-ttu-id="3bbdb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bbdb-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="3bbdb-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="3bbdb-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="3bbdb-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="3bbdb-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3bbdb-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3bbdb-114">Parent elements</span></span>



| <span data-ttu-id="3bbdb-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="3bbdb-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3bbdb-116">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="3bbdb-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3bbdb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bbdb-117">Remarks</span></span>

<span data-ttu-id="3bbdb-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3bbdb-118">Required.</span></span>

<span data-ttu-id="3bbdb-119">Debe aparecer exactamente una vez para cada elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbdb-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3bbdb-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3bbdb-120">Examples</span></span>

<span data-ttu-id="3bbdb-121">En el ejemplo siguiente se muestra el marcado básico para el elemento **DropDownGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="3bbdb-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="3bbdb-122">En esta sección de código se muestra la declaración de control **DropDownGallery. MenuGroups** en un espacio de comandos de la [Galería](windowsribbon-controls-dropdowngallery.md) desplegable.</span><span class="sxs-lookup"><span data-stu-id="3bbdb-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3bbdb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bbdb-123">Requirements</span></span>



| <span data-ttu-id="3bbdb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bbdb-124">Requirement</span></span> | <span data-ttu-id="3bbdb-125">Value</span><span class="sxs-lookup"><span data-stu-id="3bbdb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3bbdb-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bbdb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbdb-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bbdb-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3bbdb-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bbdb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbdb-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bbdb-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bbdb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bbdb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbdb-131">**Control Galería desplegable**</span><span class="sxs-lookup"><span data-stu-id="3bbdb-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="3bbdb-132">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="3bbdb-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 






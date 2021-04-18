---
title: Propiedad Ribbon. ApplicationMenu
description: Representa el menú de la aplicación. | Propiedad Ribbon. ApplicationMenu
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Ribbon. ApplicationMenu (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717531"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="80412-105">Propiedad Ribbon. ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="80412-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="80412-106">Representa el menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80412-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="80412-107">Uso</span><span class="sxs-lookup"><span data-stu-id="80412-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="80412-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="80412-108">Attributes</span></span>

<span data-ttu-id="80412-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="80412-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="80412-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="80412-110">Child elements</span></span>



| <span data-ttu-id="80412-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="80412-111">Element</span></span>                                                                     | <span data-ttu-id="80412-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="80412-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="80412-113">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="80412-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="80412-114">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="80412-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="80412-115">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="80412-115">Parent elements</span></span>



| <span data-ttu-id="80412-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="80412-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="80412-117">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="80412-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="80412-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80412-118">Remarks</span></span>

<span data-ttu-id="80412-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="80412-119">Required.</span></span>

<span data-ttu-id="80412-120">Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="80412-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="80412-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="80412-121">Examples</span></span>

<span data-ttu-id="80412-122">En el ejemplo siguiente se muestra el marcado básico para el elemento **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="80412-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="80412-123">En esta sección de código se muestra la declaración de control **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="80412-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="80412-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80412-124">Requirements</span></span>



| <span data-ttu-id="80412-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80412-125">Requirement</span></span> | <span data-ttu-id="80412-126">Value</span><span class="sxs-lookup"><span data-stu-id="80412-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="80412-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80412-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80412-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="80412-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="80412-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80412-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80412-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80412-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






---
title: Ribbon. Tabs (propiedad)
description: Representa un contenedor para todas las pestañas principales en una cinta de opciones.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Ribbon. Tabs (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489310"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="13183-104">Ribbon. Tabs (propiedad)</span><span class="sxs-lookup"><span data-stu-id="13183-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="13183-105">Representa un contenedor para todas las pestañas principales en una cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="13183-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="13183-106">Uso</span><span class="sxs-lookup"><span data-stu-id="13183-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="13183-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="13183-107">Attributes</span></span>

<span data-ttu-id="13183-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="13183-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="13183-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13183-109">Child elements</span></span>



| <span data-ttu-id="13183-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="13183-110">Element</span></span>                                             | <span data-ttu-id="13183-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="13183-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="13183-112">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="13183-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="13183-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="13183-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="13183-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="13183-114">Parent elements</span></span>



| <span data-ttu-id="13183-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="13183-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="13183-116">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="13183-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="13183-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13183-117">Remarks</span></span>

<span data-ttu-id="13183-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13183-118">Required.</span></span>

<span data-ttu-id="13183-119">Puede producirse una o varias veces para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="13183-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="13183-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="13183-120">Examples</span></span>

<span data-ttu-id="13183-121">En el ejemplo siguiente se muestra el marcado básico de un elemento **Ribbon. tabs** con una declaración de [**pestañas**](windowsribbon-element-tab.md) de **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="13183-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a><span data-ttu-id="13183-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13183-122">Requirements</span></span>



| <span data-ttu-id="13183-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13183-123">Requirement</span></span> | <span data-ttu-id="13183-124">Value</span><span class="sxs-lookup"><span data-stu-id="13183-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="13183-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13183-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13183-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="13183-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="13183-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13183-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13183-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="13183-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13183-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="13183-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13183-130">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="13183-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 






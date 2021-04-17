---
title: Application. views (propiedad)
description: Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la cinta de opciones y el ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Propiedad Application. views (cinta) de Windows
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705145"
---
# <a name="applicationviews-property"></a><span data-ttu-id="f50ca-104">Application. views (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f50ca-104">Application.Views property</span></span>

<span data-ttu-id="f50ca-105">Representa un contenedor para cada vista del marco de la cinta de opciones, específicamente la [**cinta**](windowsribbon-element-ribbon.md) de opciones y el [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="f50ca-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="f50ca-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f50ca-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="f50ca-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f50ca-107">Attributes</span></span>

<span data-ttu-id="f50ca-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="f50ca-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f50ca-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f50ca-109">Child elements</span></span>



| <span data-ttu-id="f50ca-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f50ca-110">Element</span></span>                                                               | <span data-ttu-id="f50ca-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f50ca-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f50ca-112">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="f50ca-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="f50ca-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="f50ca-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f50ca-114">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="f50ca-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="f50ca-115">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="f50ca-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="f50ca-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f50ca-116">Parent elements</span></span>



| <span data-ttu-id="f50ca-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f50ca-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="f50ca-118">**Aplicación**</span><span class="sxs-lookup"><span data-stu-id="f50ca-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f50ca-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f50ca-119">Remarks</span></span>

<span data-ttu-id="f50ca-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f50ca-120">Required.</span></span>

<span data-ttu-id="f50ca-121">Debe aparecer exactamente una vez para cada elemento de la [**aplicación**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="f50ca-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="f50ca-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f50ca-122">Examples</span></span>

<span data-ttu-id="f50ca-123">En el ejemplo siguiente se muestra un elemento **Application. views** que contiene un manifiesto de controles de la cinta de opciones, cada uno con una referencia a un comando declarado en el elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="f50ca-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="f50ca-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f50ca-124">Requirements</span></span>



| <span data-ttu-id="f50ca-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f50ca-125">Requirement</span></span> | <span data-ttu-id="f50ca-126">Value</span><span class="sxs-lookup"><span data-stu-id="f50ca-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f50ca-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f50ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f50ca-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f50ca-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f50ca-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f50ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f50ca-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f50ca-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f50ca-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f50ca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50ca-132">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="f50ca-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 






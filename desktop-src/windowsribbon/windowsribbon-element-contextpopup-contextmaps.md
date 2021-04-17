---
title: Propiedad ContextPopup. ContextMaps
description: Representa un contenedor para los elementos ContextMap.
ms.assetid: 06dfd4ba-a1d8-48bb-b185-d265e007a820
keywords:
- ContextPopup. ContextMaps (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ContextPopup.ContextMaps
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034381c4af840219ff1d6dd4d7a73aa34f528915
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705168"
---
# <a name="contextpopupcontextmaps-property"></a><span data-ttu-id="e3212-104">Propiedad ContextPopup. ContextMaps</span><span class="sxs-lookup"><span data-stu-id="e3212-104">ContextPopup.ContextMaps property</span></span>

<span data-ttu-id="e3212-105">Representa un contenedor para los elementos [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="e3212-105">Represents a container for [**ContextMap**](windowsribbon-element-contextmap.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="e3212-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e3212-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMaps>
  child elements
</ContextPopup.ContextMaps>
```

## <a name="attributes"></a><span data-ttu-id="e3212-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3212-107">Attributes</span></span>

<span data-ttu-id="e3212-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="e3212-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e3212-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3212-109">Child elements</span></span>



| <span data-ttu-id="e3212-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e3212-110">Element</span></span>                                                           | <span data-ttu-id="e3212-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3212-111">Description</span></span>                                        |
|-------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e3212-112">**ContextMap**</span><span class="sxs-lookup"><span data-stu-id="e3212-112">**ContextMap**</span></span>](windowsribbon-element-contextmap.md)<br/> | <span data-ttu-id="e3212-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="e3212-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e3212-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e3212-114">Parent elements</span></span>



| <span data-ttu-id="e3212-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e3212-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="e3212-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="e3212-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e3212-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3212-117">Remarks</span></span>

<span data-ttu-id="e3212-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e3212-118">Optional.</span></span>

<span data-ttu-id="e3212-119">Puede producirse al menos una vez para cada [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="e3212-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e3212-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3212-120">Examples</span></span>

<span data-ttu-id="e3212-121">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="e3212-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="e3212-122">En esta sección de código se muestra una declaración de control **ContextPopup. ContextMaps** .</span><span class="sxs-lookup"><span data-stu-id="e3212-122">This section of code shows a **ContextPopup.ContextMaps** control declaration.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="requirements"></a><span data-ttu-id="e3212-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3212-123">Requirements</span></span>



| <span data-ttu-id="e3212-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3212-124">Requirement</span></span> | <span data-ttu-id="e3212-125">Value</span><span class="sxs-lookup"><span data-stu-id="e3212-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e3212-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3212-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e3212-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3212-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e3212-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3212-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e3212-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3212-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3212-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3212-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3212-131">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="e3212-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






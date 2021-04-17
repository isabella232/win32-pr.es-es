---
title: Propiedad ContextPopup. ContextMenus
description: Representa un contenedor de elementos ContextMenu.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- ContextPopup. ContextMenus (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705169"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="a8e5e-104">Propiedad ContextPopup. ContextMenus</span><span class="sxs-lookup"><span data-stu-id="a8e5e-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="a8e5e-105">Representa un contenedor de elementos [**ContextMenu**](windowsribbon-element-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e5e-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="a8e5e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a8e5e-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="a8e5e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8e5e-107">Attributes</span></span>

<span data-ttu-id="a8e5e-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="a8e5e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8e5e-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8e5e-109">Child elements</span></span>



| <span data-ttu-id="a8e5e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8e5e-110">Element</span></span>                                                             | <span data-ttu-id="a8e5e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8e5e-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a8e5e-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="a8e5e-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="a8e5e-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="a8e5e-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a8e5e-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a8e5e-114">Parent elements</span></span>



| <span data-ttu-id="a8e5e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8e5e-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="a8e5e-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="a8e5e-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a8e5e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8e5e-117">Remarks</span></span>

<span data-ttu-id="a8e5e-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e5e-118">Optional.</span></span>

<span data-ttu-id="a8e5e-119">Puede producirse al menos una vez para cada [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="a8e5e-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8e5e-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8e5e-120">Examples</span></span>

<span data-ttu-id="a8e5e-121">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e5e-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="a8e5e-122">En esta sección de código se muestra una declaración de control **ContextPopup. ContextMenus** .</span><span class="sxs-lookup"><span data-stu-id="a8e5e-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a8e5e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8e5e-123">Requirements</span></span>



| <span data-ttu-id="a8e5e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e5e-124">Requirement</span></span> | <span data-ttu-id="a8e5e-125">Value</span><span class="sxs-lookup"><span data-stu-id="a8e5e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a8e5e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8e5e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e5e-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8e5e-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a8e5e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8e5e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e5e-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8e5e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8e5e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8e5e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e5e-131">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="a8e5e-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






---
title: Propiedad ContextPopup. MiniToolbars
description: Representa un contenedor para los elementos MiniToolbar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- ContextPopup. MiniToolbars (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492502"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="93db4-104">Propiedad ContextPopup. MiniToolbars</span><span class="sxs-lookup"><span data-stu-id="93db4-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="93db4-105">Representa un contenedor para los elementos [**MiniToolbar**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="93db4-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="93db4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="93db4-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="93db4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="93db4-107">Attributes</span></span>

<span data-ttu-id="93db4-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="93db4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="93db4-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93db4-109">Child elements</span></span>



| <span data-ttu-id="93db4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="93db4-110">Element</span></span>                                                             | <span data-ttu-id="93db4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="93db4-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="93db4-112">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="93db4-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="93db4-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="93db4-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="93db4-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="93db4-114">Parent elements</span></span>



| <span data-ttu-id="93db4-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="93db4-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="93db4-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="93db4-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="93db4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93db4-117">Remarks</span></span>

<span data-ttu-id="93db4-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="93db4-118">Optional.</span></span>

<span data-ttu-id="93db4-119">Puede producirse al menos una vez para cada [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="93db4-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="93db4-120">Dado que los controles de [**MiniToolbar**](windowsribbon-element-minitoolbar.md) no son accesibles desde el teclado, los comandos que exponen deben estar disponibles en cualquier parte de la interfaz de usuario de la cinta.</span><span class="sxs-lookup"><span data-stu-id="93db4-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="93db4-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="93db4-121">Examples</span></span>

<span data-ttu-id="93db4-122">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="93db4-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="93db4-123">En esta sección de código se muestra la declaración de control **ContextPopup. MiniToolbars** .</span><span class="sxs-lookup"><span data-stu-id="93db4-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="93db4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93db4-124">Requirements</span></span>



| <span data-ttu-id="93db4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93db4-125">Requirement</span></span> | <span data-ttu-id="93db4-126">Value</span><span class="sxs-lookup"><span data-stu-id="93db4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="93db4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93db4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="93db4-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="93db4-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="93db4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93db4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="93db4-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="93db4-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93db4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="93db4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93db4-132">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="93db4-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






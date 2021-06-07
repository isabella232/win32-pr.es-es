---
title: Elemento ContextPopup
description: Representa el control Context Popup en la vista ContextPopup.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Elemento ContextPopup de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f779b0196d14fb42246c2a10d476352d835b6cf8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443475"
---
# <a name="contextpopup-element"></a><span data-ttu-id="231b0-104">Elemento ContextPopup</span><span class="sxs-lookup"><span data-stu-id="231b0-104">ContextPopup element</span></span>

<span data-ttu-id="231b0-105">Representa el [control Context Popup](windowsribbon-controls-contextpopup.md) en la vista ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="231b0-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="231b0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="231b0-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="231b0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="231b0-107">Attributes</span></span>

<span data-ttu-id="231b0-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="231b0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="231b0-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="231b0-109">Child elements</span></span>



| <span data-ttu-id="231b0-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="231b0-110">Element</span></span>                                                                                         | <span data-ttu-id="231b0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="231b0-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="231b0-112">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="231b0-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="231b0-113">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="231b0-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="231b0-114">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="231b0-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="231b0-115">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="231b0-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="231b0-116">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="231b0-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="231b0-117">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="231b0-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="231b0-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="231b0-118">Parent elements</span></span>



| <span data-ttu-id="231b0-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="231b0-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="231b0-120">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="231b0-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="231b0-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="231b0-121">Remarks</span></span>

<span data-ttu-id="231b0-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="231b0-122">Optional.</span></span>

<span data-ttu-id="231b0-123">Puede producirse como máximo una vez para [**cada Application.Views**](windowsribbon-element-application-views.md).</span><span class="sxs-lookup"><span data-stu-id="231b0-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="231b0-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="231b0-124">Examples</span></span>

<span data-ttu-id="231b0-125">En el ejemplo siguiente se muestra el marcado básico para una **vista ContextPopup.**</span><span class="sxs-lookup"><span data-stu-id="231b0-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="231b0-126">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="231b0-126">Element information</span></span>

* <span data-ttu-id="231b0-127">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="231b0-127">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="231b0-128">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="231b0-128">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="231b0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="231b0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231b0-130">Control Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="231b0-130">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






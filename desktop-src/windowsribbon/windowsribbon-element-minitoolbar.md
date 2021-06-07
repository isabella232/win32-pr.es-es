---
title: MiniToolbar, elemento
description: Representa una barra de herramientas contextual.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Cinta de opciones de Windows del elemento MiniToolbar
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443266"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="793c3-104">MiniToolbar, elemento</span><span class="sxs-lookup"><span data-stu-id="793c3-104">MiniToolbar element</span></span>

<span data-ttu-id="793c3-105">Representa una barra de herramientas contextual.</span><span class="sxs-lookup"><span data-stu-id="793c3-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="793c3-106">Uso</span><span class="sxs-lookup"><span data-stu-id="793c3-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="793c3-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="793c3-107">Attributes</span></span>



| <span data-ttu-id="793c3-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="793c3-108">Attribute</span></span>           | <span data-ttu-id="793c3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="793c3-109">Type</span></span>                 | <span data-ttu-id="793c3-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="793c3-110">Required</span></span>       | <span data-ttu-id="793c3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="793c3-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="793c3-112">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="793c3-112">**Name**</span></span><br/> | <span data-ttu-id="793c3-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="793c3-113">xs:string</span></span><br/> | <span data-ttu-id="793c3-114">Sí</span><span class="sxs-lookup"><span data-stu-id="793c3-114">Yes</span></span><br/> | <span data-ttu-id="793c3-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="793c3-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="793c3-116">Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="793c3-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="793c3-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="793c3-117">Child elements</span></span>



| <span data-ttu-id="793c3-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="793c3-118">Element</span></span>                                                         | <span data-ttu-id="793c3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="793c3-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="793c3-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="793c3-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="793c3-121">Debe producirse al menos una vez</span><span class="sxs-lookup"><span data-stu-id="793c3-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="793c3-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="793c3-122">Parent elements</span></span>



| <span data-ttu-id="793c3-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="793c3-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="793c3-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="793c3-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="793c3-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="793c3-125">Remarks</span></span>

<span data-ttu-id="793c3-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="793c3-126">Optional.</span></span>

<span data-ttu-id="793c3-127">Puede producirse una o varias veces para [**cada ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="793c3-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="793c3-128">A diferencia [**del elemento ContextMenu,**](windowsribbon-element-contextmenu.md) **minitoolbar** permanece visible cuando se hace clic en un elemento de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="793c3-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="793c3-129">Si se muestra sin [**contextMenu,**](windowsribbon-element-contextmenu.md) **la barra miniherramienta** se atenua cuando se desplaza el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="793c3-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="793c3-130">Debido a este comportamiento de desvanezco, [**contextMenu**](windowsribbon-element-contextmenu.md) debe mostrarse cerca del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="793c3-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="793c3-131">Dado que los controles de **MiniToolbar** no son accesibles mediante el teclado, los comandos que exponen deben estar disponibles en otra parte de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="793c3-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="793c3-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="793c3-132">Examples</span></span>

<span data-ttu-id="793c3-133">En el ejemplo siguiente se muestra el marcado básico para una [**vista ContextPopup.**](windowsribbon-element-contextpopup.md)</span><span class="sxs-lookup"><span data-stu-id="793c3-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="793c3-134">En esta sección de código se muestra un conjunto de declaraciones de control **MiniToolbar.**</span><span class="sxs-lookup"><span data-stu-id="793c3-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="793c3-135">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="793c3-135">Element information</span></span>

* <span data-ttu-id="793c3-136">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="793c3-136">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="793c3-137">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="793c3-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="793c3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="793c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793c3-139">Control Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="793c3-139">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






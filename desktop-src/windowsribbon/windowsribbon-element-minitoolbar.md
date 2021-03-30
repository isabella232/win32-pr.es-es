---
title: Elemento MiniToolbar
description: Representa una barra de herramientas contextual.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- MiniToolbar cinta de opciones de Windows
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148873"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="e1df0-104">Elemento MiniToolbar</span><span class="sxs-lookup"><span data-stu-id="e1df0-104">MiniToolbar element</span></span>

<span data-ttu-id="e1df0-105">Representa una barra de herramientas contextual.</span><span class="sxs-lookup"><span data-stu-id="e1df0-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="e1df0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e1df0-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="e1df0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1df0-107">Attributes</span></span>



| <span data-ttu-id="e1df0-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="e1df0-108">Attribute</span></span>           | <span data-ttu-id="e1df0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1df0-109">Type</span></span>                 | <span data-ttu-id="e1df0-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e1df0-110">Required</span></span>       | <span data-ttu-id="e1df0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1df0-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1df0-112">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e1df0-112">**Name**</span></span><br/> | <span data-ttu-id="e1df0-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e1df0-113">xs:string</span></span><br/> | <span data-ttu-id="e1df0-114">Sí</span><span class="sxs-lookup"><span data-stu-id="e1df0-114">Yes</span></span><br/> | <span data-ttu-id="e1df0-115"><dt> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="e1df0-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e1df0-116">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="e1df0-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="e1df0-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1df0-117">Child elements</span></span>



| <span data-ttu-id="e1df0-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1df0-118">Element</span></span>                                                         | <span data-ttu-id="e1df0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1df0-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="e1df0-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="e1df0-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="e1df0-121">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="e1df0-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e1df0-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e1df0-122">Parent elements</span></span>



| <span data-ttu-id="e1df0-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1df0-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1df0-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="e1df0-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e1df0-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1df0-125">Remarks</span></span>

<span data-ttu-id="e1df0-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e1df0-126">Optional.</span></span>

<span data-ttu-id="e1df0-127">Puede producirse una o varias veces para cada [**ContextPopup. MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="e1df0-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="e1df0-128">A diferencia del elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , el **MiniToolbar** permanece visible cuando se hace clic en un elemento de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e1df0-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="e1df0-129">Si se muestra sin un [**ContextMenu**](windowsribbon-element-contextmenu.md), el **MiniToolbar** se atenúa cuando se mueve el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="e1df0-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="e1df0-130">Debido a este comportamiento de difuminación, se debe mostrar un [**ContextMenu**](windowsribbon-element-contextmenu.md) cerca del puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="e1df0-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="e1df0-131">Dado que los controles de **MiniToolbar** no son accesibles desde el teclado, los comandos que exponen deben estar disponibles en cualquier parte de la interfaz de usuario de la cinta.</span><span class="sxs-lookup"><span data-stu-id="e1df0-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="e1df0-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e1df0-132">Examples</span></span>

<span data-ttu-id="e1df0-133">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="e1df0-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="e1df0-134">En esta sección de código se muestra un conjunto de declaraciones de control **MiniToolbar** .</span><span class="sxs-lookup"><span data-stu-id="e1df0-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e1df0-135">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e1df0-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="e1df0-136">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1df0-136">Minimum supported system</span></span><br/> | <span data-ttu-id="e1df0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1df0-137">Windows 7</span></span> |
| <span data-ttu-id="e1df0-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e1df0-138">Can be empty</span></span>                        | <span data-ttu-id="e1df0-139">No</span><span class="sxs-lookup"><span data-stu-id="e1df0-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="e1df0-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1df0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1df0-141">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="e1df0-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






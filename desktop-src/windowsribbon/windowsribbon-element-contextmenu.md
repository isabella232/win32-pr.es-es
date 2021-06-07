---
title: Elemento ContextMenu
description: Representa un control de menú contextual.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Elemento ContextMenu de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 916a031ed642a76fb22ecc58dbbe1ce29cbcd105
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443476"
---
# <a name="contextmenu-element"></a><span data-ttu-id="8b451-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="8b451-104">ContextMenu element</span></span>

<span data-ttu-id="8b451-105">Representa un control de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="8b451-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="8b451-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8b451-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="8b451-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b451-107">Attributes</span></span>



| <span data-ttu-id="8b451-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="8b451-108">Attribute</span></span>           | <span data-ttu-id="8b451-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b451-109">Type</span></span>                 | <span data-ttu-id="8b451-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="8b451-110">Required</span></span>       | <span data-ttu-id="8b451-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b451-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b451-112">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8b451-112">**Name**</span></span><br/> | <span data-ttu-id="8b451-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="8b451-113">xs:string</span></span><br/> | <span data-ttu-id="8b451-114">Sí</span><span class="sxs-lookup"><span data-stu-id="8b451-114">Yes</span></span><br/> | <span data-ttu-id="8b451-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="8b451-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8b451-116">Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="8b451-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="8b451-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b451-117">Child elements</span></span>



| <span data-ttu-id="8b451-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b451-118">Element</span></span>                                                         | <span data-ttu-id="8b451-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b451-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8b451-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="8b451-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="8b451-121">Debe producirse al menos una vez</span><span class="sxs-lookup"><span data-stu-id="8b451-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8b451-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8b451-122">Parent elements</span></span>



| <span data-ttu-id="8b451-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b451-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b451-124">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="8b451-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8b451-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b451-125">Remarks</span></span>

<span data-ttu-id="8b451-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8b451-126">Optional.</span></span>

<span data-ttu-id="8b451-127">Puede producirse una o varias veces para [**cada ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="8b451-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b451-128">ContextMenu **no** puede hospedar [controles Combo Box](windowsribbon-controls-combobox.md) o [Spinner.](windowsribbon-controls-spinner.md)</span><span class="sxs-lookup"><span data-stu-id="8b451-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8b451-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b451-129">Examples</span></span>

<span data-ttu-id="8b451-130">En el ejemplo siguiente se muestra el marcado básico para una [**vista ContextPopup.**](windowsribbon-element-contextpopup.md)</span><span class="sxs-lookup"><span data-stu-id="8b451-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="8b451-131">En esta sección de código se muestra un conjunto de declaraciones de control **ContextMenu.**</span><span class="sxs-lookup"><span data-stu-id="8b451-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8b451-132">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8b451-132">Element information</span></span>

* <span data-ttu-id="8b451-133">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b451-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="8b451-134">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="8b451-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="8b451-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b451-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b451-136">Control Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="8b451-136">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






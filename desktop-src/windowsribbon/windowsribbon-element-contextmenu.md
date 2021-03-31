---
title: Elemento ContextMenu
description: Representa un control de menú contextual.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Barra de herramientas de Windows de elemento ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783916"
---
# <a name="contextmenu-element"></a><span data-ttu-id="a53a5-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="a53a5-104">ContextMenu element</span></span>

<span data-ttu-id="a53a5-105">Representa un control de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="a53a5-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="a53a5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a53a5-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="a53a5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a53a5-107">Attributes</span></span>



| <span data-ttu-id="a53a5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a53a5-108">Attribute</span></span>           | <span data-ttu-id="a53a5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a53a5-109">Type</span></span>                 | <span data-ttu-id="a53a5-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a53a5-110">Required</span></span>       | <span data-ttu-id="a53a5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53a5-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53a5-112">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a53a5-112">**Name**</span></span><br/> | <span data-ttu-id="a53a5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a53a5-113">xs:string</span></span><br/> | <span data-ttu-id="a53a5-114">Sí</span><span class="sxs-lookup"><span data-stu-id="a53a5-114">Yes</span></span><br/> | <span data-ttu-id="a53a5-115"><dt> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a53a5-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a53a5-116">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a53a5-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="a53a5-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a53a5-117">Child elements</span></span>



| <span data-ttu-id="a53a5-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="a53a5-118">Element</span></span>                                                         | <span data-ttu-id="a53a5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53a5-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="a53a5-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a53a5-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="a53a5-121">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="a53a5-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a53a5-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a53a5-122">Parent elements</span></span>



| <span data-ttu-id="a53a5-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="a53a5-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a53a5-124">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="a53a5-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a53a5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a53a5-125">Remarks</span></span>

<span data-ttu-id="a53a5-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a53a5-126">Optional.</span></span>

<span data-ttu-id="a53a5-127">Puede producirse una o varias veces para cada [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="a53a5-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a53a5-128">Un control **ContextMenu** no puede hospedar controles de [cuadro combinado](windowsribbon-controls-combobox.md) o [control de número](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="a53a5-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a53a5-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a53a5-129">Examples</span></span>

<span data-ttu-id="a53a5-130">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="a53a5-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="a53a5-131">En esta sección de código se muestra un conjunto de declaraciones de control **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="a53a5-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a53a5-132">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a53a5-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a53a5-133">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a53a5-133">Minimum supported system</span></span><br/> | <span data-ttu-id="a53a5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a53a5-134">Windows 7</span></span> |
| <span data-ttu-id="a53a5-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a53a5-135">Can be empty</span></span>                        | <span data-ttu-id="a53a5-136">No</span><span class="sxs-lookup"><span data-stu-id="a53a5-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="a53a5-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a53a5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53a5-138">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="a53a5-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






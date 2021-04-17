---
title: Elemento ContextMap
description: Representa una asignación de par de ContextMenu y MiniToolbar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- ContextMap cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2ddcc8bdea16f5e00974b2b2e58934941e44c68
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105704895"
---
# <a name="contextmap-element"></a><span data-ttu-id="a8a01-104">Elemento ContextMap</span><span class="sxs-lookup"><span data-stu-id="a8a01-104">ContextMap element</span></span>

<span data-ttu-id="a8a01-105">Representa una asignación de par de [**ContextMenu**](windowsribbon-element-contextmenu.md) y [**MiniToolbar**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a01-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="a8a01-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a8a01-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="a8a01-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8a01-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8a01-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a8a01-108">Attribute</span></span></th>
<th><span data-ttu-id="a8a01-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8a01-109">Type</span></span></th>
<th><span data-ttu-id="a8a01-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a8a01-110">Required</span></span></th>
<th><span data-ttu-id="a8a01-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8a01-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8a01-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a8a01-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a8a01-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="a8a01-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a8a01-114">No</span><span class="sxs-lookup"><span data-stu-id="a8a01-114">No</span></span><br/></td>
<td><span data-ttu-id="a8a01-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a8a01-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a8a01-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="a8a01-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a8a01-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a8a01-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a8a01-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a8a01-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a8a01-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8a01-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8a01-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="a8a01-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="a8a01-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="a8a01-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="a8a01-122">No</span><span class="sxs-lookup"><span data-stu-id="a8a01-122">No</span></span><br/></td>
<td><span data-ttu-id="a8a01-123">Debe corresponder a un <a href="windowsribbon-element-contextmenu.md"><strong></strong></a> <em>nombre</em>de ContextMenu existente.</span><span class="sxs-lookup"><span data-stu-id="a8a01-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="a8a01-124">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a8a01-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a8a01-125">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a8a01-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8a01-126"><strong>MiniToolbar</strong></span><span class="sxs-lookup"><span data-stu-id="a8a01-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="a8a01-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="a8a01-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="a8a01-128">No</span><span class="sxs-lookup"><span data-stu-id="a8a01-128">No</span></span><br/></td>
<td><span data-ttu-id="a8a01-129">Debe corresponder a un <a href="windowsribbon-element-minitoolbar.md"><strong></strong></a> <em>nombre</em>de MiniToolbar existente.</span><span class="sxs-lookup"><span data-stu-id="a8a01-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="a8a01-130">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="a8a01-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a8a01-131">Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="a8a01-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a8a01-132">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8a01-132">Child elements</span></span>

<span data-ttu-id="a8a01-133">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a8a01-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a8a01-134">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a8a01-134">Parent elements</span></span>



| <span data-ttu-id="a8a01-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8a01-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8a01-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="a8a01-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a8a01-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8a01-137">Remarks</span></span>

<span data-ttu-id="a8a01-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a01-138">Optional.</span></span>

<span data-ttu-id="a8a01-139">Puede producirse una o varias veces para cada [**ContextPopup. ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="a8a01-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a8a01-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a8a01-140">Examples</span></span>

<span data-ttu-id="a8a01-141">En el ejemplo siguiente se muestra el marcado básico de una vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a01-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="a8a01-142">En esta sección de código se muestra un conjunto de declaraciones de control **ContextMap** .</span><span class="sxs-lookup"><span data-stu-id="a8a01-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a8a01-143">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a8a01-143">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a8a01-144">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8a01-144">Minimum supported system</span></span><br/> | <span data-ttu-id="a8a01-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8a01-145">Windows 7</span></span> |
| <span data-ttu-id="a8a01-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a8a01-146">Can be empty</span></span>                        | <span data-ttu-id="a8a01-147">Sí</span><span class="sxs-lookup"><span data-stu-id="a8a01-147">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="a8a01-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8a01-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a01-149">Control popup de contexto</span><span class="sxs-lookup"><span data-stu-id="a8a01-149">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 






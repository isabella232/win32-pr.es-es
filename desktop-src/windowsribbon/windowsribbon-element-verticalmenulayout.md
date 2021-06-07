---
title: Elemento VerticalMenuLayout
description: Representa un diseño vertical para los elementos de una galería.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444056"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="61914-104">Elemento VerticalMenuLayout</span><span class="sxs-lookup"><span data-stu-id="61914-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="61914-105">Representa un diseño vertical para los elementos de una galería.</span><span class="sxs-lookup"><span data-stu-id="61914-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="61914-106">Uso</span><span class="sxs-lookup"><span data-stu-id="61914-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="61914-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="61914-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61914-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="61914-108">Attribute</span></span></th>
<th><span data-ttu-id="61914-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="61914-109">Type</span></span></th>
<th><span data-ttu-id="61914-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="61914-110">Required</span></span></th>
<th><span data-ttu-id="61914-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="61914-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61914-112"><strong>Pinza</strong></span><span class="sxs-lookup"><span data-stu-id="61914-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="61914-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="61914-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="61914-114">No</span><span class="sxs-lookup"><span data-stu-id="61914-114">No</span></span><br/></td>
<td><span data-ttu-id="61914-115">Un identificador de tamaño asociado a la lista desplegable de la galería.</span><span class="sxs-lookup"><span data-stu-id="61914-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="61914-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="61914-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="61914-117">
<dt><span></span><span></span><strong></strong> (Ninguno)</span><span class="sxs-lookup"><span data-stu-id="61914-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="61914-118"><dt><span></span><span></span><strong></strong> (Vertical)</span><span class="sxs-lookup"><span data-stu-id="61914-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="61914-119">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61914-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61914-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="61914-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="61914-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="61914-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="61914-122">No</span><span class="sxs-lookup"><span data-stu-id="61914-122">No</span></span><br/></td>
<td><span data-ttu-id="61914-123"><strong>Windows 8 y versiones más recientes</strong></span><span class="sxs-lookup"><span data-stu-id="61914-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="61914-124">Resalta todos los elementos de la lista hasta el elemento actual del mouseover (en lugar de solo el elemento de mouseover).</span><span class="sxs-lookup"><span data-stu-id="61914-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="61914-125">Normalmente se usa para varias <strong>funcionalidades deshacer</strong> <strong>y rehacer.</strong></span><span class="sxs-lookup"><span data-stu-id="61914-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="61914-126">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="61914-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="61914-127"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="61914-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="61914-128">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61914-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61914-129"><strong>Filas</strong></span><span class="sxs-lookup"><span data-stu-id="61914-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="61914-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="61914-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="61914-131">No</span><span class="sxs-lookup"><span data-stu-id="61914-131">No</span></span><br/></td>
<td><span data-ttu-id="61914-132">Especifica el número de filas de elementos que se verán sin desplazarse.</span><span class="sxs-lookup"><span data-stu-id="61914-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="61914-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="61914-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="61914-134">Cualquier entero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="61914-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="61914-135">El valor predeterminado <strong>es -1,</strong> que especifica que se muestren tantas filas de elementos como sea posible.</span><span class="sxs-lookup"><span data-stu-id="61914-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="61914-136">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61914-136">Child elements</span></span>

<span data-ttu-id="61914-137">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="61914-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="61914-138">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="61914-138">Parent elements</span></span>



| <span data-ttu-id="61914-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="61914-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61914-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="61914-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="61914-141">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="61914-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="61914-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="61914-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="61914-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61914-143">Remarks</span></span>

<span data-ttu-id="61914-144">Necesario.</span><span class="sxs-lookup"><span data-stu-id="61914-144">Required.</span></span>

<span data-ttu-id="61914-145">El **elemento VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deben producirse una vez para cada [**elemento DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)</span><span class="sxs-lookup"><span data-stu-id="61914-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="61914-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61914-146">Examples</span></span>

<span data-ttu-id="61914-147">En el ejemplo siguiente se muestra el marcado básico para un **elemento VerticalMenuLayout.**</span><span class="sxs-lookup"><span data-stu-id="61914-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="61914-148">En esta sección de código se muestran las declaraciones de control [**InRibbonGallery.**](windowsribbon-element-inribbongallery.md)</span><span class="sxs-lookup"><span data-stu-id="61914-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="61914-149">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="61914-149">Element information</span></span>


- <span data-ttu-id="61914-150">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="61914-150">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="61914-151">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="61914-151">**Can be empty**: Yes</span></span>



 

 






---
title: Elemento FlowMenuLayout
description: Representa un diseño horizontal con saltos de línea para los elementos de una galería.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Elemento FlowMenuLayout de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442886"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="7e200-104">Elemento FlowMenuLayout</span><span class="sxs-lookup"><span data-stu-id="7e200-104">FlowMenuLayout element</span></span>

<span data-ttu-id="7e200-105">Representa un diseño horizontal con saltos de línea para los elementos de una galería.</span><span class="sxs-lookup"><span data-stu-id="7e200-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="7e200-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7e200-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="7e200-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e200-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e200-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e200-108">Attribute</span></span></th>
<th><span data-ttu-id="7e200-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e200-109">Type</span></span></th>
<th><span data-ttu-id="7e200-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="7e200-110">Required</span></span></th>
<th><span data-ttu-id="7e200-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e200-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e200-112"><strong>Columnas</strong></span><span class="sxs-lookup"><span data-stu-id="7e200-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="7e200-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7e200-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7e200-114">No</span><span class="sxs-lookup"><span data-stu-id="7e200-114">No</span></span><br/></td>
<td><span data-ttu-id="7e200-115">Especifica el número de elementos que se mostrarán en una sola fila.</span><span class="sxs-lookup"><span data-stu-id="7e200-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="7e200-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="7e200-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="7e200-117">Cualquier entero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="7e200-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="7e200-118">El valor predeterminado es <strong>2</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e200-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e200-119"><strong>Pinza</strong></span><span class="sxs-lookup"><span data-stu-id="7e200-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="7e200-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="7e200-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="7e200-121">No</span><span class="sxs-lookup"><span data-stu-id="7e200-121">No</span></span><br/></td>
<td><span data-ttu-id="7e200-122">Un identificador de tamaño asociado a la lista desplegable de la galería.</span><span class="sxs-lookup"><span data-stu-id="7e200-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="7e200-123">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7e200-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="7e200-124">
<dt><span></span><span></span><strong></strong> (Ninguno)</span><span class="sxs-lookup"><span data-stu-id="7e200-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7e200-125"><dt><span></span><span></span><strong></strong> (Vertical)</span><span class="sxs-lookup"><span data-stu-id="7e200-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7e200-126"><dt><span></span><span></span><strong></strong> (Esquina)</span><span class="sxs-lookup"><span data-stu-id="7e200-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="7e200-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7e200-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e200-128"><strong>Filas</strong></span><span class="sxs-lookup"><span data-stu-id="7e200-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="7e200-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7e200-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="7e200-130">No</span><span class="sxs-lookup"><span data-stu-id="7e200-130">No</span></span><br/></td>
<td><span data-ttu-id="7e200-131">Especifica el número de filas de elementos que se verán sin desplazarse.</span><span class="sxs-lookup"><span data-stu-id="7e200-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="7e200-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="7e200-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="7e200-133">Cualquier entero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="7e200-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="7e200-134">El valor predeterminado <strong>es -1,</strong> que especifica que se muestren tantas filas de elementos como sea posible.</span><span class="sxs-lookup"><span data-stu-id="7e200-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7e200-135">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e200-135">Child elements</span></span>

<span data-ttu-id="7e200-136">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7e200-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7e200-137">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7e200-137">Parent elements</span></span>



| <span data-ttu-id="7e200-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e200-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e200-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="7e200-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="7e200-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="7e200-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="7e200-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="7e200-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7e200-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e200-142">Remarks</span></span>

<span data-ttu-id="7e200-143">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7e200-143">Required.</span></span>

<span data-ttu-id="7e200-144">El [**elemento VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o **FlowMenuLayout** deben producirse una vez para cada [**elemento DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)</span><span class="sxs-lookup"><span data-stu-id="7e200-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="7e200-145">Los elementos se organizan según las propiedades de salto de línea inherentes a los *atributos de* fila *y* columna.</span><span class="sxs-lookup"><span data-stu-id="7e200-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="7e200-146">Cuando el contenido supera la longitud de una sola línea, el menú interrumpe las líneas, ajusta las líneas y alinea el contenido correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e200-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="7e200-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e200-147">Examples</span></span>

<span data-ttu-id="7e200-148">En el ejemplo siguiente se muestra el marcado básico para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="7e200-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="7e200-149">En esta sección de código se muestra la declaración de control [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) con una **especificación FlowMenuLayout.**</span><span class="sxs-lookup"><span data-stu-id="7e200-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="7e200-150">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7e200-150">Element information</span></span>

* <span data-ttu-id="7e200-151">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e200-151">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="7e200-152">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="7e200-152">**Can be empty**: Yes</span></span>


 

 






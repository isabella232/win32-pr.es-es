---
title: Elemento InRibbonGallery
description: Representa la galería de In-Ribbon, un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones. Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery cinta de opciones de Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "104077479"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="2bdf7-105">Elemento InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="2bdf7-105">InRibbonGallery element</span></span>

<span data-ttu-id="2bdf7-106">Representa la [Galería en cinta](windowsribbon-controls-inribbongallery.md), un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="2bdf7-107">Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="2bdf7-108">Uso</span><span class="sxs-lookup"><span data-stu-id="2bdf7-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="2bdf7-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bdf7-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bdf7-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="2bdf7-110">Attribute</span></span></th>
<th><span data-ttu-id="2bdf7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bdf7-111">Type</span></span></th>
<th><span data-ttu-id="2bdf7-112">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2bdf7-112">Required</span></span></th>
<th><span data-ttu-id="2bdf7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bdf7-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bdf7-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-115">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="2bdf7-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2bdf7-116">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-116">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-117">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2bdf7-118">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2bdf7-119">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2bdf7-120">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2bdf7-121">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="2bdf7-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="2bdf7-124">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-124">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-125">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bdf7-126">Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="2bdf7-127">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="2bdf7-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2bdf7-128">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="2bdf7-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2bdf7-129">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-129">Default.</span></span> <br/> </dd> <span data-ttu-id="2bdf7-130"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="2bdf7-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-133">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-133">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-134">Junto con <em>ItemWidth</em>, determina el tamaño de la imagen del elemento que se muestra en el control de la galería.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bdf7-135">Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a</span><span class="sxs-lookup"><span data-stu-id="2bdf7-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="2bdf7-136">.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="2bdf7-137">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2bdf7-138">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-141">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-141">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-142">Junto con <em>ItemHeight</em>, determina el tamaño de la imagen del elemento que se muestra en el control de la galería.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bdf7-143">Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a</span><span class="sxs-lookup"><span data-stu-id="2bdf7-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="2bdf7-144">.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="2bdf7-145">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2bdf7-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-149">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-149">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-150">Especifica el número máximo de columnas que muestra el <strong>InRibbonGallery</strong> , por ejemplo, en la lista desplegable de diseño de grupo <em>grande</em> .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="2bdf7-151">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-154">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-154">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-155">Especifica el número máximo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño del grupo <em>mediano</em> , antes de cambiar a un diseño <em>grande</em> .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="2bdf7-156">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-159">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-159">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-160">Especifica el número máximo de filas para el diseño de los elementos <strong>InRibbonGallery</strong> .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="2bdf7-161">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2bdf7-162">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-165">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-165">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-166">Especifica el número mínimo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño de grupo <em>grande</em> , antes de cambiar a <em>medio</em>.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="2bdf7-167">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2bdf7-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2bdf7-170">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-170">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-171">Especifica el número mínimo de columnas que el <strong>InRibbonGallery</strong> muestra en el diseño del grupo <em>mediano</em> , antes de cambiar a <em>pequeño</em>.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="2bdf7-172">
<dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="2bdf7-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="2bdf7-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="2bdf7-175">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-175">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-176">Especifica dónde se muestra la etiqueta del elemento, en relación con la imagen.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="2bdf7-177">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2bdf7-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2bdf7-178">
<dt><span></span><span></span><strong></strong> Descendente</span><span class="sxs-lookup"><span data-stu-id="2bdf7-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-179"><dt><span></span><span></span><strong></strong> U</span><span class="sxs-lookup"><span data-stu-id="2bdf7-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-180"><dt><span></span><span></span><strong></strong> Salido</span><span class="sxs-lookup"><span data-stu-id="2bdf7-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-181"><dt><span></span><span></span><strong></strong> Superpone</span><span class="sxs-lookup"><span data-stu-id="2bdf7-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-182"><dt><span></span><span></span><strong></strong> Correcta</span><span class="sxs-lookup"><span data-stu-id="2bdf7-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-183"><dt><span></span><span></span><strong></strong> Primeras</span><span class="sxs-lookup"><span data-stu-id="2bdf7-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-184"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="2bdf7-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="2bdf7-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="2bdf7-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="2bdf7-186">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-186">No</span></span><br/></td>
<td><span data-ttu-id="2bdf7-187">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2bdf7-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2bdf7-188">
<dt><span></span><span></span><strong></strong> Elementos</span><span class="sxs-lookup"><span data-stu-id="2bdf7-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2bdf7-189"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="2bdf7-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2bdf7-190">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2bdf7-190">Child elements</span></span>



| <span data-ttu-id="2bdf7-191">Elemento</span><span class="sxs-lookup"><span data-stu-id="2bdf7-191">Element</span></span>                                                                                           | <span data-ttu-id="2bdf7-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bdf7-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2bdf7-193">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="2bdf7-194">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="2bdf7-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2bdf7-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="2bdf7-196">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="2bdf7-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="2bdf7-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="2bdf7-198">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="2bdf7-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="2bdf7-199">**Botón**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="2bdf7-200">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="2bdf7-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2bdf7-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="2bdf7-202">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="2bdf7-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2bdf7-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="2bdf7-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="2bdf7-204">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="2bdf7-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2bdf7-205">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2bdf7-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bdf7-206">Elemento</span><span class="sxs-lookup"><span data-stu-id="2bdf7-206">Element</span></span></th>
<th><span data-ttu-id="2bdf7-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bdf7-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bdf7-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bdf7-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2bdf7-209"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bdf7-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2bdf7-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bdf7-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="2bdf7-211">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="2bdf7-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bdf7-212">Remarks</span></span>

<span data-ttu-id="2bdf7-213">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-213">Optional.</span></span>

<span data-ttu-id="2bdf7-214">Puede aparecer como máximo una vez por cada elemento de [**Grupo**](windowsribbon-element-group.md) o [**ControlGroup**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2bdf7-215">En la captura de pantalla siguiente se muestra el control [Galería de cintas en cinta](windowsribbon-controls-inribbongallery.md) de opciones de Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de la galería de la cinta de opciones en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="2bdf7-217">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2bdf7-217">Examples</span></span>

<span data-ttu-id="2bdf7-218">En el ejemplo siguiente se muestra el marcado básico de una [Galería de la cinta de](windowsribbon-controls-inribbongallery.md)opciones.</span><span class="sxs-lookup"><span data-stu-id="2bdf7-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="2bdf7-219">En esta sección de código se muestran las declaraciones de comandos de **InRibbonGallery** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="2bdf7-220">En esta sección de código se muestran las declaraciones de control de **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="2bdf7-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2bdf7-221">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2bdf7-221">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2bdf7-222">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bdf7-222">Minimum supported system</span></span><br/> | <span data-ttu-id="2bdf7-223">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bdf7-223">Windows 7</span></span> |
| <span data-ttu-id="2bdf7-224">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2bdf7-224">Can be empty</span></span>                        | <span data-ttu-id="2bdf7-225">No</span><span class="sxs-lookup"><span data-stu-id="2bdf7-225">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="2bdf7-226">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2bdf7-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdf7-227">Control de la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="2bdf7-227">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="2bdf7-228">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="2bdf7-228">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="2bdf7-229">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="2bdf7-229">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 






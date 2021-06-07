---
title: Elemento InRibbonGallery
description: Representa el In-Ribbon galería, un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones. Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Cinta de opciones de Windows del elemento InRibbonGallery
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443376"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="38bec-105">Elemento InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="38bec-105">InRibbonGallery element</span></span>

<span data-ttu-id="38bec-106">Representa la [Galería en cinta](windowsribbon-controls-inribbongallery.md)de opciones , un control basado en la galería que expone un subconjunto predeterminado de elementos directamente en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="38bec-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="38bec-107">Los elementos restantes se muestran cuando se hace clic en un botón de menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="38bec-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="38bec-108">Uso</span><span class="sxs-lookup"><span data-stu-id="38bec-108">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="38bec-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="38bec-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38bec-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="38bec-110">Attribute</span></span></th>
<th><span data-ttu-id="38bec-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="38bec-111">Type</span></span></th>
<th><span data-ttu-id="38bec-112">Requerido</span><span class="sxs-lookup"><span data-stu-id="38bec-112">Required</span></span></th>
<th><span data-ttu-id="38bec-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="38bec-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38bec-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-115">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="38bec-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="38bec-116">No</span><span class="sxs-lookup"><span data-stu-id="38bec-116">No</span></span><br/></td>
<td><span data-ttu-id="38bec-117">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="38bec-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="38bec-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="38bec-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="38bec-119">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="38bec-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="38bec-120">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="38bec-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="38bec-121">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="38bec-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bec-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="38bec-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="38bec-124">No</span><span class="sxs-lookup"><span data-stu-id="38bec-124">No</span></span><br/></td>
<td><span data-ttu-id="38bec-125">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="38bec-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="38bec-126">Solo se aplica a galerías donde el valor del atributo <em>Type</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="38bec-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="38bec-127">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="38bec-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="38bec-128">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="38bec-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="38bec-129">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38bec-129">Default.</span></span> <br/> </dd> <span data-ttu-id="38bec-130"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="38bec-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-133">No</span><span class="sxs-lookup"><span data-stu-id="38bec-133">No</span></span><br/></td>
<td><span data-ttu-id="38bec-134">Junto con <em>ItemWidth</em>, determina el tamaño de la imagen de elemento que se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="38bec-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="38bec-135">Solo se aplica a galerías donde el valor del atributo <em>Type</em> es igual a</span><span class="sxs-lookup"><span data-stu-id="38bec-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="38bec-136">.</span><span class="sxs-lookup"><span data-stu-id="38bec-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="38bec-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="38bec-138">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="38bec-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bec-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-141">No</span><span class="sxs-lookup"><span data-stu-id="38bec-141">No</span></span><br/></td>
<td><span data-ttu-id="38bec-142">Junto con <em>ItemHeight</em>, determina el tamaño de la imagen de elemento que se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="38bec-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="38bec-143">Solo se aplica a galerías donde el valor del atributo <em>Type</em> es igual a</span><span class="sxs-lookup"><span data-stu-id="38bec-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="38bec-144">.</span><span class="sxs-lookup"><span data-stu-id="38bec-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="38bec-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="38bec-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="38bec-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-149">No</span><span class="sxs-lookup"><span data-stu-id="38bec-149">No</span></span><br/></td>
<td><span data-ttu-id="38bec-150">Especifica el número máximo de columnas que <strong>muestra InRibbonGallery,</strong> por ejemplo, en la lista desplegable <em>Diseño</em> de grupo grande.</span><span class="sxs-lookup"><span data-stu-id="38bec-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="38bec-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bec-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-154">No</span><span class="sxs-lookup"><span data-stu-id="38bec-154">No</span></span><br/></td>
<td><span data-ttu-id="38bec-155">Especifica el número máximo de columnas que <strong>InRibbonGallery</strong> muestra en el diseño del grupo Mediano, antes de cambiar a <em>Diseño</em> grande. <em></em></span><span class="sxs-lookup"><span data-stu-id="38bec-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="38bec-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-159">No</span><span class="sxs-lookup"><span data-stu-id="38bec-159">No</span></span><br/></td>
<td><span data-ttu-id="38bec-160">Especifica el número máximo de filas para el diseño de <strong>los elementos InRibbonGallery.</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="38bec-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="38bec-162">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="38bec-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bec-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-165">No</span><span class="sxs-lookup"><span data-stu-id="38bec-165">No</span></span><br/></td>
<td><span data-ttu-id="38bec-166">Especifica el número mínimo de columnas que <strong>inRibbonGallery</strong> muestra en el diseño <em>de</em> grupo grande, antes de cambiar a <em>Medio.</em></span><span class="sxs-lookup"><span data-stu-id="38bec-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="38bec-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38bec-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="38bec-170">No</span><span class="sxs-lookup"><span data-stu-id="38bec-170">No</span></span><br/></td>
<td><span data-ttu-id="38bec-171">Especifica el número mínimo de columnas que <strong>inRibbonGallery</strong> muestra en el diseño del grupo Mediano, antes de cambiar a <em>Pequeño</em>. <em></em></span><span class="sxs-lookup"><span data-stu-id="38bec-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="38bec-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="38bec-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38bec-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="38bec-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="38bec-175">No</span><span class="sxs-lookup"><span data-stu-id="38bec-175">No</span></span><br/></td>
<td><span data-ttu-id="38bec-176">Especifica dónde se muestra la etiqueta de elemento, en relación con la imagen.</span><span class="sxs-lookup"><span data-stu-id="38bec-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="38bec-177">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="38bec-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="38bec-178">
<dt><span></span><span></span><strong></strong> (Inferior)</span><span class="sxs-lookup"><span data-stu-id="38bec-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-179"><dt><span></span><span></span><strong></strong> (Ocultar)</span><span class="sxs-lookup"><span data-stu-id="38bec-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-180"><dt><span></span><span></span><strong></strong> (Izquierda)</span><span class="sxs-lookup"><span data-stu-id="38bec-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-181"><dt><span></span><span></span><strong></strong> (Superposición)</span><span class="sxs-lookup"><span data-stu-id="38bec-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-182"><dt><span></span><span></span><strong></strong> (Derecha)</span><span class="sxs-lookup"><span data-stu-id="38bec-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-183"><dt><span></span><span></span><strong></strong> (Superior)</span><span class="sxs-lookup"><span data-stu-id="38bec-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-184"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="38bec-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="38bec-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="38bec-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="38bec-186">No</span><span class="sxs-lookup"><span data-stu-id="38bec-186">No</span></span><br/></td>
<td><span data-ttu-id="38bec-187">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="38bec-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="38bec-188">
<dt><span></span><span></span><strong></strong> (Elementos)</span><span class="sxs-lookup"><span data-stu-id="38bec-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="38bec-189"><dt><span></span><span></span><strong></strong> (Comandos)</span><span class="sxs-lookup"><span data-stu-id="38bec-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="38bec-190">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38bec-190">Child elements</span></span>



| <span data-ttu-id="38bec-191">Elemento</span><span class="sxs-lookup"><span data-stu-id="38bec-191">Element</span></span>                                                                                           | <span data-ttu-id="38bec-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="38bec-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="38bec-193">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="38bec-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="38bec-194">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="38bec-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="38bec-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="38bec-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="38bec-196">Debe producirse exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="38bec-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="38bec-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="38bec-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="38bec-198">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="38bec-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="38bec-199">**Button**</span><span class="sxs-lookup"><span data-stu-id="38bec-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="38bec-200">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="38bec-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="38bec-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="38bec-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="38bec-202">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="38bec-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="38bec-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="38bec-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="38bec-204">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="38bec-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="38bec-205">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="38bec-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38bec-206">Elemento</span><span class="sxs-lookup"><span data-stu-id="38bec-206">Element</span></span></th>
<th><span data-ttu-id="38bec-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="38bec-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38bec-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="38bec-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="38bec-209"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="38bec-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="38bec-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="38bec-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="38bec-211">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="38bec-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="38bec-212">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38bec-212">Remarks</span></span>

<span data-ttu-id="38bec-213">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38bec-213">Optional.</span></span>

<span data-ttu-id="38bec-214">Puede producirse como máximo una vez para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="38bec-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="38bec-215">En la siguiente captura de pantalla se muestra el control [De](windowsribbon-controls-inribbongallery.md) la cinta de opciones en la galería Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38bec-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de la galería en la cinta de opciones de microsoft paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="38bec-217">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38bec-217">Examples</span></span>

<span data-ttu-id="38bec-218">En el ejemplo siguiente se muestra el marcado básico para una [galería en cinta de opciones](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="38bec-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="38bec-219">En esta sección de código se muestran las declaraciones [](windowsribbon-element-group.md) del comando **InRibbonGallery,** con un grupo asociado que actúa como contenedor primario para el **elemento InRibbonGallery.**</span><span class="sxs-lookup"><span data-stu-id="38bec-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


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



<span data-ttu-id="38bec-220">En esta sección de código se muestran las declaraciones de control **InRibbonGallery.**</span><span class="sxs-lookup"><span data-stu-id="38bec-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="38bec-221">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="38bec-221">Element information</span></span>


* <span data-ttu-id="38bec-222">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="38bec-222">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="38bec-223">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="38bec-223">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="38bec-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="38bec-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38bec-225">Control de la Galería en la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="38bec-225">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="38bec-226">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="38bec-226">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="38bec-227">Ejemplo de galería</span><span class="sxs-lookup"><span data-stu-id="38bec-227">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 






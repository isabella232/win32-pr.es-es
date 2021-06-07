---
title: Elemento SplitButtonGallery
description: Representa un control Split Button Gallery (Dividir galería de botones) con un menú desplegable basado en la galería.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5f8767135b9472acba333b1cdfa6ab102e9b7f4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444836"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="70ce7-104">Elemento SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="70ce7-104">SplitButtonGallery element</span></span>

<span data-ttu-id="70ce7-105">Representa un [control Split Button Gallery (Dividir](windowsribbon-controls-splitbuttongallery.md) galería de botones) con un menú desplegable basado en la galería.</span><span class="sxs-lookup"><span data-stu-id="70ce7-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="70ce7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="70ce7-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="70ce7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="70ce7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70ce7-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="70ce7-108">Attribute</span></span></th>
<th><span data-ttu-id="70ce7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="70ce7-109">Type</span></span></th>
<th><span data-ttu-id="70ce7-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="70ce7-110">Required</span></span></th>
<th><span data-ttu-id="70ce7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ce7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70ce7-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="70ce7-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="70ce7-114">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-114">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-115">Solo es válido <a href="windowsribbon-element-menugroup.md"><strong>si MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="70ce7-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="70ce7-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="70ce7-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="70ce7-117">Cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="70ce7-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="70ce7-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="70ce7-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="70ce7-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="70ce7-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ce7-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="70ce7-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="70ce7-122">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-122">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70ce7-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="70ce7-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="70ce7-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="70ce7-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="70ce7-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="70ce7-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="70ce7-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="70ce7-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="70ce7-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ce7-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="70ce7-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="70ce7-130">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-130">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-131">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="70ce7-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70ce7-132">Solo se aplica a galerías donde el valor del atributo <em>Type</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="70ce7-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="70ce7-133">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="70ce7-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="70ce7-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="70ce7-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="70ce7-135">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="70ce7-135">Default.</span></span> <br/> </dd> <span data-ttu-id="70ce7-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="70ce7-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ce7-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="70ce7-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="70ce7-139">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-139">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="70ce7-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="70ce7-141">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="70ce7-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ce7-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="70ce7-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="70ce7-144">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-144">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="70ce7-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="70ce7-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="70ce7-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ce7-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="70ce7-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="70ce7-149">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-149">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-150">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="70ce7-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="70ce7-151">
<dt><span></span><span></span><strong></strong> (Inferior)</span><span class="sxs-lookup"><span data-stu-id="70ce7-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-152"><dt><span></span><span></span><strong></strong> (Ocultar)</span><span class="sxs-lookup"><span data-stu-id="70ce7-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-153"><dt><span></span><span></span><strong></strong> (Izquierda)</span><span class="sxs-lookup"><span data-stu-id="70ce7-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-154"><dt><span></span><span></span><strong></strong> (Superposición)</span><span class="sxs-lookup"><span data-stu-id="70ce7-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-155"><dt><span></span><span></span><strong></strong> (Derecha)</span><span class="sxs-lookup"><span data-stu-id="70ce7-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-156"><dt><span></span><span></span><strong></strong> (Superior)</span><span class="sxs-lookup"><span data-stu-id="70ce7-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ce7-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="70ce7-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="70ce7-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="70ce7-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="70ce7-159">No</span><span class="sxs-lookup"><span data-stu-id="70ce7-159">No</span></span><br/></td>
<td><span data-ttu-id="70ce7-160">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="70ce7-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="70ce7-161">
<dt><span></span><span></span><strong></strong> (Elementos)</span><span class="sxs-lookup"><span data-stu-id="70ce7-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="70ce7-162"><dt><span></span><span></span><strong></strong> (Comandos)</span><span class="sxs-lookup"><span data-stu-id="70ce7-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="70ce7-163">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70ce7-163">Child elements</span></span>



| <span data-ttu-id="70ce7-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="70ce7-164">Element</span></span>                                                                                                 | <span data-ttu-id="70ce7-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ce7-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="70ce7-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="70ce7-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="70ce7-167">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="70ce7-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="70ce7-168">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="70ce7-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="70ce7-169">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="70ce7-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="70ce7-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="70ce7-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="70ce7-171">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="70ce7-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="70ce7-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="70ce7-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="70ce7-173">Debe producirse exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="70ce7-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="70ce7-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="70ce7-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="70ce7-175">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="70ce7-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="70ce7-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="70ce7-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="70ce7-177">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="70ce7-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="70ce7-178">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="70ce7-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70ce7-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="70ce7-179">Element</span></span></th>
<th><span data-ttu-id="70ce7-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ce7-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70ce7-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="70ce7-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="70ce7-182"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="70ce7-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="70ce7-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="70ce7-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="70ce7-184">Cuando se encuentra en un <a href="windowsribbon-element-applicationmenu.md"><strong>elemento ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70ce7-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="70ce7-185">Este elemento solo se admite en el primer nivel y no debe tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="70ce7-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70ce7-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="70ce7-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="70ce7-187">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="70ce7-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70ce7-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="70ce7-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="70ce7-189">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70ce7-189">Remarks</span></span>

<span data-ttu-id="70ce7-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="70ce7-190">Optional.</span></span>

<span data-ttu-id="70ce7-191">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton.**](windowsribbon-element-splitbutton.md)</span><span class="sxs-lookup"><span data-stu-id="70ce7-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="70ce7-192">**SplitButtonGallery admite los** [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="70ce7-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="70ce7-193">[Interfaz de usuario \_ Una aplicación usa PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) para consultar el estado de alternancia del control de botón de **splitButtonGallery.**</span><span class="sxs-lookup"><span data-stu-id="70ce7-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="70ce7-194">En la siguiente captura de pantalla se muestra el [control](windowsribbon-controls-splitbuttongallery.md) Galería de botones de división de la cinta Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70ce7-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de galería de botón de división en Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="70ce7-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="70ce7-196">Examples</span></span>

<span data-ttu-id="70ce7-197">En el ejemplo siguiente se muestra el marcado básico para la Galería [de botones de división](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="70ce7-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="70ce7-198">En esta sección de código se muestran las declaraciones del comando **SplitButtonGallery,** con un grupo asociado que funciona como contenedor primario para el **elemento SplitButtonGallery.** [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="70ce7-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="70ce7-199">En esta sección de código se muestran las declaraciones de control **SplitButtonGallery.**</span><span class="sxs-lookup"><span data-stu-id="70ce7-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="70ce7-200">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="70ce7-200">Element information</span></span>


- <span data-ttu-id="70ce7-201">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="70ce7-201">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="70ce7-202">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="70ce7-202">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="70ce7-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="70ce7-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ce7-204">Control Split Button Gallery (Galería de botones de división)</span><span class="sxs-lookup"><span data-stu-id="70ce7-204">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="70ce7-205">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="70ce7-205">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="70ce7-206">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="70ce7-206">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="70ce7-207">Ejemplo de galería</span><span class="sxs-lookup"><span data-stu-id="70ce7-207">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 


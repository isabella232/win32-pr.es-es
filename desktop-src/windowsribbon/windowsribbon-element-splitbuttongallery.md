---
title: Elemento SplitButtonGallery
description: Representa un control de galería de botones de expansión con un menú desplegable basado en la galería.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488054"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="312a0-104">Elemento SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="312a0-104">SplitButtonGallery element</span></span>

<span data-ttu-id="312a0-105">Representa un control de [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md) con un menú desplegable basado en la galería.</span><span class="sxs-lookup"><span data-stu-id="312a0-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="312a0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="312a0-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="312a0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="312a0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="312a0-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="312a0-108">Attribute</span></span></th>
<th><span data-ttu-id="312a0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="312a0-109">Type</span></span></th>
<th><span data-ttu-id="312a0-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="312a0-110">Required</span></span></th>
<th><span data-ttu-id="312a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="312a0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="312a0-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="312a0-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="312a0-114">No</span><span class="sxs-lookup"><span data-stu-id="312a0-114">No</span></span><br/></td>
<td><span data-ttu-id="312a0-115">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="312a0-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="312a0-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="312a0-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="312a0-117">Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="312a0-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="312a0-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="312a0-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="312a0-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="312a0-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="312a0-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-121">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="312a0-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="312a0-122">No</span><span class="sxs-lookup"><span data-stu-id="312a0-122">No</span></span><br/></td>
<td><span data-ttu-id="312a0-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="312a0-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="312a0-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="312a0-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="312a0-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="312a0-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="312a0-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="312a0-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="312a0-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="312a0-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="312a0-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="312a0-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="312a0-130">No</span><span class="sxs-lookup"><span data-stu-id="312a0-130">No</span></span><br/></td>
<td><span data-ttu-id="312a0-131">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="312a0-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="312a0-132">Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="312a0-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="312a0-133">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="312a0-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="312a0-134">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="312a0-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="312a0-135">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="312a0-135">Default.</span></span> <br/> </dd> <span data-ttu-id="312a0-136"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="312a0-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="312a0-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="312a0-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="312a0-139">No</span><span class="sxs-lookup"><span data-stu-id="312a0-139">No</span></span><br/></td>
<td><span data-ttu-id="312a0-140"><dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="312a0-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="312a0-141">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="312a0-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="312a0-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="312a0-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="312a0-144">No</span><span class="sxs-lookup"><span data-stu-id="312a0-144">No</span></span><br/></td>
<td><span data-ttu-id="312a0-145"><dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="312a0-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="312a0-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="312a0-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="312a0-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="312a0-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="312a0-149">No</span><span class="sxs-lookup"><span data-stu-id="312a0-149">No</span></span><br/></td>
<td><span data-ttu-id="312a0-150">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="312a0-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="312a0-151">
<dt><span></span><span></span><strong></strong> Descendente</span><span class="sxs-lookup"><span data-stu-id="312a0-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-152"><dt><span></span><span></span><strong></strong> U</span><span class="sxs-lookup"><span data-stu-id="312a0-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-153"><dt><span></span><span></span><strong></strong> Salido</span><span class="sxs-lookup"><span data-stu-id="312a0-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-154"><dt><span></span><span></span><strong></strong> Superpone</span><span class="sxs-lookup"><span data-stu-id="312a0-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-155"><dt><span></span><span></span><strong></strong> Correcta</span><span class="sxs-lookup"><span data-stu-id="312a0-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-156"><dt><span></span><span></span><strong></strong> Primeras</span><span class="sxs-lookup"><span data-stu-id="312a0-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="312a0-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="312a0-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="312a0-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="312a0-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="312a0-159">No</span><span class="sxs-lookup"><span data-stu-id="312a0-159">No</span></span><br/></td>
<td><span data-ttu-id="312a0-160">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="312a0-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="312a0-161">
<dt><span></span><span></span><strong></strong> Elementos</span><span class="sxs-lookup"><span data-stu-id="312a0-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="312a0-162"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="312a0-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="312a0-163">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="312a0-163">Child elements</span></span>



| <span data-ttu-id="312a0-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="312a0-164">Element</span></span>                                                                                                 | <span data-ttu-id="312a0-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="312a0-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="312a0-166">**Botón**</span><span class="sxs-lookup"><span data-stu-id="312a0-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="312a0-167">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="312a0-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="312a0-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="312a0-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="312a0-169">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="312a0-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="312a0-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="312a0-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="312a0-171">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="312a0-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="312a0-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="312a0-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="312a0-173">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="312a0-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="312a0-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="312a0-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="312a0-175">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="312a0-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="312a0-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="312a0-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="312a0-177">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="312a0-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="312a0-178">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="312a0-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="312a0-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="312a0-179">Element</span></span></th>
<th><span data-ttu-id="312a0-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="312a0-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="312a0-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="312a0-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="312a0-182"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="312a0-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="312a0-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="312a0-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="312a0-184">Cuando está contenido en un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="312a0-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="312a0-185">Este elemento solo se admite en el primer nivel y no debe tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="312a0-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="312a0-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="312a0-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="312a0-187">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="312a0-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="312a0-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="312a0-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="312a0-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="312a0-189">Remarks</span></span>

<span data-ttu-id="312a0-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="312a0-190">Optional.</span></span>

<span data-ttu-id="312a0-191">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**splitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="312a0-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="312a0-192">**SplitButtonGallery** admite los [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="312a0-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="312a0-193">[Interfaz de usuario \_ Una aplicación utiliza PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) para consultar el estado de alternancia del control de botón de un **SplitButtonGallery**.</span><span class="sxs-lookup"><span data-stu-id="312a0-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="312a0-194">En la captura de pantalla siguiente se muestra el control [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md) de la cinta en Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="312a0-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control Galería de botones de división en Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="312a0-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="312a0-196">Examples</span></span>

<span data-ttu-id="312a0-197">En el ejemplo siguiente se muestra el marcado básico de la [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="312a0-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="312a0-198">En esta sección de código se muestran las declaraciones de comandos de **SplitButtonGallery** , con un [**Grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario para el elemento **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="312a0-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


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



<span data-ttu-id="312a0-199">En esta sección de código se muestran las declaraciones de control de **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="312a0-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="312a0-200">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="312a0-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="312a0-201">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312a0-201">Minimum supported system</span></span><br/> | <span data-ttu-id="312a0-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="312a0-202">Windows 7</span></span> |
| <span data-ttu-id="312a0-203">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="312a0-203">Can be empty</span></span>                        | <span data-ttu-id="312a0-204">No</span><span class="sxs-lookup"><span data-stu-id="312a0-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="312a0-205">Consulte también</span><span class="sxs-lookup"><span data-stu-id="312a0-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312a0-206">Control Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="312a0-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="312a0-207">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="312a0-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="312a0-208">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="312a0-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="312a0-209">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="312a0-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 


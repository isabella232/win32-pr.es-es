---
title: Elemento DropDownGallery
description: Representa un control de galería de Drop-Down con un menú basado en la galería.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533226"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="5f286-104">Elemento DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="5f286-104">DropDownGallery element</span></span>

<span data-ttu-id="5f286-105">Representa un control de [Galería desplegable](windowsribbon-controls-dropdowngallery.md) con un menú basado en la galería.</span><span class="sxs-lookup"><span data-stu-id="5f286-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="5f286-106">Uso</span><span class="sxs-lookup"><span data-stu-id="5f286-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="5f286-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f286-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f286-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="5f286-108">Attribute</span></span></th>
<th><span data-ttu-id="5f286-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f286-109">Type</span></span></th>
<th><span data-ttu-id="5f286-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f286-110">Required</span></span></th>
<th><span data-ttu-id="5f286-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f286-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f286-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f286-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="5f286-114">No</span><span class="sxs-lookup"><span data-stu-id="5f286-114">No</span></span><br/></td>
<td><span data-ttu-id="5f286-115">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="5f286-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="5f286-116">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="5f286-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5f286-117">Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="5f286-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="5f286-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="5f286-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="5f286-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f286-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f286-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-121">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="5f286-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="5f286-122">No</span><span class="sxs-lookup"><span data-stu-id="5f286-122">No</span></span><br/></td>
<td><span data-ttu-id="5f286-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5f286-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="5f286-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="5f286-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="5f286-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="5f286-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="5f286-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="5f286-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="5f286-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f286-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f286-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="5f286-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="5f286-130">No</span><span class="sxs-lookup"><span data-stu-id="5f286-130">No</span></span><br/></td>
<td><span data-ttu-id="5f286-131">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de galería.</span><span class="sxs-lookup"><span data-stu-id="5f286-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5f286-132">Solo se aplica a galerías en las que el valor del atributo de <em>tipo</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="5f286-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="5f286-133">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="5f286-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="5f286-134">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="5f286-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="5f286-135">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5f286-135">Default.</span></span> <br/> </dd> <span data-ttu-id="5f286-136"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="5f286-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f286-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f286-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="5f286-139">No</span><span class="sxs-lookup"><span data-stu-id="5f286-139">No</span></span><br/></td>
<td><span data-ttu-id="5f286-140"><dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="5f286-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="5f286-141">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="5f286-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f286-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5f286-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="5f286-144">No</span><span class="sxs-lookup"><span data-stu-id="5f286-144">No</span></span><br/></td>
<td><span data-ttu-id="5f286-145"><dt><span></span><span></span><strong></strong> (XS: integer)</span><span class="sxs-lookup"><span data-stu-id="5f286-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="5f286-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="5f286-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f286-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="5f286-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="5f286-149">No</span><span class="sxs-lookup"><span data-stu-id="5f286-149">No</span></span><br/></td>
<td><span data-ttu-id="5f286-150">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5f286-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="5f286-151">
<dt><span></span><span></span><strong></strong> Descendente</span><span class="sxs-lookup"><span data-stu-id="5f286-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-152"><dt><span></span><span></span><strong></strong> U</span><span class="sxs-lookup"><span data-stu-id="5f286-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-153"><dt><span></span><span></span><strong></strong> Salido</span><span class="sxs-lookup"><span data-stu-id="5f286-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-154"><dt><span></span><span></span><strong></strong> Superpone</span><span class="sxs-lookup"><span data-stu-id="5f286-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-155"><dt><span></span><span></span><strong></strong> Correcta</span><span class="sxs-lookup"><span data-stu-id="5f286-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-156"><dt><span></span><span></span><strong></strong> Primeras</span><span class="sxs-lookup"><span data-stu-id="5f286-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f286-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="5f286-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="5f286-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f286-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="5f286-159">No</span><span class="sxs-lookup"><span data-stu-id="5f286-159">No</span></span><br/></td>
<td><span data-ttu-id="5f286-160">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5f286-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="5f286-161">
<dt><span></span><span></span><strong></strong> Elementos</span><span class="sxs-lookup"><span data-stu-id="5f286-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="5f286-162"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="5f286-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="5f286-163">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f286-163">Child elements</span></span>



| <span data-ttu-id="5f286-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f286-164">Element</span></span>                                                                                           | <span data-ttu-id="5f286-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f286-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5f286-166">**Botón**</span><span class="sxs-lookup"><span data-stu-id="5f286-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="5f286-167">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5f286-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5f286-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="5f286-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="5f286-169">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5f286-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5f286-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="5f286-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="5f286-171">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="5f286-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="5f286-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5f286-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="5f286-173">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="5f286-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="5f286-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="5f286-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="5f286-175">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5f286-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5f286-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="5f286-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="5f286-177">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="5f286-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5f286-178">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5f286-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f286-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f286-179">Element</span></span></th>
<th><span data-ttu-id="5f286-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f286-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f286-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f286-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5f286-182"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f286-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5f286-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f286-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f286-184">Cuando está contenido en un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5f286-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="5f286-185">Este elemento solo se admite en el primer nivel y no debe tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="5f286-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f286-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f286-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5f286-187">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="5f286-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f286-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f286-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="5f286-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f286-189">Remarks</span></span>

<span data-ttu-id="5f286-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5f286-190">Optional.</span></span>

<span data-ttu-id="5f286-191">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**splitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="5f286-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="5f286-192">**DropDownGallery** admite los [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="5f286-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="5f286-193">En la captura de pantalla siguiente se muestra el control [Galería desplegable](windowsribbon-controls-dropdowngallery.md) de la cinta de opciones de Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f286-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de Galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="5f286-195">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5f286-195">Examples</span></span>

<span data-ttu-id="5f286-196">En el ejemplo siguiente se muestra el marcado básico para **DropDownGallery**.</span><span class="sxs-lookup"><span data-stu-id="5f286-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="5f286-197">En esta sección de código se muestran las declaraciones de comandos de **DropDownGallery** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="5f286-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="5f286-198">En esta sección de código se muestran las declaraciones de control de **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="5f286-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5f286-199">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5f286-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="5f286-200">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f286-200">Minimum supported system</span></span><br/> | <span data-ttu-id="5f286-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f286-201">Windows 7</span></span> |
| <span data-ttu-id="5f286-202">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f286-202">Can be empty</span></span>                        | <span data-ttu-id="5f286-203">No</span><span class="sxs-lookup"><span data-stu-id="5f286-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="5f286-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f286-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f286-205">**Control Galería desplegable**</span><span class="sxs-lookup"><span data-stu-id="5f286-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="5f286-206">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="5f286-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="5f286-207">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="5f286-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="5f286-208">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="5f286-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 


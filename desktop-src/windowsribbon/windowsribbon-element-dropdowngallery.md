---
title: Elemento DropDownGallery
description: Representa un control Drop-Down galería con un menú basado en la galería.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443426"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="aa266-104">Elemento DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="aa266-104">DropDownGallery element</span></span>

<span data-ttu-id="aa266-105">Representa un [control Galería desplegable con](windowsribbon-controls-dropdowngallery.md) un menú basado en la galería.</span><span class="sxs-lookup"><span data-stu-id="aa266-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="aa266-106">Uso</span><span class="sxs-lookup"><span data-stu-id="aa266-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="aa266-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa266-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa266-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="aa266-108">Attribute</span></span></th>
<th><span data-ttu-id="aa266-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa266-109">Type</span></span></th>
<th><span data-ttu-id="aa266-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="aa266-110">Required</span></span></th>
<th><span data-ttu-id="aa266-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa266-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa266-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa266-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="aa266-114">No</span><span class="sxs-lookup"><span data-stu-id="aa266-114">No</span></span><br/></td>
<td><span data-ttu-id="aa266-115">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="aa266-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="aa266-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="aa266-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="aa266-117">Cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="aa266-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="aa266-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="aa266-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="aa266-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="aa266-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa266-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="aa266-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="aa266-122">No</span><span class="sxs-lookup"><span data-stu-id="aa266-122">No</span></span><br/></td>
<td><span data-ttu-id="aa266-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aa266-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="aa266-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="aa266-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="aa266-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="aa266-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="aa266-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="aa266-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="aa266-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="aa266-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa266-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="aa266-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="aa266-130">No</span><span class="sxs-lookup"><span data-stu-id="aa266-130">No</span></span><br/></td>
<td><span data-ttu-id="aa266-131">Determina si el recurso de imagen grande o pequeño del comando se muestra en el control de la galería.</span><span class="sxs-lookup"><span data-stu-id="aa266-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa266-132">Solo se aplica a galerías donde el valor del atributo <em>Type</em> es igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="aa266-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="aa266-133">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="aa266-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="aa266-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="aa266-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="aa266-135">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="aa266-135">Default.</span></span> <br/> </dd> <span data-ttu-id="aa266-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="aa266-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa266-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="aa266-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="aa266-139">No</span><span class="sxs-lookup"><span data-stu-id="aa266-139">No</span></span><br/></td>
<td><span data-ttu-id="aa266-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="aa266-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="aa266-141">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="aa266-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa266-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="aa266-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="aa266-144">No</span><span class="sxs-lookup"><span data-stu-id="aa266-144">No</span></span><br/></td>
<td><span data-ttu-id="aa266-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="aa266-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="aa266-146">El valor predeterminado es -1.</span><span class="sxs-lookup"><span data-stu-id="aa266-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa266-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="aa266-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="aa266-149">No</span><span class="sxs-lookup"><span data-stu-id="aa266-149">No</span></span><br/></td>
<td><span data-ttu-id="aa266-150">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="aa266-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="aa266-151">
<dt><span></span><span></span><strong></strong> (Inferior)</span><span class="sxs-lookup"><span data-stu-id="aa266-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-152"><dt><span></span><span></span><strong></strong> (Ocultar)</span><span class="sxs-lookup"><span data-stu-id="aa266-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-153"><dt><span></span><span></span><strong></strong> (Izquierda)</span><span class="sxs-lookup"><span data-stu-id="aa266-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-154"><dt><span></span><span></span><strong></strong> (Superposición)</span><span class="sxs-lookup"><span data-stu-id="aa266-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-155"><dt><span></span><span></span><strong></strong> (Derecha)</span><span class="sxs-lookup"><span data-stu-id="aa266-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-156"><dt><span></span><span></span><strong></strong> (Superior)</span><span class="sxs-lookup"><span data-stu-id="aa266-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa266-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="aa266-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="aa266-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa266-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="aa266-159">No</span><span class="sxs-lookup"><span data-stu-id="aa266-159">No</span></span><br/></td>
<td><span data-ttu-id="aa266-160">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="aa266-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="aa266-161">
<dt><span></span><span></span><strong></strong> (Elementos)</span><span class="sxs-lookup"><span data-stu-id="aa266-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="aa266-162"><dt><span></span><span></span><strong></strong> (Comandos)</span><span class="sxs-lookup"><span data-stu-id="aa266-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="aa266-163">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa266-163">Child elements</span></span>



| <span data-ttu-id="aa266-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa266-164">Element</span></span>                                                                                           | <span data-ttu-id="aa266-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa266-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="aa266-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="aa266-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="aa266-167">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="aa266-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="aa266-168">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="aa266-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="aa266-169">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="aa266-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="aa266-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="aa266-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="aa266-171">Debe producirse exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="aa266-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="aa266-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="aa266-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="aa266-173">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="aa266-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="aa266-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="aa266-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="aa266-175">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="aa266-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="aa266-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="aa266-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="aa266-177">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="aa266-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="aa266-178">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="aa266-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa266-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa266-179">Element</span></span></th>
<th><span data-ttu-id="aa266-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa266-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa266-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa266-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="aa266-182"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa266-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="aa266-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa266-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="aa266-184">Cuando se encuentra en un <a href="windowsribbon-element-applicationmenu.md"><strong>elemento ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aa266-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="aa266-185">Este elemento solo se admite en el primer nivel y no debe tener ningún elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="aa266-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa266-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa266-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="aa266-187">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="aa266-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa266-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa266-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="aa266-189">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa266-189">Remarks</span></span>

<span data-ttu-id="aa266-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aa266-190">Optional.</span></span>

<span data-ttu-id="aa266-191">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton.**](windowsribbon-element-splitbutton.md)</span><span class="sxs-lookup"><span data-stu-id="aa266-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="aa266-192">**DropDownGallery admite los** [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="aa266-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="aa266-193">En la siguiente captura de pantalla se muestra [el](windowsribbon-controls-dropdowngallery.md) control Galería desplegable de la cinta Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa266-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de pantalla de un control de galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="aa266-195">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aa266-195">Examples</span></span>

<span data-ttu-id="aa266-196">En el ejemplo siguiente se muestra el marcado básico para **DropDownGallery**.</span><span class="sxs-lookup"><span data-stu-id="aa266-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="aa266-197">En esta sección de código se muestran las declaraciones **DropDownGallery** Command, con un grupo asociado que actúa como contenedor primario para el **elemento DropDownGallery.** [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="aa266-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


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



<span data-ttu-id="aa266-198">En esta sección de código se muestran las declaraciones de control **DropDownGallery.**</span><span class="sxs-lookup"><span data-stu-id="aa266-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="aa266-199">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="aa266-199">Element information</span></span>

* <span data-ttu-id="aa266-200">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa266-200">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="aa266-201">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="aa266-201">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="aa266-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa266-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa266-203">**Control galería desplegable**</span><span class="sxs-lookup"><span data-stu-id="aa266-203">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="aa266-204">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="aa266-204">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="aa266-205">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="aa266-205">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="aa266-206">Ejemplo de galería</span><span class="sxs-lookup"><span data-stu-id="aa266-206">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 


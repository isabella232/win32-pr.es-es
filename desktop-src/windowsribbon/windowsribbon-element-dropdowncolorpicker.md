---
title: Elemento DropDownColorPicker
description: Representa un Pickercontrol de color Drop-Down que, cuando se hace clic en él, muestra una paleta de muestras de color.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103786028"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="224c8-104">Elemento DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="224c8-104">DropDownColorPicker element</span></span>

<span data-ttu-id="224c8-105">Representa un control de [selector de colores desplegable](windowsribbon-controls-dropdowncolorpicker.md)que, cuando se hace clic en él, muestra una paleta de muestras de color.</span><span class="sxs-lookup"><span data-stu-id="224c8-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="224c8-106">Uso</span><span class="sxs-lookup"><span data-stu-id="224c8-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="224c8-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="224c8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="224c8-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="224c8-108">Attribute</span></span></th>
<th><span data-ttu-id="224c8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="224c8-109">Type</span></span></th>
<th><span data-ttu-id="224c8-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="224c8-110">Required</span></span></th>
<th><span data-ttu-id="224c8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="224c8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="224c8-112"><strong>Chip</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="224c8-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="224c8-114">No</span><span class="sxs-lookup"><span data-stu-id="224c8-114">No</span></span><br/></td>
<td><span data-ttu-id="224c8-115">Tamaño de cada chip o muestra de color.</span><span class="sxs-lookup"><span data-stu-id="224c8-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="224c8-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="224c8-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="224c8-117">
<dt><span></span><span></span><strong></strong> Pequeño</span><span class="sxs-lookup"><span data-stu-id="224c8-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-118">Cada chip de color es un cuadrado de 11x11 píxeles.</span><span class="sxs-lookup"><span data-stu-id="224c8-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="224c8-119"><dt><span></span><span></span><strong></strong> Medio</span><span class="sxs-lookup"><span data-stu-id="224c8-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-120">Cada chip de color es un cuadrado de 16x16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="224c8-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="224c8-121"><dt><span></span><span></span><strong></strong> Amplíe</span><span class="sxs-lookup"><span data-stu-id="224c8-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-122">Cada chip de color es un cuadrado de 24x24 píxeles.</span><span class="sxs-lookup"><span data-stu-id="224c8-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224c8-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="224c8-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="224c8-125">No</span><span class="sxs-lookup"><span data-stu-id="224c8-125">No</span></span><br/></td>
<td><span data-ttu-id="224c8-126">Plantillas de diseño que especifican el tipo de <a href="windowsribbon-controls-dropdowncolorpicker.md">selector de colores desplegable</a>.</span><span class="sxs-lookup"><span data-stu-id="224c8-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="224c8-127">Restringido a uno de los valores siguientes (si no se declaran atributos opcionales relacionados con un <em>ColorTemplate</em> , se muestra la vista predeterminada):</span><span class="sxs-lookup"><span data-stu-id="224c8-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="224c8-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="224c8-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-129">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="224c8-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="224c8-130">Establecer el atributo <em>ColorTemplate</em> en <code>ThemeColors</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="224c8-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="224c8-131">Delimitador de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="224c8-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="224c8-132">De forma predeterminada, se muestra el botón color <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="224c8-133">Cuadrícula del muestrario de <strong>colores del tema</strong> de Windows.</span><span class="sxs-lookup"><span data-stu-id="224c8-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="224c8-134">Cuadrícula de muestrario de <strong>colores estándar</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="224c8-135">La cuadrícula del muestrario de <strong>colores recientes</strong> es opcional.</span><span class="sxs-lookup"><span data-stu-id="224c8-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="224c8-136">Selector de cuadro de diálogo <strong>más colores</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="224c8-137"><strong>No</strong> se muestra el botón color de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="224c8-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="224c8-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="224c8-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="224c8-139">Establecer el atributo <em>ColorTemplate</em> en <code>StandardColors</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="224c8-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="224c8-140">Delimitador de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="224c8-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="224c8-141">De forma predeterminada, se muestra el botón color <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="224c8-142">Cuadrícula de muestrario de <strong>colores estándar</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="224c8-143">Selector de cuadro de diálogo <strong>más colores</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="224c8-144"><strong>No</strong> se muestra el botón color de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="224c8-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="224c8-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="224c8-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="224c8-146">Establecer el atributo <em>ColorTemplate</em> en <code>HighlightColors</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="224c8-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="224c8-147">Delimitador de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="224c8-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="224c8-148">Cuadrícula del muestrario de <strong>colores estándar</strong> sin encabezado.</span><span class="sxs-lookup"><span data-stu-id="224c8-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="224c8-149"><strong>No</strong> se muestra el botón color de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="224c8-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224c8-150"><strong>Columnas</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="224c8-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="224c8-152">No</span><span class="sxs-lookup"><span data-stu-id="224c8-152">No</span></span><br/></td>
<td><span data-ttu-id="224c8-153">El número de columnas de chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="224c8-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="224c8-154">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="224c8-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-155">Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="224c8-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224c8-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-157">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="224c8-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="224c8-158">No</span><span class="sxs-lookup"><span data-stu-id="224c8-158">No</span></span><br/></td>
<td><span data-ttu-id="224c8-159">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="224c8-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="224c8-160">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="224c8-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-161">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="224c8-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="224c8-162">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="224c8-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="224c8-163">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="224c8-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224c8-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="224c8-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="224c8-166">No</span><span class="sxs-lookup"><span data-stu-id="224c8-166">No</span></span><br/></td>
<td><span data-ttu-id="224c8-167">Muestra u oculta el botón color <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="224c8-168">Solo es válido <code>StandardColors</code> cuando <code>ThemeColors</code> se especifica o para el atributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="224c8-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="224c8-169">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="224c8-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="224c8-170">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="224c8-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="224c8-171"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="224c8-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224c8-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="224c8-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="224c8-174">No</span><span class="sxs-lookup"><span data-stu-id="224c8-174">No</span></span><br/></td>
<td><span data-ttu-id="224c8-175">Muestra u oculta el botón <strong>sin color</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="224c8-176">Válido para todos los valores de <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="224c8-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="224c8-177">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="224c8-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="224c8-178">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="224c8-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="224c8-179"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="224c8-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224c8-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="224c8-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="224c8-182">No</span><span class="sxs-lookup"><span data-stu-id="224c8-182">No</span></span><br/></td>
<td><span data-ttu-id="224c8-183">El número de filas del chip de color (o muestra) en el área de <strong>colores recientes</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="224c8-184">Solo es válido cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="224c8-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="224c8-185">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="224c8-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-186">Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="224c8-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224c8-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="224c8-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="224c8-189">No</span><span class="sxs-lookup"><span data-stu-id="224c8-189">No</span></span><br/></td>
<td><span data-ttu-id="224c8-190">El número de filas del chip de color (o muestra) en el área <strong>colores estándar</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="224c8-191">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="224c8-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-192">Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="224c8-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224c8-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="224c8-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="224c8-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="224c8-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="224c8-195">No</span><span class="sxs-lookup"><span data-stu-id="224c8-195">No</span></span><br/></td>
<td><span data-ttu-id="224c8-196">El número de filas del chip de color (o muestra) en el área <strong>colores del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="224c8-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="224c8-197">Solo es válido cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="224c8-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="224c8-198">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="224c8-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="224c8-199">Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="224c8-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="224c8-200">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="224c8-200">Child elements</span></span>

<span data-ttu-id="224c8-201">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="224c8-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="224c8-202">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="224c8-202">Parent elements</span></span>



| <span data-ttu-id="224c8-203">Elemento</span><span class="sxs-lookup"><span data-stu-id="224c8-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="224c8-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="224c8-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="224c8-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="224c8-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="224c8-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="224c8-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="224c8-207">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="224c8-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="224c8-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="224c8-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="224c8-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="224c8-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="224c8-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="224c8-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="224c8-211">Observaciones</span><span class="sxs-lookup"><span data-stu-id="224c8-211">Remarks</span></span>

<span data-ttu-id="224c8-212">Opcional.</span><span class="sxs-lookup"><span data-stu-id="224c8-212">Optional.</span></span>

<span data-ttu-id="224c8-213">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="224c8-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="224c8-214">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="224c8-214">Examples</span></span>

<span data-ttu-id="224c8-215">En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="224c8-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="224c8-216">En esta sección de código se muestran las declaraciones de comando para tres elementos **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="224c8-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="224c8-217">En esta sección de código se muestran los tres tipos de declaraciones de control de **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="224c8-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="224c8-218">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="224c8-218">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="224c8-219">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="224c8-219">Minimum supported system</span></span><br/> | <span data-ttu-id="224c8-220">Windows 7</span><span class="sxs-lookup"><span data-stu-id="224c8-220">Windows 7</span></span> |
| <span data-ttu-id="224c8-221">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="224c8-221">Can be empty</span></span>                        | <span data-ttu-id="224c8-222">Sí</span><span class="sxs-lookup"><span data-stu-id="224c8-222">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="224c8-223">Consulte también</span><span class="sxs-lookup"><span data-stu-id="224c8-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224c8-224">Control de selector de colores desplegables</span><span class="sxs-lookup"><span data-stu-id="224c8-224">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="224c8-225">Ejemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="224c8-225">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 






---
title: Elemento DropDownColorPicker
description: Representa un Drop-Down selector de color que cuando se hace clic muestra una paleta de muestras de color.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442906"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="d20b7-104">Elemento DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="d20b7-104">DropDownColorPicker element</span></span>

<span data-ttu-id="d20b7-105">Representa una [lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md)control que cuando se hace clic muestra una paleta de muestras de color.</span><span class="sxs-lookup"><span data-stu-id="d20b7-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="d20b7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d20b7-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="d20b7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d20b7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d20b7-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d20b7-108">Attribute</span></span></th>
<th><span data-ttu-id="d20b7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d20b7-109">Type</span></span></th>
<th><span data-ttu-id="d20b7-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="d20b7-110">Required</span></span></th>
<th><span data-ttu-id="d20b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d20b7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d20b7-112"><strong>ChipSize</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d20b7-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d20b7-114">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-114">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-115">Tamaño de cada chip de color o muestra.</span><span class="sxs-lookup"><span data-stu-id="d20b7-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="d20b7-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d20b7-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d20b7-117">
<dt><span></span><span></span><strong></strong> (Pequeño)</span><span class="sxs-lookup"><span data-stu-id="d20b7-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-118">Cada chip de color es un cuadrado de 11 x 11 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d20b7-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d20b7-119"><dt><span></span><span></span><strong></strong> (Medio)</span><span class="sxs-lookup"><span data-stu-id="d20b7-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-120">Cada chip de color es un cuadrado de 16 x 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d20b7-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d20b7-121"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="d20b7-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-122">Cada chip de color es un cuadrado de 24 x 24 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d20b7-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d20b7-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d20b7-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="d20b7-125">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-125">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-126">Plantillas de diseño que especifican el tipo <a href="windowsribbon-controls-dropdowncolorpicker.md">de lista desplegable Selector de colores</a>.</span><span class="sxs-lookup"><span data-stu-id="d20b7-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="d20b7-127">Se restringe a uno de los siguientes valores (si no se declara ningún atributo opcional relacionado con una <em>colorTemplate,</em> se muestra la vista predeterminada):</span><span class="sxs-lookup"><span data-stu-id="d20b7-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="d20b7-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="d20b7-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-129">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="d20b7-130">Establecer el <em>atributo ColorTemplate</em> en <code>ThemeColors</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="d20b7-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d20b7-131">Delimitador SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d20b7-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d20b7-132"><strong>El</strong> botón de color automático se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d20b7-133">Cuadrícula <strong>de muestra de colores</strong> de tema de Windows.</span><span class="sxs-lookup"><span data-stu-id="d20b7-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d20b7-134"><strong>Cuadrícula de muestra</strong> de colores estándar.</span><span class="sxs-lookup"><span data-stu-id="d20b7-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d20b7-135"><strong>La cuadrícula de</strong> muestra Colores recientes es opcional.</span><span class="sxs-lookup"><span data-stu-id="d20b7-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="d20b7-136"><strong>Iniciador del cuadro</strong> de diálogo Más colores.</span><span class="sxs-lookup"><span data-stu-id="d20b7-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d20b7-137"><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d20b7-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="d20b7-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="d20b7-139">Establecer el <em>atributo ColorTemplate</em> en <code>StandardColors</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="d20b7-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d20b7-140">Delimitador SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d20b7-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d20b7-141"><strong>El</strong> botón de color automático se muestra de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d20b7-142"><strong>Cuadrícula de muestra</strong> de colores estándar.</span><span class="sxs-lookup"><span data-stu-id="d20b7-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d20b7-143"><strong>Iniciador del cuadro</strong> de diálogo Más colores.</span><span class="sxs-lookup"><span data-stu-id="d20b7-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d20b7-144"><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d20b7-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="d20b7-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="d20b7-146">Establecer el <em>atributo ColorTemplate</em> en <code>HighlightColors</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="d20b7-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d20b7-147">Delimitador SplitButton.</span><span class="sxs-lookup"><span data-stu-id="d20b7-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d20b7-148"><strong>Cuadrícula de muestra</strong> de colores estándar sin encabezado.</span><span class="sxs-lookup"><span data-stu-id="d20b7-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="d20b7-149"><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d20b7-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d20b7-150"><strong>Columnas</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d20b7-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d20b7-152">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-152">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-153">Número de columnas de chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="d20b7-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="d20b7-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d20b7-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-155">Cualquier valor entero positivo entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="d20b7-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d20b7-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-157">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="d20b7-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d20b7-158">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-158">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-159">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d20b7-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d20b7-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="d20b7-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-161">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="d20b7-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d20b7-162">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="d20b7-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d20b7-163">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d20b7-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d20b7-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="d20b7-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="d20b7-166">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-166">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-167">Muestra (u oculta) el <strong>botón Color</strong> automático.</span><span class="sxs-lookup"><span data-stu-id="d20b7-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="d20b7-168">Válido solo cuando <code>StandardColors</code> se especifica o para el atributo <code>ThemeColors</code> <em>ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="d20b7-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="d20b7-169">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="d20b7-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d20b7-170">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d20b7-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d20b7-171"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d20b7-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d20b7-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="d20b7-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="d20b7-174">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-174">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-175">Muestra (u oculta) el <strong>botón Sin</strong> color.</span><span class="sxs-lookup"><span data-stu-id="d20b7-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="d20b7-176">Válido para todos <em>los valores de ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="d20b7-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="d20b7-177">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="d20b7-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d20b7-178">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d20b7-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d20b7-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d20b7-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d20b7-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d20b7-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d20b7-182">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-182">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-183">Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> recientes.</span><span class="sxs-lookup"><span data-stu-id="d20b7-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="d20b7-184">Válido solo cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="d20b7-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d20b7-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d20b7-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-186">Cualquier valor entero positivo entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="d20b7-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d20b7-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d20b7-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d20b7-189">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-189">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-190">Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> estándar.</span><span class="sxs-lookup"><span data-stu-id="d20b7-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="d20b7-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d20b7-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-192">Cualquier valor entero positivo entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="d20b7-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d20b7-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d20b7-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d20b7-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d20b7-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d20b7-195">No</span><span class="sxs-lookup"><span data-stu-id="d20b7-195">No</span></span><br/></td>
<td><span data-ttu-id="d20b7-196">Número de filas de chip de color (o muestra) en el área <strong>Colores del</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="d20b7-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="d20b7-197">Válido solo cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="d20b7-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d20b7-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d20b7-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d20b7-199">Cualquier valor entero positivo entre 1 y 256, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="d20b7-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d20b7-200">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d20b7-200">Child elements</span></span>

<span data-ttu-id="d20b7-201">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d20b7-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d20b7-202">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d20b7-202">Parent elements</span></span>



| <span data-ttu-id="d20b7-203">Elemento</span><span class="sxs-lookup"><span data-stu-id="d20b7-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d20b7-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d20b7-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="d20b7-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d20b7-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="d20b7-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d20b7-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="d20b7-207">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="d20b7-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="d20b7-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d20b7-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="d20b7-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d20b7-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="d20b7-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d20b7-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d20b7-211">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d20b7-211">Remarks</span></span>

<span data-ttu-id="d20b7-212">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d20b7-212">Optional.</span></span>

<span data-ttu-id="d20b7-213">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md) [**o SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="d20b7-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d20b7-214">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d20b7-214">Examples</span></span>

<span data-ttu-id="d20b7-215">En el ejemplo siguiente se muestra el marcado básico para los tres tipos de lista [Selector de colores](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="d20b7-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="d20b7-216">En esta sección de código se muestran las declaraciones command para tres **elementos DropDownColorPicker.**</span><span class="sxs-lookup"><span data-stu-id="d20b7-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


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



<span data-ttu-id="d20b7-217">En esta sección de código se muestran los tres tipos de declaraciones de control **DropDownColorPicker.**</span><span class="sxs-lookup"><span data-stu-id="d20b7-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d20b7-218">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d20b7-218">Element information</span></span>

* <span data-ttu-id="d20b7-219">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d20b7-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d20b7-220">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="d20b7-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="d20b7-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="d20b7-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d20b7-222">Control de Selector de colores desplegable</span><span class="sxs-lookup"><span data-stu-id="d20b7-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="d20b7-223">Ejemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="d20b7-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 






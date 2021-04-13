---
title: Elemento FontControl
description: Representa un control de fuente, que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl cinta de opciones de Windows
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "104420512"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="40e68-104">Elemento FontControl</span><span class="sxs-lookup"><span data-stu-id="40e68-104">FontControl element</span></span>

<span data-ttu-id="40e68-105">Representa un [control de fuente](windowsribbon-controls-fontcontrol.md), que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.</span><span class="sxs-lookup"><span data-stu-id="40e68-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="40e68-106">Uso</span><span class="sxs-lookup"><span data-stu-id="40e68-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="40e68-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="40e68-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40e68-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="40e68-108">Attribute</span></span></th>
<th><span data-ttu-id="40e68-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="40e68-109">Type</span></span></th>
<th><span data-ttu-id="40e68-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="40e68-110">Required</span></span></th>
<th><span data-ttu-id="40e68-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e68-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40e68-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="40e68-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="40e68-114">No</span><span class="sxs-lookup"><span data-stu-id="40e68-114">No</span></span><br/></td>
<td><span data-ttu-id="40e68-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40e68-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="40e68-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="40e68-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="40e68-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="40e68-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="40e68-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="40e68-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="40e68-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40e68-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="40e68-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="40e68-122">No</span><span class="sxs-lookup"><span data-stu-id="40e68-122">No</span></span><br/></td>
<td><span data-ttu-id="40e68-123">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="40e68-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="40e68-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="40e68-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e68-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="40e68-126">Establecer el atributo <em>FontType</em> en <code>FontOnly</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="40e68-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="40e68-127">Cuadro combinado de <strong>familia de fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="40e68-128">Cuadro combinado de <strong>tamaño de fuente</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="40e68-129">Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-130">Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="40e68-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="40e68-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="40e68-132">Establecer el atributo <em>FontType</em> en <code>FontWithColor</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="40e68-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="40e68-133">Cuadro combinado de <strong>familia de fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="40e68-134">Cuadro combinado de <strong>tamaño de fuente</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="40e68-135"><strong>Aumentar</strong> el tamaño de la fuente y <strong>reducir</strong> los botones de incremento y decremento de fuente.</span><span class="sxs-lookup"><span data-stu-id="40e68-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="40e68-136">Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-137">Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="40e68-138">Selector de colores de <strong>color de texto</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="40e68-139">Selector de colores de <strong>color de resaltado de texto</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-140">Este control está oculto de forma predeterminada, pero se puede mostrar estableciendo el atributo <em>IsHighlightButtonVisible</em> en <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="40e68-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="40e68-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="40e68-142">Establecer el atributo <em>FontType</em> en <code>RichFont</code> habilita la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="40e68-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="40e68-143">Cuadro combinado de <strong>familia de fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="40e68-144">Cuadro combinado de <strong>tamaño de fuente</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="40e68-145"><strong>Aumentar</strong> el tamaño de la fuente y <strong>reducir</strong> los botones de incremento y decremento de fuente.</span><span class="sxs-lookup"><span data-stu-id="40e68-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="40e68-146">Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-147">Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada y no se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="40e68-148">Selector de colores de <strong>color de texto</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="40e68-149">Selector de colores de <strong>color de resaltado de texto</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-150">Este control se muestra de forma predeterminada y no se puede ocultar estableciendo el atributo <em>IsHighlightButtonVisible</em> en <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="40e68-151">Botones <strong>de alternancia de subíndice y</strong> <strong>superíndice</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40e68-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-154">No</span><span class="sxs-lookup"><span data-stu-id="40e68-154">No</span></span><br/></td>
<td><span data-ttu-id="40e68-155"><strong>Windows 8 y versiones más recientes</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="40e68-156">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="40e68-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-157">Los botones de aumentar y reducir nunca se muestran en <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40e68-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="40e68-158">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-159">Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="40e68-160"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-161">Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40e68-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-164">No</span><span class="sxs-lookup"><span data-stu-id="40e68-164">No</span></span><br/></td>
<td><span data-ttu-id="40e68-165">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="40e68-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-166">El resaltado de color solo está disponible desde un <strong>FontControl</strong> cuando el valor del atributo <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="40e68-167">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-168">Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="40e68-169">Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="40e68-170"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-171">Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="40e68-172">Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40e68-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-175">No</span><span class="sxs-lookup"><span data-stu-id="40e68-175">No</span></span><br/></td>
<td><span data-ttu-id="40e68-176">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="40e68-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="40e68-177">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-178">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e68-178">Default.</span></span> <br/> </dd> <span data-ttu-id="40e68-179"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-180">Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40e68-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-183">No</span><span class="sxs-lookup"><span data-stu-id="40e68-183">No</span></span><br/></td>
<td><span data-ttu-id="40e68-184">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="40e68-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="40e68-185">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-186">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e68-186">Default.</span></span> <br/> </dd> <span data-ttu-id="40e68-187"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-188">Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40e68-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="40e68-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="40e68-191">No</span><span class="sxs-lookup"><span data-stu-id="40e68-191">No</span></span><br/></td>
<td><span data-ttu-id="40e68-192">Tamaño de punto máximo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="40e68-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="40e68-193">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="40e68-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-194">Un valor entero entre 1 y 9999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="40e68-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="40e68-195">El valor predeterminado es <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="40e68-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40e68-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="40e68-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="40e68-198">No</span><span class="sxs-lookup"><span data-stu-id="40e68-198">No</span></span><br/></td>
<td><span data-ttu-id="40e68-199">Tamaño de punto mínimo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="40e68-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="40e68-200">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="40e68-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-201">Un valor entero entre 1 y 9999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="40e68-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="40e68-202">El valor predeterminado es <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="40e68-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40e68-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-205">No</span><span class="sxs-lookup"><span data-stu-id="40e68-205">No</span></span><br/></td>
<td><span data-ttu-id="40e68-206">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="40e68-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="40e68-207">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-208">Solo muestra las fuentes TrueType y OpenType.</span><span class="sxs-lookup"><span data-stu-id="40e68-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="40e68-209"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-210">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e68-210">Default.</span></span> <span data-ttu-id="40e68-211">No se aplica ninguna restricción en el tipo de fuentes que se muestran.</span><span class="sxs-lookup"><span data-stu-id="40e68-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40e68-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="40e68-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="40e68-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="40e68-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="40e68-214">No</span><span class="sxs-lookup"><span data-stu-id="40e68-214">No</span></span><br/></td>
<td><span data-ttu-id="40e68-215">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="40e68-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-216">Las fuentes verticales van precedidas de un símbolo @ en la lista de <strong>familias de fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="40e68-217">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="40e68-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-218">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40e68-218">Default.</span></span> <span data-ttu-id="40e68-219">Muestra las fuentes verticales que se establecen para <strong>mostrarse</strong> en el panel de control <strong>fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="40e68-220"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="40e68-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="40e68-221">Permite que una aplicación que no admite texto vertical oculte ninguna fuente vertical que esté configurada para <strong>mostrarse</strong> en el panel de control <strong>fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40e68-222">En Windows Vista, el panel de control <strong>fuentes</strong> no ofrece la funcionalidad <strong>Mostrar</strong> u <strong>ocultar</strong> .</span><span class="sxs-lookup"><span data-stu-id="40e68-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="40e68-223">En este caso, el atributo <em>ShowVerticalFonts</em> debe establecerse en <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="40e68-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="40e68-224">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40e68-224">Child elements</span></span>

<span data-ttu-id="40e68-225">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="40e68-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="40e68-226">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="40e68-226">Parent elements</span></span>



| <span data-ttu-id="40e68-227">Elemento</span><span class="sxs-lookup"><span data-stu-id="40e68-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="40e68-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="40e68-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="40e68-229">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="40e68-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="40e68-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="40e68-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="40e68-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40e68-231">Remarks</span></span>

<span data-ttu-id="40e68-232">Opcional.</span><span class="sxs-lookup"><span data-stu-id="40e68-232">Optional.</span></span>

<span data-ttu-id="40e68-233">Puede aparecer como máximo una vez por cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)o [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="40e68-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="40e68-234">Cualquier atributo de comando **FontControl** declarado en el marcado, como [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), se reemplaza por los atributos de los controles individuales que componen el **FontControl**.</span><span class="sxs-lookup"><span data-stu-id="40e68-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="40e68-235">Cualquier intento de seleccionar una muestra de color del selector de colores de un [control de fuente](windowsribbon-controls-fontcontrol.md) puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.</span><span class="sxs-lookup"><span data-stu-id="40e68-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="40e68-236">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="40e68-236">Examples</span></span>

<span data-ttu-id="40e68-237">En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [control de fuente](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="40e68-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="40e68-238">En esta sección de código se muestran las declaraciones de comandos de **FontControl** , cada una con una declaración de contenedor de [**Grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="40e68-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="40e68-239">En esta sección de código se muestran las declaraciones de control de **FontControl** en las que cada **FontControl** y [**Grupo**](windowsribbon-element-group.md) se declaran en una sola pestaña.</span><span class="sxs-lookup"><span data-stu-id="40e68-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="40e68-240">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="40e68-240">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="40e68-241">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e68-241">Minimum supported system</span></span><br/> | <span data-ttu-id="40e68-242">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40e68-242">Windows 7</span></span> |
| <span data-ttu-id="40e68-243">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40e68-243">Can be empty</span></span>                        | <span data-ttu-id="40e68-244">Sí</span><span class="sxs-lookup"><span data-stu-id="40e68-244">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="40e68-245">Consulte también</span><span class="sxs-lookup"><span data-stu-id="40e68-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e68-246">Control de control de fuentes</span><span class="sxs-lookup"><span data-stu-id="40e68-246">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="40e68-247">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="40e68-247">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="40e68-248">Ejemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="40e68-248">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 






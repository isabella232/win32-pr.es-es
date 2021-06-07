---
title: Elemento FontControl
description: Representa un control de fuente, que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Elemento FontControl de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443406"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="9c19f-104">Elemento FontControl</span><span class="sxs-lookup"><span data-stu-id="9c19f-104">FontControl element</span></span>

<span data-ttu-id="9c19f-105">Representa un [control de fuente](windowsribbon-controls-fontcontrol.md), que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c19f-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="9c19f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="9c19f-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="9c19f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c19f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c19f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="9c19f-108">Attribute</span></span></th>
<th><span data-ttu-id="9c19f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c19f-109">Type</span></span></th>
<th><span data-ttu-id="9c19f-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="9c19f-110">Required</span></span></th>
<th><span data-ttu-id="9c19f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c19f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c19f-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="9c19f-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="9c19f-114">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-114">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9c19f-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="9c19f-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="9c19f-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9c19f-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="9c19f-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="9c19f-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="9c19f-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9c19f-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c19f-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="9c19f-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="9c19f-122">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-122">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-123">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9c19f-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="9c19f-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="9c19f-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c19f-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="9c19f-126">Establecer el <em>atributo FontType</em> en <code>FontOnly</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c19f-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="9c19f-127"><strong>Cuadro combinado familia</strong> de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c19f-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="9c19f-128"><strong>Cuadro combinado Tamaño de</strong> fuente.</span><span class="sxs-lookup"><span data-stu-id="9c19f-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="9c19f-129"><strong>Botones</strong>de <strong>alternancia</strong>Negrita, <strong>Cursiva,</strong> <strong>Subrayado y Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-130">Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="9c19f-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="9c19f-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="9c19f-132">Establecer el <em>atributo FontType</em> en <code>FontWithColor</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c19f-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="9c19f-133"><strong>Cuadro combinado familia</strong> de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c19f-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="9c19f-134"><strong>Cuadro combinado tamaño de</strong> fuente.</span><span class="sxs-lookup"><span data-stu-id="9c19f-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="9c19f-135"><strong>Aumentar la fuente y</strong> <strong>reducir el tamaño</strong> de fuente de los botones de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="9c19f-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="9c19f-136"><strong>Botones</strong>de <strong>alternancia</strong>Negrita, <strong>Cursiva,</strong> <strong>Subrayado y Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-137">Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="9c19f-138"><strong>Selector de color</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="9c19f-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="9c19f-139"><strong>Selector de color de resaltado</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="9c19f-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-140">Este control está oculto de forma predeterminada, pero se puede mostrar estableciendo el <em>atributo IsHighlightButtonVisible</em> en <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="9c19f-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="9c19f-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="9c19f-142">Establecer el <em>atributo FontType</em> en <code>RichFont</code> habilita la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c19f-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="9c19f-143"><strong>Cuadro combinado familia</strong> de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c19f-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="9c19f-144"><strong>Cuadro combinado tamaño de</strong> fuente.</span><span class="sxs-lookup"><span data-stu-id="9c19f-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="9c19f-145"><strong>Aumentar la fuente y</strong> <strong>reducir el tamaño</strong> de fuente de los botones de incremento y decremento.</span><span class="sxs-lookup"><span data-stu-id="9c19f-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="9c19f-146"><strong>Botones</strong>de <strong>alternancia</strong>Negrita, <strong>Cursiva,</strong> <strong>Subrayado y Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-147">Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada y no se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="9c19f-148"><strong>Selector de color</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="9c19f-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="9c19f-149"><strong>Selector de color de resaltado</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="9c19f-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-150">Este control se muestra de forma predeterminada y no se puede ocultar estableciendo el <em>atributo IsHighlightButtonVisible</em> en <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="9c19f-151"><strong>Botones de</strong> <strong>alternancia de subíndice</strong> y superíndice.</span><span class="sxs-lookup"><span data-stu-id="9c19f-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c19f-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-154">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-154">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-155"><strong>Windows 8 y versiones más recientes</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="9c19f-156">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9c19f-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-157">Los botones Aumentar/Reducir nunca se muestran en <a href="windowsribbon-element-minitoolbar.md"><strong>minitoolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9c19f-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="9c19f-158">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-159">Valor predeterminado cuando el valor <em>de FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="9c19f-160"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-161">Valor predeterminado cuando el valor <em>de FontType</em> es igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c19f-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-164">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-164">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-165">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9c19f-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-166">El resaltado de color solo está disponible desde <strong>un FontControl</strong> cuando el valor del <em>atributo FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="9c19f-167">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-168">Valor predeterminado cuando el valor <em>de FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="9c19f-169">Válido solo cuando el valor <em>de FontType</em> es igual <code>FontWithColor</code> a o <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="9c19f-170"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-171">Valor predeterminado cuando el valor <em>de FontType</em> es igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="9c19f-172">Válido solo cuando el valor <em>de FontType</em> es igual <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c19f-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-175">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-175">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-176">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9c19f-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="9c19f-177">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-178">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c19f-178">Default.</span></span> <br/> </dd> <span data-ttu-id="9c19f-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-180">Válido solo cuando el valor <em>de FontType</em> es igual <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c19f-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-183">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-183">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-184">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9c19f-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="9c19f-185">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-186">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c19f-186">Default.</span></span> <br/> </dd> <span data-ttu-id="9c19f-187"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-188">Válido solo cuando el valor <em>de FontType</em> es igual <code>FontOnly</code> a o <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c19f-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="9c19f-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="9c19f-191">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-191">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-192">Tamaño máximo de punto que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="9c19f-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="9c19f-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="9c19f-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-194">Valor entero comprendido entre 1 y 9999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9c19f-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="9c19f-195">El valor predeterminado <strong>es 9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="9c19f-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c19f-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="9c19f-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="9c19f-198">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-198">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-199">Tamaño de punto mínimo que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="9c19f-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="9c19f-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="9c19f-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-201">Valor entero comprendido entre 1 y 9999, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9c19f-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="9c19f-202">El valor predeterminado <strong>es 1.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c19f-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-205">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-205">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-206">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9c19f-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="9c19f-207">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-208">Muestra solo las fuentes TrueType y OpenType.</span><span class="sxs-lookup"><span data-stu-id="9c19f-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="9c19f-209"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-210">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c19f-210">Default.</span></span> <span data-ttu-id="9c19f-211">No se coloca ninguna restricción en el tipo de fuentes que se muestra.</span><span class="sxs-lookup"><span data-stu-id="9c19f-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c19f-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="9c19f-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c19f-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="9c19f-214">No</span><span class="sxs-lookup"><span data-stu-id="9c19f-214">No</span></span><br/></td>
<td><span data-ttu-id="9c19f-215">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9c19f-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-216">Las fuentes verticales van precedidas de un símbolo @ en la <strong>lista Familia de</strong> fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c19f-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="9c19f-217">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="9c19f-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-218">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c19f-218">Default.</span></span> <span data-ttu-id="9c19f-219">Muestra las fuentes verticales establecidas en <strong>Mostrar en</strong> el panel de control <strong>Fuentes.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="9c19f-220"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="9c19f-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="9c19f-221">Permite que una aplicación que no admite texto vertical oculte las fuentes verticales establecidas en <strong>Mostrar</strong> en el panel de control <strong>Fuentes.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9c19f-222">En Windows Vista, el panel de control <strong>Fuentes</strong> no ofrece <strong>la funcionalidad Mostrar</strong> u <strong>ocultar.</strong></span><span class="sxs-lookup"><span data-stu-id="9c19f-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="9c19f-223">En este caso, el <em>atributo ShowVerticalFonts</em> debe establecerse en <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="9c19f-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9c19f-224">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c19f-224">Child elements</span></span>

<span data-ttu-id="9c19f-225">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9c19f-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9c19f-226">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9c19f-226">Parent elements</span></span>



| <span data-ttu-id="9c19f-227">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c19f-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="9c19f-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="9c19f-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="9c19f-229">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="9c19f-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="9c19f-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="9c19f-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="9c19f-231">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c19f-231">Remarks</span></span>

<span data-ttu-id="9c19f-232">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9c19f-232">Optional.</span></span>

<span data-ttu-id="9c19f-233">Puede producirse como máximo una vez para cada [**elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Group**](windowsribbon-element-group.md) [**o MenuGroup.**](windowsribbon-element-menugroup.md)</span><span class="sxs-lookup"><span data-stu-id="9c19f-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="9c19f-234">Los **atributos del comando FontControl** declarados en el marcado, como [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)se reemplazan por los atributos de los controles individuales que componen **FontControl**.</span><span class="sxs-lookup"><span data-stu-id="9c19f-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="9c19f-235">Cualquier intento de seleccionar una muestra de color del selector de colores de un [control de](windowsribbon-controls-fontcontrol.md) fuente puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.</span><span class="sxs-lookup"><span data-stu-id="9c19f-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="9c19f-236">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c19f-236">Examples</span></span>

<span data-ttu-id="9c19f-237">En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [Control de fuentes](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="9c19f-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="9c19f-238">En esta sección de código se muestran las declaraciones del comando **FontControl,** cada una con una declaración [**de contenedor**](windowsribbon-element-group.md) group.</span><span class="sxs-lookup"><span data-stu-id="9c19f-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


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



<span data-ttu-id="9c19f-239">En esta sección de código se muestran las **declaraciones de** control FontControl en las que cada **FontControl** y [**Group**](windowsribbon-element-group.md) se declaran en una sola pestaña.</span><span class="sxs-lookup"><span data-stu-id="9c19f-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="9c19f-240">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9c19f-240">Element information</span></span>

* <span data-ttu-id="9c19f-241">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c19f-241">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="9c19f-242">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="9c19f-242">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="9c19f-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c19f-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c19f-244">Control Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="9c19f-244">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="9c19f-245">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="9c19f-245">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="9c19f-246">Ejemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="9c19f-246">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 






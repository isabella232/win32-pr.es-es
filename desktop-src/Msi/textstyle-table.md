---
description: La tabla TextStyle muestra los distintos estilos de fuente que se usan en los controles que tienen texto.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabla de TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001286"
---
# <a name="textstyle-table"></a><span data-ttu-id="213dd-103">Tabla de TextStyle</span><span class="sxs-lookup"><span data-stu-id="213dd-103">TextStyle Table</span></span>

<span data-ttu-id="213dd-104">La tabla TextStyle muestra los distintos estilos de fuente que se usan en los controles que tienen texto.</span><span class="sxs-lookup"><span data-stu-id="213dd-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="213dd-105">La tabla TextStyle tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="213dd-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="213dd-106">Columna</span><span class="sxs-lookup"><span data-stu-id="213dd-106">Column</span></span>    | <span data-ttu-id="213dd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="213dd-107">Type</span></span>                               | <span data-ttu-id="213dd-108">Clave</span><span class="sxs-lookup"><span data-stu-id="213dd-108">Key</span></span> | <span data-ttu-id="213dd-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="213dd-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="213dd-110">Estilo]</span><span class="sxs-lookup"><span data-stu-id="213dd-110">TextStyle</span></span> | [<span data-ttu-id="213dd-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="213dd-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="213dd-112">Y</span><span class="sxs-lookup"><span data-stu-id="213dd-112">Y</span></span>   | <span data-ttu-id="213dd-113">N</span><span class="sxs-lookup"><span data-stu-id="213dd-113">N</span></span>        |
| <span data-ttu-id="213dd-114">FaceName</span><span class="sxs-lookup"><span data-stu-id="213dd-114">FaceName</span></span>  | [<span data-ttu-id="213dd-115">Texto</span><span class="sxs-lookup"><span data-stu-id="213dd-115">Text</span></span>](text.md)                   | <span data-ttu-id="213dd-116">N</span><span class="sxs-lookup"><span data-stu-id="213dd-116">N</span></span>   | <span data-ttu-id="213dd-117">N</span><span class="sxs-lookup"><span data-stu-id="213dd-117">N</span></span>        |
| <span data-ttu-id="213dd-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="213dd-118">Size</span></span>      | [<span data-ttu-id="213dd-119">Entero</span><span class="sxs-lookup"><span data-stu-id="213dd-119">Integer</span></span>](integer.md)             | <span data-ttu-id="213dd-120">N</span><span class="sxs-lookup"><span data-stu-id="213dd-120">N</span></span>   | <span data-ttu-id="213dd-121">N</span><span class="sxs-lookup"><span data-stu-id="213dd-121">N</span></span>        |
| <span data-ttu-id="213dd-122">Color</span><span class="sxs-lookup"><span data-stu-id="213dd-122">Color</span></span>     | [<span data-ttu-id="213dd-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="213dd-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="213dd-124">N</span><span class="sxs-lookup"><span data-stu-id="213dd-124">N</span></span>   | <span data-ttu-id="213dd-125">Y</span><span class="sxs-lookup"><span data-stu-id="213dd-125">Y</span></span>        |
| <span data-ttu-id="213dd-126">StyleBits</span><span class="sxs-lookup"><span data-stu-id="213dd-126">StyleBits</span></span> | [<span data-ttu-id="213dd-127">Entero</span><span class="sxs-lookup"><span data-stu-id="213dd-127">Integer</span></span>](integer.md)             | <span data-ttu-id="213dd-128">N</span><span class="sxs-lookup"><span data-stu-id="213dd-128">N</span></span>   | <span data-ttu-id="213dd-129">Y</span><span class="sxs-lookup"><span data-stu-id="213dd-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="213dd-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="213dd-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="213dd-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Estilo]</span><span class="sxs-lookup"><span data-stu-id="213dd-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="213dd-132">Esta columna es el nombre del estilo de fuente.</span><span class="sxs-lookup"><span data-stu-id="213dd-132">This column is the name of the font style.</span></span> <span data-ttu-id="213dd-133">Este nombre se puede incrustar en la cadena de texto para indicar un cambio de estilo.</span><span class="sxs-lookup"><span data-stu-id="213dd-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="213dd-134">Tenga en cuenta que el nombre de estilo de fuente utilizado en este campo no debe acabar con los caracteres: \_ UL.</span><span class="sxs-lookup"><span data-stu-id="213dd-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="213dd-135">Vea [Agregar controles y texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="213dd-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="213dd-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span><span class="sxs-lookup"><span data-stu-id="213dd-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="213dd-137">Cadena que indica el nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="213dd-137">A string indicating the name of the font.</span></span> <span data-ttu-id="213dd-138">La cadena no debe tener más de 31 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="213dd-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="213dd-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Ajusta</span><span class="sxs-lookup"><span data-stu-id="213dd-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="213dd-140">Tamaño de fuente medido en puntos.</span><span class="sxs-lookup"><span data-stu-id="213dd-140">The font size measured in points.</span></span> <span data-ttu-id="213dd-141">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="213dd-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="213dd-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span><span class="sxs-lookup"><span data-stu-id="213dd-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="213dd-143">Esta columna especifica el color del texto que se muestra en un [control de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="213dd-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="213dd-144">Todos los demás tipos de controles siempre utilizan el color de texto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="213dd-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="213dd-145">El valor colocado en esta columna debe calcularse mediante la siguiente fórmula: 65536 \* azul + 256 \* verde + rojo, donde rojo, verde y azul están cada uno en el intervalo de 0-255.</span><span class="sxs-lookup"><span data-stu-id="213dd-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="213dd-146">El valor no debe superar 16777215, que es el valor de blanco.</span><span class="sxs-lookup"><span data-stu-id="213dd-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="213dd-147">El valor es 0 para negro, 255 para rojo, 65280 para verde, 16711680 para azul y 8421504 para gris.</span><span class="sxs-lookup"><span data-stu-id="213dd-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="213dd-148">Al dejar el campo vacío, se especifica el color predeterminado.</span><span class="sxs-lookup"><span data-stu-id="213dd-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="213dd-149">No coloque controles de [texto](text-control.md) transparente sobre los mapas de bits de color.</span><span class="sxs-lookup"><span data-stu-id="213dd-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="213dd-150">Es posible que el texto no esté visible si el usuario cambia la combinación de colores de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="213dd-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="213dd-151">Por ejemplo, el texto puede volverse invisible si el usuario establece el parámetro de contraste alto para accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="213dd-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="213dd-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span><span class="sxs-lookup"><span data-stu-id="213dd-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="213dd-153">Combinación de bits que indica el formato del texto.</span><span class="sxs-lookup"><span data-stu-id="213dd-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="213dd-154">Los bits de estilo individuales tienen los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="213dd-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="213dd-155">Constante</span><span class="sxs-lookup"><span data-stu-id="213dd-155">Constant</span></span>                             | <span data-ttu-id="213dd-156">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="213dd-156">Hexadecimal</span></span> | <span data-ttu-id="213dd-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="213dd-157">Decimal</span></span> | <span data-ttu-id="213dd-158">Estilo</span><span class="sxs-lookup"><span data-stu-id="213dd-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="213dd-159">**msidbTextStyleStyleBitsBold**</span><span class="sxs-lookup"><span data-stu-id="213dd-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="213dd-160">0x001</span><span class="sxs-lookup"><span data-stu-id="213dd-160">0x001</span></span>       | <span data-ttu-id="213dd-161">1</span><span class="sxs-lookup"><span data-stu-id="213dd-161">1</span></span>       | <span data-ttu-id="213dd-162">Bold</span><span class="sxs-lookup"><span data-stu-id="213dd-162">Bold</span></span>       |
| <span data-ttu-id="213dd-163">**msidbTextStyleStyleBitsItalic**</span><span class="sxs-lookup"><span data-stu-id="213dd-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="213dd-164">0x002</span><span class="sxs-lookup"><span data-stu-id="213dd-164">0x002</span></span>       | <span data-ttu-id="213dd-165">2</span><span class="sxs-lookup"><span data-stu-id="213dd-165">2</span></span>       | <span data-ttu-id="213dd-166">Cursiva</span><span class="sxs-lookup"><span data-stu-id="213dd-166">Italic</span></span>     |
| <span data-ttu-id="213dd-167">**msidbTextStyleStyleBitsUnderline**</span><span class="sxs-lookup"><span data-stu-id="213dd-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="213dd-168">0x004</span><span class="sxs-lookup"><span data-stu-id="213dd-168">0x004</span></span>       | <span data-ttu-id="213dd-169">4</span><span class="sxs-lookup"><span data-stu-id="213dd-169">4</span></span>       | <span data-ttu-id="213dd-170">Subrayado</span><span class="sxs-lookup"><span data-stu-id="213dd-170">Underline</span></span>  |
| <span data-ttu-id="213dd-171">**msidbTextStyleStyleBitsStrike**</span><span class="sxs-lookup"><span data-stu-id="213dd-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="213dd-172">0x008</span><span class="sxs-lookup"><span data-stu-id="213dd-172">0x008</span></span>       | <span data-ttu-id="213dd-173">8</span><span class="sxs-lookup"><span data-stu-id="213dd-173">8</span></span>       | <span data-ttu-id="213dd-174">Golpear</span><span class="sxs-lookup"><span data-stu-id="213dd-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="213dd-175">Validación</span><span class="sxs-lookup"><span data-stu-id="213dd-175">Validation</span></span>

<dl>

[<span data-ttu-id="213dd-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="213dd-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="213dd-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="213dd-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="213dd-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="213dd-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="213dd-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="213dd-179">ICE45</span></span>](ice45.md)  
</dl>

 

 




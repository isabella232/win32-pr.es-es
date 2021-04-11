---
title: Formato y diseño de texto
description: DirectWrite proporciona dos interfaces para dar formato al texto IDWriteTextFormat y IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formato de texto
- DirectWrite, diseño
- DirectWrite, interfaz IDWriteTextFormat
- DirectWrite, interfaz IDWriteTextLayout
- Interfaz IDWriteTextFormat
- Interfaz IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271347"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="24617-109">Formato y diseño de texto</span><span class="sxs-lookup"><span data-stu-id="24617-109">Text Formatting and Layout</span></span>

<span data-ttu-id="24617-110">[DirectWrite](direct-write-portal.md) proporciona dos interfaces para dar formato al texto: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="24617-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="24617-111">**IDWriteTextFormat** describe solo el formato del texto y se utiliza en casos en los que una cadena completa debe ser del mismo tamaño de fuente, estilo, peso, etc.</span><span class="sxs-lookup"><span data-stu-id="24617-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="24617-112">Por otro lado, **IDWriteTextLayout** encapsula una cadena de texto y el formato de los intervalos especificados de la cadena.</span><span class="sxs-lookup"><span data-stu-id="24617-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="24617-113">En este documento se describe cada interfaz y sus usos.</span><span class="sxs-lookup"><span data-stu-id="24617-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="24617-114">Para obtener más información sobre la creación y los métodos de estas interfaces, vea las páginas de referencia de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="24617-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="24617-115">Este documento contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="24617-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="24617-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="24617-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="24617-117">Modificar un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="24617-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="24617-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="24617-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="24617-119">Aplicar formato a un intervalo de texto</span><span class="sxs-lookup"><span data-stu-id="24617-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="24617-120">Opciones de representación</span><span class="sxs-lookup"><span data-stu-id="24617-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="24617-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="24617-121">IDWriteTextFormat</span></span>

<span data-ttu-id="24617-122">Un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se usa para:</span><span class="sxs-lookup"><span data-stu-id="24617-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="24617-123">Describe el formato de una cadena completa cuando se representa.</span><span class="sxs-lookup"><span data-stu-id="24617-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="24617-124">Para representar una cadena con varios formatos, use un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="24617-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="24617-125">Especifique el formato de texto predeterminado al crear un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="24617-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="24617-126">Para crear un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , se usa el método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) y se especifica la familia de fuentes, la colección de fuentes, el espesor de fuente, el tamaño de fuente (en DIP) y el nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="24617-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="24617-127">Modificar un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="24617-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="24617-128">Una vez creada una interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , algunos valores no se pueden cambiar: la familia de fuentes, la colección, el peso y el tamaño, así como el nombre de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="24617-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="24617-129">Para cambiar estos valores, se debe crear un nuevo objeto **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="24617-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="24617-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) permite cambiar las propiedades anteriores sin volver a crear el elemento.</span><span class="sxs-lookup"><span data-stu-id="24617-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anthing.</span></span> <span data-ttu-id="24617-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) le permite realizar cambios en el formato que se aplican a todo el texto, como la alineación del texto.</span><span class="sxs-lookup"><span data-stu-id="24617-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="24617-132">Si desea aplicar formato a intervalos de caracteres específicos, debe hacerlo mediante un **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="24617-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="24617-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) proporciona métodos para establecer la alineación del texto, la dirección del flujo, la tabulación incremental, el interlineado, la alineación del párrafo, el recorte y el ajuste de línea.</span><span class="sxs-lookup"><span data-stu-id="24617-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="24617-134">Estas propiedades se pueden cambiar en cualquier momento después de la creación del objeto **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="24617-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="24617-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="24617-135">IDWriteTextLayout</span></span>

<span data-ttu-id="24617-136">La interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , a diferencia de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), representa un bloque de texto y el formato asociado.</span><span class="sxs-lookup"><span data-stu-id="24617-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="24617-137">**IDWriteTextFormat** representa la información de formato inicial.</span><span class="sxs-lookup"><span data-stu-id="24617-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="24617-138">En el ejemplo siguiente se muestra cómo crear un objeto **IDWriteTextLayout** mediante [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="24617-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



<span data-ttu-id="24617-139">El texto de un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) no se puede cambiar una vez creado el objeto.</span><span class="sxs-lookup"><span data-stu-id="24617-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="24617-140">Para cambiar el texto, debe eliminar el objeto existente y crear un nuevo objeto **IDWriteTextLayout** .</span><span class="sxs-lookup"><span data-stu-id="24617-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="24617-141">Puede usar un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para dar formato a los intervalos de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="24617-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="24617-142">**IDWriteTextLayout** también proporciona métodos para cambiar el estilo y el peso de la fuente, y para agregar características de fuentes OpenType y pruebas de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="24617-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="24617-143">Para obtener más información y una lista completa de los métodos, vea la página de referencia de [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="24617-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="24617-144">Aplicar formato a un intervalo de texto</span><span class="sxs-lookup"><span data-stu-id="24617-144">Formatting a range of text</span></span>

<span data-ttu-id="24617-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) proporciona varios métodos para dar formato a los intervalos de texto.</span><span class="sxs-lookup"><span data-stu-id="24617-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="24617-146">Cada uno de estos métodos toma una estructura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) como un parámetro para especificar la posición del texto inicial dentro de la cadena y la longitud del intervalo al que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="24617-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="24617-147">En el ejemplo siguiente se muestra cómo establecer el espesor de fuente de un intervalo de texto en negrita.</span><span class="sxs-lookup"><span data-stu-id="24617-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="24617-148">Opciones de representación</span><span class="sxs-lookup"><span data-stu-id="24617-148">Rendering Options</span></span>

<span data-ttu-id="24617-149">El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D](../direct2d/direct2d-portal.md); sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="24617-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="24617-150">La cadena descrita por un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="24617-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="24617-151">Se [representa mediante Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="24617-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="24617-152">Se [representa mediante un representador de texto personalizado](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="24617-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="24617-153">[Se representan en una superficie de GDI](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="24617-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
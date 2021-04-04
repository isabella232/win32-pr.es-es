---
description: En este tema se describe cómo escribir texto en un OM XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Escribir texto en un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277673"
---
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="91cfd-103">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="91cfd-104">En este tema se describe cómo escribir texto en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="91cfd-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="91cfd-105">El texto se coloca en un OM XPS creando y dando formato a una interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) y agregando después la interfaz **IXpsOMGlyphs** a la lista de objetos visuales de la página o Canvas.</span><span class="sxs-lookup"><span data-stu-id="91cfd-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="91cfd-106">Cada interfaz **IXpsOMGlyphs** representa una ejecución de glifos, que es una ejecución continua de caracteres que comparten un formato común.</span><span class="sxs-lookup"><span data-stu-id="91cfd-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="91cfd-107">Cuando cambia un elemento de formato de caracteres (por ejemplo, el tipo o el tamaño de fuente) o cuando se interrumpe una línea, se debe crear una nueva interfaz **IXpsOMGlyphs** y agregarla a la lista de objetos visuales.</span><span class="sxs-lookup"><span data-stu-id="91cfd-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="91cfd-108">Algunas de las propiedades de una ejecución de glifo se pueden establecer mediante los métodos de la interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) .</span><span class="sxs-lookup"><span data-stu-id="91cfd-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="91cfd-109">Sin embargo, algunas propiedades interactúan con otras y se deben establecer mediante una interfaz [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .</span><span class="sxs-lookup"><span data-stu-id="91cfd-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="91cfd-110">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="91cfd-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="91cfd-111">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="91cfd-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="91cfd-112">Crear una ejecución de glifo desde una cadena</span><span class="sxs-lookup"><span data-stu-id="91cfd-112">Create a glyph run from a string</span></span>

<span data-ttu-id="91cfd-113">Una ejecución de glifo se crea normalmente en varios pasos que incluyen la carga de los recursos de fuente que se usan en la ejecución del glifo, el establecimiento de un pincel de relleno, la especificación del tamaño de fuente y la ubicación de inicio, y el establecimiento de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="91cfd-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="91cfd-114">La siguiente sección del ejemplo de código contiene una rutina que acepta algunas variables, incluidos el tamaño, el color y la ubicación de la fuente, y los caracteres que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="91cfd-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="91cfd-115">A continuación, el código crea una ejecución de glifo y, a continuación, la agrega a una página.</span><span class="sxs-lookup"><span data-stu-id="91cfd-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="91cfd-116">En el ejemplo de código se supone que se ha producido la inicialización descrita en [Initialize an XPS OM](xps-object-model-initialization.md) y que el documento tiene al menos una página.</span><span class="sxs-lookup"><span data-stu-id="91cfd-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="91cfd-117">Para obtener más información sobre cómo crear un OM XPS en blanco, consulte [crear un OM XPS en blanco](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="91cfd-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a><span data-ttu-id="91cfd-118">Carga y creación de recursos</span><span class="sxs-lookup"><span data-stu-id="91cfd-118">Load and create resources</span></span>

<span data-ttu-id="91cfd-119">La creación de una interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) requiere un recurso de fuente.</span><span class="sxs-lookup"><span data-stu-id="91cfd-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="91cfd-120">En muchos casos, un bloque de texto utiliza la misma fuente y color.</span><span class="sxs-lookup"><span data-stu-id="91cfd-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="91cfd-121">Por lo tanto, esta sección del ejemplo de código creará las interfaces de recursos de fuente que se utilizarán en las llamadas que colocan el texto en la página.</span><span class="sxs-lookup"><span data-stu-id="91cfd-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a><span data-ttu-id="91cfd-122">Dibujar texto en una página</span><span class="sxs-lookup"><span data-stu-id="91cfd-122">Draw text in a page</span></span>

<span data-ttu-id="91cfd-123">En la sección final del ejemplo de código se crean las ejecuciones del glifo para cada ejecución de texto con formato similar.</span><span class="sxs-lookup"><span data-stu-id="91cfd-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="91cfd-124">Para ejecutar el código de esta sección final, se necesitan la interfaz **xpsFactory** , así como el recurso de fuente y un pincel de color de texto, y deben haberse creado e inicializado.</span><span class="sxs-lookup"><span data-stu-id="91cfd-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="91cfd-125">En este ejemplo, la función descrita en la primera sección se usa para crear las ejecuciones del glifo y agregarlas a la página.</span><span class="sxs-lookup"><span data-stu-id="91cfd-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a><span data-ttu-id="91cfd-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91cfd-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="91cfd-127">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="91cfd-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="91cfd-128">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="91cfd-129">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="91cfd-130">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="91cfd-131">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="91cfd-132">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="91cfd-133">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="91cfd-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="91cfd-134">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="91cfd-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="91cfd-135">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="91cfd-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="91cfd-136">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="91cfd-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="91cfd-137">**IXpsOMGlyphsEditor**</span><span class="sxs-lookup"><span data-stu-id="91cfd-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="91cfd-138">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="91cfd-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="91cfd-139">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="91cfd-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="91cfd-140">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="91cfd-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="91cfd-141">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="91cfd-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="91cfd-142">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="91cfd-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="91cfd-143">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="91cfd-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="91cfd-144">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="91cfd-145">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="91cfd-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="91cfd-146">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="91cfd-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

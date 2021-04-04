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
# <a name="write-text-to-an-xps-om"></a>Escribir texto en un OM XPS

En este tema se describe cómo escribir texto en un OM XPS.

El texto se coloca en un OM XPS creando y dando formato a una interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) y agregando después la interfaz **IXpsOMGlyphs** a la lista de objetos visuales de la página o Canvas. Cada interfaz **IXpsOMGlyphs** representa una ejecución de glifos, que es una ejecución continua de caracteres que comparten un formato común. Cuando cambia un elemento de formato de caracteres (por ejemplo, el tipo o el tamaño de fuente) o cuando se interrumpe una línea, se debe crear una nueva interfaz **IXpsOMGlyphs** y agregarla a la lista de objetos visuales.

Algunas de las propiedades de una ejecución de glifo se pueden establecer mediante los métodos de la interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) . Sin embargo, algunas propiedades interactúan con otras y se deben establecer mediante una interfaz [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .

Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Ejemplo de código

### <a name="create-a-glyph-run-from-a-string"></a>Crear una ejecución de glifo desde una cadena

Una ejecución de glifo se crea normalmente en varios pasos que incluyen la carga de los recursos de fuente que se usan en la ejecución del glifo, el establecimiento de un pincel de relleno, la especificación del tamaño de fuente y la ubicación de inicio, y el establecimiento de la cadena Unicode.

La siguiente sección del ejemplo de código contiene una rutina que acepta algunas variables, incluidos el tamaño, el color y la ubicación de la fuente, y los caracteres que se van a escribir. A continuación, el código crea una ejecución de glifo y, a continuación, la agrega a una página. En el ejemplo de código se supone que se ha producido la inicialización descrita en [Initialize an XPS OM](xps-object-model-initialization.md) y que el documento tiene al menos una página. Para obtener más información sobre cómo crear un OM XPS en blanco, consulte [crear un OM XPS en blanco](create-a-blank-xps-om.md).


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



### <a name="load-and-create-resources"></a>Carga y creación de recursos

La creación de una interfaz [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) requiere un recurso de fuente. En muchos casos, un bloque de texto utiliza la misma fuente y color. Por lo tanto, esta sección del ejemplo de código creará las interfaces de recursos de fuente que se utilizarán en las llamadas que colocan el texto en la página.


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



### <a name="draw-text-in-a-page"></a>Dibujar texto en una página

En la sección final del ejemplo de código se crean las ejecuciones del glifo para cada ejecución de texto con formato similar. Para ejecutar el código de esta sección final, se necesitan la interfaz **xpsFactory** , así como el recurso de fuente y un pincel de color de texto, y deben haberse creado e inicializado. En este ejemplo, la función descrita en la primera sección se usa para crear las ejecuciones del glifo y agregarlas a la página.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Navegar por el OM de XPS](navigate-the-xps-om.md)
</dt> <dt>

[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Colocar imágenes en un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

[Escribir un OM XPS en un documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Imprimir un OM XPS](print-an-xps-om.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicializar un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Referencia de la API de documentos XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

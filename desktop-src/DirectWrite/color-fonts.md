---
title: Fuentes de colores
description: En este tema se describen las fuentes de color, su compatibilidad con DirectWrite y Direct2D, y cómo usarlas en la aplicación.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255087"
---
# <a name="color-fonts"></a>Fuentes de colores

En este tema se describen las fuentes de color, su compatibilidad con DirectWrite y Direct2D, y cómo usarlas en la aplicación.

Este documento contiene las siguientes partes:

-   [¿Qué son las fuentes de color?](#what-are-color-fonts)
-   [¿Por qué usar fuentes de color?](#why-use-color-fonts)
-   [¿Qué tipos de fuentes de color Windows admite?](#what-kinds-of-color-fonts-does-windows-support)
-   [Uso de fuentes de color](#using-color-fonts)
    -   [Uso de fuentes de color en una aplicación XAML](#using-color-fonts-in-a-xaml-app)
    -   [Uso de fuentes de color en Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Uso de fuentes de color DirectWrite y Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Uso de fuentes de color con Win2D](#using-color-fonts-with-win2d)
-   [Temas relacionados](#related-topics)

## <a name="what-are-color-fonts"></a>¿Qué son las fuentes de color?

Las fuentes de color, también conocidas como fuentes de color o fuentes tótices, son una tecnología de fuentes que permite a los diseñadores de fuentes usar varios colores dentro de cada glifo. Las fuentes de color permiten escenarios de texto con forma de color en aplicaciones y sitios web con menos código y una compatibilidad más sólida con el sistema operativo que las técnicas ad hoc implementadas por encima del sistema de representación de texto.

Las fuentes con las que probablemente esté más familiarizado no son fuentes de color. Estas fuentes definen solo la forma de los glifos que contienen, ya sea con contornos vectoriales o mapas de bits monocromáticos. En el momento del dibujo, un representador de texto rellena la forma del glifo con un único color (el color de fuente) especificado por la aplicación o el documento que se representa. Las fuentes de color, por otro lado, contienen información de color además de información de forma. Algunos enfoques permiten a los diseñadores de fuentes ofrecer varias paletas de colores, lo que proporciona flexibilidad a la fuente de color.

En el ejemplo siguiente se muestra un glifo de la Segoe UI fuente de color Emoji. El glifo se representa en monocromo a la izquierda y en color a la derecha.

![Muestra glifos en paralelo, el glifo izquierdo representado en monocromo, a la derecha en la fuente de color Emoji de Segoe U I.](images/color-font-cat.png)

Las fuentes de color suelen incluir información de reserva para plataformas que no admiten fuentes de color o para escenarios en los que se ha deshabilitado la funcionalidad de color. En esas plataformas, las fuentes de color se representan como fuentes monocromáticas normales.

## <a name="why-use-color-fonts"></a>¿Por qué usar fuentes de color?

Históricamente, los diseñadores y desarrolladores han usado diversas técnicas para lograr texto en blanco. Por ejemplo, los sitios web suelen usar imágenes de trama en lugar de texto para mostrar encabezados enriquecidos. Este enfoque permite flexibilidad de flexibilidad, pero los gráficos de trama no se escalan bien a todos los tamaños de pantalla, ni proporcionan las mismas características de accesibilidad que el texto real. Otra técnica común consiste en superponer varias fuentes monocromáticas en diferentes colores de fuente, pero esto normalmente requiere código de diseño adicional para administrar.

Las fuentes de color ofrecen una manera de lograr estos efectos visuales con toda la simplicidad y funcionalidad de las fuentes normales. El texto representado en una fuente de color es el mismo que otro texto: se puede copiar y pegar, se puede analizar mediante herramientas de accesibilidad, etc.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>¿Qué tipos de fuentes de color Windows admite?

La [especificación OpenType define](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) varias maneras de insertar información de color en una fuente. A partir de Windows 10 de aniversario, DirectWrite y Direct2D (y los marcos Windows basados en ellos) admiten todos estos enfoques. Se resumen en la tabla siguiente:



| Técnica                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / [Tablas CPAL](/typography/opentype/spec/cpal) | Usa capas de vectores de color, cuyas formas se definen de la misma manera que los contornos de glifo de un solo color. **Nota:** Se admite a partir de Windows 8.1. <br/>                                                                                                                                                 |
| [Tabla SVG](/typography/opentype/spec/svg)                                                                 | Usa imágenes vectoriales que se han escrito en el formato de gráficos vectoriales escalables. **Nota:** A Windows 10 de aniversario, DirectWrite admite un subconjunto de la especificación SVG completa. No se garantiza que todo el contenido SVG se represente en una fuente SVG OpenType. Consulte [Compatibilidad con SVG](../direct2d/svg-support.md) para obtener más detalles. <br/> |
| [CLONT](/typography/opentype/spec/cbdt) / [Tablas CBLC](/typography/opentype/spec/cblc) | Usa imágenes de mapa de bits de color incrustadas.                                                                                                                                                                                                                                                                                |
| [tabla sbix](/typography/opentype/spec/sbix)                                                               | Usa imágenes de mapa de bits de color incrustadas.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Uso de fuentes de color

Desde la perspectiva del usuario, las fuentes de color son solo fuentes . Por ejemplo, normalmente se pueden instalar y desinstalar del sistema de la misma manera que las fuentes monocromáticas, y se representan como texto normal seleccionable.

Desde la perspectiva del desarrollador, las fuentes de color normalmente se usan de la misma manera que las fuentes monocromáticas. En los marcos XAML y Microsoft Edge, puede cambiar el estilo del texto con fuentes de color de la misma manera que las fuentes normales y, de forma predeterminada, el texto se representará en color. Sin embargo, si la aplicación llama directamente a las API de Direct2D (o a las API de Win2D) para representar texto, debe solicitar explícitamente la representación de fuentes de color.

### <a name="using-color-fonts-in-a-xaml-app"></a>Uso de fuentes de color en una aplicación XAML

Los elementos de texto de la plataforma XAML (como [TextBlock,](/uwp/api/windows.ui.xaml.controls.textblock) [TextBox,](/uwp/api/windows.ui.xaml.controls.textbox) [RichEditBox,](/uwp/api/windows.ui.xaml.controls.richeditbox) [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)y [FontIcon)](/uwp/api/windows.ui.xaml.controls.fonticon)admiten fuentes de color de forma predeterminada. Basta con que el texto tenga una fuente de color y los glifos de color se representarán en color. En el ejemplo de código siguiente se muestra una manera de dar estilo a un TextBlock con una fuente de color empaquetada con la aplicación. La misma técnica se aplica a las fuentes normales.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Si nunca quieres que el elemento de texto XAML represente texto en color, establece su [propiedad IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) en false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Uso de fuentes de color en Microsoft Edge

Las fuentes de color se representan de forma predeterminada en sitios web y aplicaciones web que se ejecutan en Microsoft Edge, incluido el control [WebView xaml.](/uwp/api/windows.ui.xaml.controls.webview) Simplemente use HTML y CSS para dar estilo al texto con una fuente de color, y los glifos de color se representarán en color.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Uso de fuentes de color DirectWrite y Direct2D

La aplicación puede usar los métodos de dibujo de texto de nivel superior de Direct2D [**(DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) y [**DrawTextLayout)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)o puede usar técnicas de nivel inferior para dibujar ejecuciones de glifo directamente. En cualquier caso, la aplicación requiere cambios de código para controlar los glifos de color correctamente. Si la aplicación usa las API **DrawText** y **DrawTextLayout** de Direct2D, tenga en cuenta que no representan glifos de color de forma predeterminada. Esto es para evitar cambios de comportamiento inesperados en las aplicaciones de representación de texto que se diseñaron antes de la compatibilidad con fuentes de color.

Para participar en la representación de glifos de color, pase la marca de opciones [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) al método de dibujo. En el ejemplo de código siguiente se muestra cómo llamar al método DrawText de Direct2D para representar una cadena en una fuente de color:


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Si la aplicación usa API de nivel inferior para controlar las ejecuciones de glifo directamente, seguirá funcionando en presencia de fuentes de color, pero no podrá dibujar glifos de color sin lógica adicional.

Para controlar correctamente los glifos de color, la aplicación debe:

1.  Pase la información de ejecución del glifo a [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), junto con un parámetro [**DWRITE \_ GLYPH IMAGE \_ \_ FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica qué tipos de glifo de color está preparada para controlar la aplicación. Si hay glifos de color presentes (según la fuente y los formatos de imagen de GLIFO DWRITE solicitados), DirectWrite dividirá la ejecución del glifo principal en ejecuciones de glifo de color individuales a las que se puede acceder a través del objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) devuelto en el paso 4. **\_ \_ \_**
2.  Compruebe el HRESULT devuelto por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar si se detectaron ejecuciones de glifos de color. Un **HRESULT** de **DWRITE \_ E \_ NOCOLOR** indica que no se ejecuta ningún glifo de color aplicable.
3.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informó de que no se ejecuta ningún glifo de color (devolviendo **DWRITE \_ E \_ NOCOLOR),** la ejecución completa del glifo se trata como monocromática y la aplicación debe dibujarla como desee (por ejemplo, mediante [**ID2D1DeviceContext::D rawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informa de la presencia de ejecuciones de glifo de color, la aplicación debe omitir la ejecución del glifo principal y, en su lugar, usar las ejecuciones de glifo de color devueltas por TranslateColorGlyphRun. Para ello, itera por el objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) devuelto, recuperando cada ejecución de glifo de color y dibujendo según corresponda para su formato de imagen de glifo (por ejemplo, puede usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) y [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para dibujar glifos de mapa de bits de color y glifos SVG, respectivamente).

En el ejemplo de código siguiente se muestra la estructura general de este procedimiento:


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Uso de fuentes de color con Win2D

De forma similar a Direct2D, las API de dibujo de texto de Win2D no representan glifos de color de forma predeterminada. Para participar en la representación de glifos de color, establezca la marca de opciones [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) en el objeto de formato de texto que la aplicación pasa al método de dibujo de texto. En el ejemplo de código siguiente se muestra cómo representar una cadena en una fuente de color mediante Win2D:


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>Temas relacionados

[DirectWrite de glifo coloreado](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interfaz IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Método IDWriteFactory4::TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**Id2D1DeviceContext4::D rawText (método)**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 


---
title: Fuentes de colores
description: En este tema se describen las fuentes de color, su compatibilidad en DirectWrite y Direct2D, y cómo utilizarlas en la aplicación.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104557795"
---
# <a name="color-fonts"></a>Fuentes de colores

En este tema se describen las fuentes de color, su compatibilidad en DirectWrite y Direct2D, y cómo utilizarlas en la aplicación.

Este documento contiene las siguientes partes:

-   [¿Qué son las fuentes de color?](#what-are-color-fonts)
-   [¿Por qué usar fuentes de color?](#why-use-color-fonts)
-   [¿Qué tipos de fuentes de color admite Windows?](#what-kinds-of-color-fonts-does-windows-support)
-   [Usar fuentes de color](#using-color-fonts)
    -   [Usar fuentes de color en una aplicación XAML](#using-color-fonts-in-a-xaml-app)
    -   [Usar fuentes de color en Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Usar fuentes de color con DirectWrite y Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Usar fuentes de color con Win2D](#using-color-fonts-with-win2d)
-   [Temas relacionados](#related-topics)

## <a name="what-are-color-fonts"></a>¿Qué son las fuentes de color?

Las fuentes de color, también conocidas como fuentes multicolores o fuentes cromáticas, son una tecnología de fuentes que permite a los diseñadores de fuentes usar varios colores dentro de cada glifo. Las fuentes de color permiten escenarios de texto multicolor en aplicaciones y sitios web con menos código y una compatibilidad de sistema operativo más sólida que las técnicas ad hoc implementadas por encima del sistema de representación de texto.

Las fuentes con las que probablemente esté familiarizado no son fuentes de color. Estas fuentes definen solo la forma de los glifos que contienen, ya sea con contornos vectoriales o con mapas de bits monocromáticos. En el momento de dibujar, un representador de texto rellena la forma de glifo usando un color único (el color de fuente) especificado por la aplicación o el documento que se está representando. Por otro lado, las fuentes de color contienen información de color además de la información de forma. Algunos enfoques permiten a los diseñadores de fuentes ofrecer varias paletas de colores, lo que proporciona la flexibilidad artística de fuente de color.

En el ejemplo siguiente se muestra un glifo de la fuente de color Segoe UI Emoji. El glifo se representa en monocromo a la izquierda y en color a la derecha.

![Muestra glifos en paralelo, el glifo izquierdo representado en monocromo, el derecho en la fuente de color Segoe U I Emoji.](images/color-font-cat.png)

Las fuentes de color suelen incluir información de reserva para plataformas que no admiten fuentes de color o para escenarios en los que se ha deshabilitado la funcionalidad de color. En esas plataformas, las fuentes de color se representan como fuentes monocromáticas normales.

## <a name="why-use-color-fonts"></a>¿Por qué usar fuentes de color?

Históricamente, los diseñadores y desarrolladores han usado diversas técnicas para lograr el texto multicolor. Por ejemplo, los sitios web suelen usar imágenes de tramas en lugar de texto para mostrar encabezados completos. Este enfoque permite una flexibilidad artística, pero los gráficos de tramas no se adaptan bien a todos los tamaños de pantalla, ni proporcionan las mismas características de accesibilidad que el texto real. Otra técnica común es superponer varias fuentes monocromáticas en diferentes colores de fuente, pero esto normalmente requiere un código de diseño adicional para administrar.

Las fuentes de color ofrecen una manera de lograr estos efectos visuales con toda la simplicidad y funcionalidad de las fuentes normales. El texto representado en una fuente de color es el mismo que el de otro texto: puede copiarse y pegarse, puede ser analizado por herramientas de accesibilidad, etc.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>¿Qué tipos de fuentes de color admite Windows?

La [especificación OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) define varias maneras de insertar información de color en una fuente. A partir de la actualización de aniversario de Windows 10, DirectWrite y Direct2D (y los marcos de trabajo de Windows integrados) admiten todos estos enfoques. Se resumen en la tabla siguiente:



| Técnica                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / Tablas de [CPAL](/typography/opentype/spec/cpal) | Utiliza capas de vectores de color, cuyas formas se definen de la misma manera que los contornos de glifo de un solo color. **Nota:** Se admite a partir de Windows 8.1. <br/>                                                                                                                                                 |
| Tabla [SVG](/typography/opentype/spec/svg)                                                                 | Utiliza imágenes vectoriales creadas en el formato de gráficos vectoriales escalables. **Nota:** A partir de la actualización de aniversario de Windows 10, DirectWrite admite un subconjunto de la especificación SVG completa. No se garantiza que todo el contenido SVG se represente en una fuente SVG OpenType. Consulte [compatibilidad con SVG](../direct2d/svg-support.md) para obtener más detalles. <br/> |
| [CBDT](/typography/opentype/spec/cbdt) / Tablas de [CBLC](/typography/opentype/spec/cblc) | Utiliza imágenes de mapa de bits de color incrustado.                                                                                                                                                                                                                                                                                |
| tabla [sbix](/typography/opentype/spec/sbix)                                                               | Utiliza imágenes de mapa de bits de color incrustado.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Usar fuentes de color

Desde la perspectiva del usuario, las fuentes de color son simplemente fuentes. Por ejemplo, normalmente se pueden instalar y desinstalar del sistema de la misma manera que las fuentes monocromáticas, y se representan como texto normal y seleccionable.

También desde la perspectiva del desarrollador, las fuentes de color suelen usarse de la misma manera que las fuentes monocromáticas. En los marcos XAML y Microsoft Edge, puede aplicar estilo al texto con fuentes de color de la misma manera que a las fuentes normales y, de forma predeterminada, el texto se representará en color. Sin embargo, si la aplicación llama directamente a las API de Direct2D (o a las API de Win2D) para representar texto, debe solicitar explícitamente la representación de fuentes de color.

### <a name="using-color-fonts-in-a-xaml-app"></a>Usar fuentes de color en una aplicación XAML

Los elementos de texto de la plataforma XAML (como [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)y [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) admiten fuentes de color de forma predeterminada. Simplemente puede aplicar estilo al texto con una fuente de color y cualquier glifo de color se representará en color. En el ejemplo de código siguiente se muestra una manera de aplicar estilo a un TextBlock con una fuente de color empaquetada con la aplicación. La misma técnica se aplica a las fuentes normales.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Si no desea que el elemento de texto XAML represente texto de colores multicolor, establezca la propiedad [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) en false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Usar fuentes de color en Microsoft Edge

Las fuentes de color se representan de forma predeterminada en sitios web y aplicaciones web que se ejecutan en Microsoft Edge, incluido el control [WebView](/uwp/api/windows.ui.xaml.controls.webview) de XAML. Simplemente use HTML y CSS para aplicar estilo al texto con una fuente de color y cualquier glifo de color se representará en color.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Usar fuentes de color con DirectWrite y Direct2D

La aplicación puede usar los métodos de dibujo de texto de nivel superior de Direct2D s ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) y [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)), o puede usar técnicas de nivel inferior para dibujar directamente las ejecuciones de glifos. En cualquier caso, la aplicación requiere cambios en el código para poder controlar correctamente los glifos de color. Si la aplicación usa las API de **DrawTextLayout** y **DrawText** de Direct2D s, tenga en cuenta que no representan glifos de color de forma predeterminada. Esto sirve para evitar cambios de comportamiento inesperados en las aplicaciones de representación de texto que se diseñaron antes de la compatibilidad con fuentes de color.

Para participar en la representación del glifo de color, pase la marca [**D2D1 \_ Draw \_ Text \_ Options \_ enable \_ color \_ Font**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) Options al método de dibujo. En el ejemplo de código siguiente se muestra cómo llamar al método DrawText de Direct2D s para representar una cadena en una fuente de color:


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



Si la aplicación usa las API de nivel inferior para controlar las ejecuciones de glifos directamente, seguirá funcionando en presencia de fuentes de color, pero no podrá dibujar glifos de color sin lógica adicional.

Para controlar correctamente los glifos de color, la aplicación debe:

1.  Pase la información de ejecución del glifo a [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), junto con un parámetro de [**formatos de \_ \_ imagen \_ de glifo DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica qué tipos de glifo de color tiene la aplicación preparada para controlar. Si hay glifos de color presentes (en función de la fuente y los **\_ formatos de \_ imagen \_ de glifo de DWRITE** solicitados), DirectWrite dividirá la ejecución del glifo principal en ejecuciones de glifos de color individuales a las que se puede tener acceso a través del objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) devuelto en el paso 4.
2.  Compruebe el HRESULT devuelto por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar si se ha detectado alguna ejecución del glifo de color. Un **valor HRESULT** de **DWRITE \_ E \_ nocolor** indica que no hay ninguna ejecución del glifo de color aplicable.
3.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informara de que no hay ejecuciones de glifos de color (devolviendo **DWRITE \_ E \_ nocolor**), toda la ejecución del glifo se trata como monocromática y la aplicación debe dibujarla como desee (por ejemplo, mediante [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Si [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) informa de la presencia de ejecuciones del glifo de color, la aplicación debe omitir la ejecución del glifo principal y, en su lugar, usar las ejecuciones del glifo de color devueltas por TranslateColorGlyphRun. Para ello, recorra en iteración el objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) devuelto, recuperando cada glifo de color y dibuje según corresponda para su formato de imagen de glifo (por ejemplo, puede usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) y [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para dibujar glifos de mapa de bits de color y glifos SVG, respectivamente).

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



### <a name="using-color-fonts-with-win2d"></a>Usar fuentes de color con Win2D

Al igual que en Direct2D, las API de dibujo de texto de Win2D s no representan glifos de color de forma predeterminada. Para participar en la representación del glifo de color, establezca la marca de opciones [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) en el objeto de formato de texto que la aplicación pasa al método de dibujo de texto. En el ejemplo de código siguiente se muestra cómo representar una cadena en una fuente de color mediante Win2D:


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

[Ejemplo de glifo de color de DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interfaz IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**IDWriteFactory4:: TranslateColorGlyphRun (método)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4::D método rawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 


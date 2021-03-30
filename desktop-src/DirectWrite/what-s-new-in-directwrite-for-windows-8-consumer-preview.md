---
title: Novedades de DirectWrite
description: Estas son algunas de las nuevas adiciones a DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: bf1a62917e18dcda7e7c4e3f1b05731b60628967
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "103800914"
---
# <a name="whats-new-in-directwrite"></a>Novedades de DirectWrite

En este tema se describen las novedades de [DirectWrite](direct-write-portal.md) para varias versiones de Windows 10.

## <a name="project-reunion-01-prerelease"></a>Versión preliminar de Project reunion 0,1

[Project reunion](/windows/apps/project-reunion/) presenta una nueva versión de DirectWrite, denominada DWriteCore, que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use entre plataformas. Para obtener más información, consulte [información general de DWriteCore](dwritecore-overview.md).

## <a name="windows-10-may-2019-update"></a>Actualización del 10 de mayo de 2019 de Windows 2019

No se agregaron características ni API ni se actualizaron para Windows 10, versión 1903 (10,0; Compilación 18362) &mdash; también conocida como Windows 10 mayo de actualización de 2019.

## <a name="windows-10-october-2018-update"></a>Actualización de octubre de 2018 de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1809 (10,0; Compilación 17763) &mdash; también se conoce como actualización de Windows 10 de octubre de 2018.

### <a name="new"></a>Nuevo

- Enumeración [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type)
- Interfaz [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) y sus métodos

## <a name="windows-10-april-2018-update"></a>Actualización de abril de 2018 de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1803 (10,0; Compilación 17134) &mdash; también se conoce como actualización de Windows 10 de abril de 2018.

### <a name="new"></a>Nuevo

- Interfaz [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) y sus métodos
- Interfaz [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) y sus métodos
- Interfaz [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) y sus métodos

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1709 (10,0; Compilación 16299) &mdash; también conocido como Windows 10 Fall Creators Update.

### <a name="new"></a>Nuevo

- Enumeración [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes)
- Enumeración [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes)
- Enumeración [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag)
- Enumeración [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model)
- Interfaz [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) y sus métodos
- Interfaz [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) y sus métodos
- Interfaz [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) y sus métodos
- Interfaz [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) y sus métodos
- Interfaz [**IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) y sus métodos
- Interfaz [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) y sus métodos
- Interfaz [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) y sus métodos
- Interfaz [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) y sus métodos
- Interfaz [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) y sus métodos
- Interfaz [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) y sus métodos
- Interfaz [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) y sus métodos
- Interfaz [**IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) y sus métodos
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) macro
- Estructura de [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
- Estructura de [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)

### <a name="moved"></a>Puesto

Enumeración de [**DWRITE_GLYPH_IMAGE_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que se ha pasado de `dwrite_3.h` a `dcommon.h` .

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update.

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1703 (10,0; Compilación 15063) &mdash; también se conoce como Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Compatibilidad ampliada con API para fuentes de nube y conjuntos de fuentes personalizadas

Windows 10 incluye las API que permiten a las aplicaciones tener acceso fácilmente a las fuentes de un servicio de fuentes de Windows. En Windows 10 Creators Update, las API para fuentes remotas se amplían para permitir el acceso sencillo a las fuentes de otros orígenes en la web a los que se puede tener acceso mediante HTTP o HTTPS. 

Las nuevas API de fuentes remotas se pueden usar con servicios web públicos o privados. Además, se pueden usar para tener acceso a archivos de fuentes OpenType y sin formato (. ttf,. OTF.,. TTC,. OTC) o fuentes empaquetadas en formatos de contenedor [WOFF](https://www.w3.org/TR/WOFF/) o [WOFF2](https://www.w3.org/TR/WOFF2/) . Las nuevas API se usan junto con las API existentes para poner en cola las solicitudes para descargar datos de fuentes remotas y para controlar el proceso de descarga real.

Otras nuevas API facilitan que las aplicaciones funcionen con fuentes personalizadas que se almacenan en el sistema de archivos local o que se cargan en un búfer de memoria.

Para obtener más información sobre las nuevas API para trabajar con fuentes remotas, conjuntos de fuentes personalizados o formatos de contenedor WOFF/WOFF2, vea el tema siguiente:

[Conjuntos de fuentes personalizadas](custom-font-sets-win10.md)

Vea también los vínculos a los temas de referencia de API que se proporcionan en ese tema.  El uso de las API nuevas y existentes para trabajar con fuentes personalizadas también se muestra en el [ejemplo de conjuntos de fuentes personalizadas de DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). En este ejemplo se muestra la implementación de código para varios escenarios diferentes, como fuentes locales en disco, fuentes remotas en la web, datos de fuentes en memoria y fuentes en formatos empaquetados de WOFF o WOFF2.

### <a name="initial-support-for-opentype-font-variations"></a>Compatibilidad inicial para las variaciones de fuente OpenType

La versión 1,8 de la especificación de formato de fuente OpenType presentó una nueva extensión emocionante al formato conocido como variaciones de fuentes OpenType. DirectWrite se ha actualizado en Windows 10 Creators Update para admitir instancias con nombre de fuentes variables. Para obtener más información, consulte el siguiente tema:

[Fuentes variables OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Actualización de aniversario de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1607 (10,0; Compilación 14393) &mdash; también conocida como actualización de aniversario de Windows 10.

### <a name="improved-support-for-color-fonts"></a>Compatibilidad mejorada para las fuentes de color

A partir de la actualización de aniversario de Windows 10, DirectWrite proporciona compatibilidad integrada para una variedad más amplia de formatos de fuente de color, lo que permite a los desarrolladores usar más tipos de fuentes en sus aplicaciones basadas en DirectWrite que nunca. Esto incluye la compatibilidad para:

-   La tabla OpenType ' COLR ', que habilita el contenido de vectores compactos en las fuentes. (Se admite desde Windows 8.1).
-   La tabla OpenType ' SVG ', que habilita el contenido SVG en las fuentes.
-   La tabla OpenType ' CBDT ', que permite el contenido del mapa de bits de color en las fuentes.
-   La tabla OpenType ' sbix ', que permite el contenido del mapa de bits de color en las fuentes.

[Direct2D](../direct2d/direct2d-portal.md), que usa DirectWrite para la representación de texto, admite estos formatos de fuente de color automáticamente cuando se habilita la marca de [**\_ fuente de color D2D1 Draw \_ Text \_ \_ \_ \_ Options**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) . Para obtener más información, vea los temas siguientes:

-   [Fuentes de colores](color-fonts.md)
-   [Ejemplo de glifo de color de DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Compatibilidad con Adobe typekit y otros clientes de servicio de fuentes

Algunos servicios de fuente, como Adobe typekit, tienen utilidades del lado cliente que permiten a un usuario cargar fuentes del servicio y utilizarlas en aplicaciones diferentes en su equipo Windows. Normalmente, estas utilidades funcionan realizando llamadas en tiempo de ejecución a GDI para cargar fuentes adicionales, en lugar de instalar de forma permanente fuentes en el sistema. Debido a ese diseño, en versiones anteriores de Windows, las fuentes se pueden usar en aplicaciones basadas en GDI, pero no en aplicaciones de DirectWrite. A partir de la actualización de aniversario de Windows 10, las fuentes que cargan estas utilidades también estarán disponibles en DirectWrite y en GDI.

Las fuentes cargadas por una utilidad de servicio de fuentes están visibles en la colección de fuentes del sistema obtenida llamando al método [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Dado que los servicios de fuente suelen seguir un modelo de licencias por usuario, las fuentes cargadas por estas utilidades se administran por usuario. Como resultado, las aplicaciones de DirectWrite existentes pueden usar fuentes que los usuarios finales han obtenido mediante dichos servicios, sin necesidad de realizar cambios en el código en la aplicación, lo que proporciona una experiencia de usuario más fluida.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Compatibilidad con las colecciones OpenType mediante el esquema de CFF

Los formatos de fuente OpenType y TrueType han admitido Long para empaquetar varias fuentes en un solo archivo de fuente, conocido como "colección de fuentes". La especificación OpenType siempre ha permitido que las fuentes utilicen los formatos TrueType o CFF para los datos de contorno del glifo. Sin embargo, hasta hace poco, la especificación solo se permite para las colecciones en las que los esquemas del glifo usan el formato TrueType. La versión de OpenType 1,7 ahora permite que las colecciones usen formatos TrueType o CFF para los datos de esquema de glifos. A partir de la actualización de aniversario de Windows 10, DirectWrite admitirá las colecciones OpenType con datos de esquema CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Integración del servicio de fuentes de Windows

A partir de Windows 10, las fuentes que se incluyen con Windows están disponibles en un servicio en línea y son accesibles a través de DirectWrite en cualquier dispositivo con Windows 10. Esto se aplica a todas las ediciones de Windows 10, incluidos Windows 10 Mobile, Xbox y HoloLens, así como el cliente de escritorio. Esto permite a las aplicaciones mostrar el contenido con cualquier fuente de Windows, incluso si la fuente no está instalada actualmente en el dispositivo.

La compatibilidad con los mecanismos de servicio de fuentes de DirectWrite se ha implementado en el marco XAML, lo que significa que las aplicaciones que usan XAML no requieren cambios en el código para aprovechar el servicio de fuentes. En el [ejemplo de código fuentes descargables (XAML)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) se muestra esto. Las aplicaciones que llaman directamente a las API de DirectWrite deberán usar nuevas API para usar los mecanismos de servicio de fuentes. Para obtener más información, vea los temas siguientes:

-   [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) (método)
-   Interfaz [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   Interfaz [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   Interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

El [ejemplo de código fuentes descargables (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) muestra el uso de varias de las nuevas API.

### <a name="font-set-apis"></a>API de conjunto de fuentes

Las interfaces de colección de fuentes de DirectWrite proporcionan una vista a una colección de fuentes organizadas por familias de fuentes, con peso, ajuste y estilo como atributos de subfamilia. Internamente, DirectWrite implementa la interfaz de colección de fuentes mediante una lista plana de fuentes con varios atributos. Este enfoque es más flexible en que en puede admitir la enumeración de familias de peso/Stretch/Style, pero también puede admitir consultas y filtrados con otros atributos de fuente.

En Windows 10, este mecanismo de control de fuentes más flexible se pone a disposición de las aplicaciones a través de IDWriteFontSet y las API relacionadas. Las API del conjunto de fuentes se pueden usar, por ejemplo, para crear una interfaz de usuario personalizada del selector de fuentes que aprovecha las propiedades de fuente personalizadas de la aplicación en un conjunto de fuentes personalizado.

Para obtener más información, vea los temas siguientes:

-   Interfaz [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interfaz [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ Enumeración de \_ \_ ID. de propiedad de fuente**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   [**IDWriteFontFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) (método)

### <a name="new-text-layout-line-spacing-modes"></a>Nuevos modos de espaciado de línea de diseño de texto

Las interfaces de formato de texto y de diseño de texto de DirectWrite admiten nuevos modos de espaciado de línea. En versiones anteriores, la implementación del diseño de texto de DirectWrite permitía el espaciado de líneas en el que el alto de cada línea se estableció automáticamente según el elemento más alto de una línea (el modo "predeterminado") o el interlineado con todas las líneas establecidas en una altura uniforme determinada por la aplicación (el modo "uniforme"). En Windows 10, se admite un modo de espaciado de línea "proporcional" adicional que proporciona a las aplicaciones más opciones para el comportamiento de los espacios de línea. Para obtener más información, vea los temas siguientes:

-   Interfaz [**IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**IDWriteTextLayout3:: SetLineSpacing**](idwritetextlayout3-setlinespacing.md) (método)
-   [**DWRITE \_ Estructura de \_ espaciado de líneas**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ Enumeración del \_ \_ método de espaciado de líneas**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ Enumeración de \_ \_ \_ uso de hueco de línea de fuente**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   [**IDWriteTextLayout3:: GetLineMetrics**](idwritetextlayout3-getlinemetrics.md) (método)
-   [**DWRITE \_ Estructura \_ METRICS1 de línea**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

El [ejemplo de código de espaciado de líneas (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) muestra el uso de varias API nuevas y también proporciona una visualización de todos los distintos modos de espaciado de línea que facilitan la comprensión de las distintas opciones de espaciado de línea que están disponibles.

### <a name="gdi-interop"></a>Interoperabilidad GDI

Desde su introducción en Windows 7, DirectWrite ha proporcionado una ruta de acceso de migración para las aplicaciones que se implementaron originalmente con el modelo de fuente de GDI, el diseño y la representación de texto. Esto se proporciona a través de la \[ \[ \] \] interfaz IDWriteGdiInterop. En Windows 10, las API adicionales proporcionan capacidades adicionales de interoperabilidad de GDI. Para obtener más información, vea el tema siguiente:

-   Interfaz [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Representar fuentes de color

A partir de Windows Windows 8.1, DirectWrite proporciona compatibilidad para fuentes de color. [Direct2D](../direct2d/direct2d-portal.md), que usa DirectWrite para la representación de texto, ha agregado el valor de enumeración D2D1 \_ dibujar \_ Opciones de texto \_ \_ habilitar \_ fuente de color \_ para habilitar esta característica al dibujar texto. Para obtener más información, vea los temas siguientes:

-   [**D2D1 \_ Enumerar \_ \_ Opciones de texto de dibujo**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   [**IDWriteFactory2:: TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun) (método)

## <a name="windows-8"></a>Windows 8

Una nueva interfaz de generador, [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1), para crear interfaces adicionales disponibles.

Propiedades de fuente adicionales, como Super/subíndice, inclinación del símbolo de intercalación, Panose y rangos Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Mejoras en el espaciado, como: controlar el espaciado de caracteres, los pares de kerning heredados y la justificación. Vea el tema [justificación, interletraje y espaciado](justification--kerning--and-spacing.md) para obtener más información.

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Parámetros y destinos de representación mejorados.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Mejoras en el análisis de complejidad del texto.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Nuevas propiedades de script, nueva compatibilidad con scripts (Unicode 6), adiciones de reserva de fuentes, paréntesis emparejados y aumento bidireccional.

Mejoras en el rendimiento de la memoria caché de fuentes. A partir de Windows 8, la caché de fuentes es global y comienza cuando se inicia el equipo.

Nuevos modos de representación.

A partir de Windows 8, [DirectWrite](direct-write-portal.md) es compatible con una serie de características que le ayudarán a crear aplicaciones para el mercado mundial.

A continuación se muestran varias áreas que le ayudarán a implementar aplicaciones de texto enriquecidas que se pueden adaptar a los clientes de todo el mundo.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Extensiones de chino, Japonés y Coreano C & D

Cada pocos años, el consorcio Unicode publica una lista normalizada de adiciones a un bloque de ideogramas de chino, Japonés y coreano. Con la revisión Unicode 6,0, han liberado los bloques de extensión C y D. Estos bloques de ideogramas se pueden encontrar en la extensión de sitio web de Unicode [C](https://www.unicode.org/charts/PDF/U2A700.pdf) y la [extensión D](https://www.unicode.org/charts/PDF/U2B740.pdf).

A partir de Windows 8, [DirectWrite](direct-write-portal.md) admite los puntos de código Unicode para estos nuevos bloques de ideogramas CJK estandarizados, por lo que puede usarlos en aplicaciones de DirectWrite.

### <a name="indian-rupee-symbol"></a>Símbolo Índico India

En marzo de 2005, el gobierno indio anunció una competición para elegir un símbolo para la moneda India India. Después de mucha competición, el 15 de julio de 2010, el gobierno indio eligió el diseño creado por D. Udaya Kumar y [DirectWrite](direct-write-portal.md) incluye compatibilidad con el punto de código Unicode vinculado al símbolo. Por lo tanto, las aplicaciones de DirectWrite admiten ahora este símbolo de moneda.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) admite ahora el uso de Emoji en aplicaciones. En las versiones anteriores de DirectWrite, se presentó un cuadro de glifo que faltaba si se intentaba representar un ideograma Emoji. A partir de Windows 8, DirectWrite admite el bloque de Unicode asociado a Emoji, por lo que si la aplicación usa los puntos de código estándar de Unicode para Emoji, muestra los glifos adecuados.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Idiomas de Myanmar, Tiffinagh y hangul antiguo

A partir de Windows 8, [DirectWrite](direct-write-portal.md) admite el bloque de puntos de código Unicode que corresponden a los glifos de los idiomas de Myanmar, Tiffinagh y hangul antiguo, de modo que puede crear aplicaciones que incluyan texto de estos tres idiomas. Además de admitir estos caracteres, DirectWrite admite la única forma en que hangul anterior controla el salto de línea.

### <a name="new-scripts"></a>Nuevos scripts

A partir de Windows 8, el método [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) devuelve información de una serie de scripts nuevos. Esta es la lista de scripts que [DirectWrite](direct-write-portal.md) admite en Windows 8 y posterior.

-   Avestan
-   Bamún
-   Batak
-   Brahmi
-   Hieroglyphics egipcio
-   Aramaic imperial
-   Pahlavi de inscripción
-   Parthian de inscripción
-   Javanés
-   Kaithi
-   Lisu (Fraser)
-   Mandeo
-   Meetei Mayek
-   Árabe meridional antiguo
-   Turco antiguo (Orkhon)
-   Samaritano
-   Tai Tham (Lanna)
-   Tai Viet
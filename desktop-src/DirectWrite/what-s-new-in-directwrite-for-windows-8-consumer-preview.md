---
title: Novedades de DirectWrite
description: Estas son algunas de las nuevas adiciones a DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: 2184ce1df7a9912a67baf1e15aa8c19f6c44f300f991506c505b672025067ae4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963815"
---
# <a name="whats-new-in-directwrite"></a>Novedades de DirectWrite

En este tema se describen las novedades [de DirectWrite](direct-write-portal.md) para varias versiones de Windows 10.

## <a name="windows-app-sdk"></a>SDK para aplicaciones de Windows

El [SDK Windows App presenta](/windows/apps/windows-app-sdk/) una nueva versión de DirectWrite, denominada DWriteCore. Para obtener más información, vea [Introducción a DWriteCore.](dwritecore-overview.md)

## <a name="windows-10-may-2019-update"></a>Actualización del 10 de mayo de 2019 de Windows 2019

No se agregaron ni actualizaron características ni API para Windows 10, versión 1903 (10.0; Compilación 18362) &mdash; también conocida como Actualización de mayo de 2019 de Windows 10.

## <a name="windows-10-october-2018-update"></a>Actualización de octubre de 2018 de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1809 (10.0; Compilación 17763) &mdash; también conocida como Actualización de octubre de 2018 de Windows 10.

### <a name="new"></a>Nuevo

- [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type) enumeración
- [**Interfaz IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) y sus métodos

## <a name="windows-10-april-2018-update"></a>Actualización de abril de 2018 de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1803 (10.0; Compilación 17134) &mdash; también conocida Windows 10 actualización de abril de 2018.

### <a name="new"></a>Nuevo

- [**Interfaz IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) y sus métodos
- [**Interfaz IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) y sus métodos
- [**Interfaz IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) y sus métodos

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1709 (10.0; Compilación 16299) &mdash; también conocida como Windows 10 Fall Creators Update.

### <a name="new"></a>Nuevo

- [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes) enumeración
- [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes) enumeración
- [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag) enumeración
- [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model) enumeración
- [**Interfaz IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) y sus métodos
- [**Interfaz IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) y sus métodos
- [**Interfaz IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) y sus métodos
- [**Interfaz IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) y sus métodos
- [**Interfaz IDWriteFontFallback1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) y sus métodos
- [**Interfaz IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) y sus métodos
- [**Interfaz IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) y sus métodos
- [**Interfaz IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) y sus métodos
- [**Interfaz IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) y sus métodos
- [**Interfaz IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) y sus métodos
- [**Interfaz IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) y sus métodos
- [**Interfaz IDWriteTextLayout4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) y sus métodos
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) macro
- [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) estructura
- [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) estructura

### <a name="moved"></a>Movido

La [**DWRITE_GLYPH_IMAGE_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) enumeración se movió de `dwrite_3.h` a `dcommon.h` .

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1703 (10.0; Compilación 15063) &mdash; también conocida como Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Compatibilidad ampliada de API para fuentes en la nube y conjuntos de fuentes personalizados

Windows 10 API incluidas que permiten a las aplicaciones acceder fácilmente a las fuentes desde un Windows fuente. En el Windows 10 Creators Update, las API de fuentes remotas se amplían para permitir un acceso sencillo a fuentes de otros orígenes en la Web a las que se puede acceder mediante HTTP o HTTPS. 

Las nuevas API de fuente remota se pueden usar con servicios web públicos o privados. Además, se pueden usar para acceder a archivos de fuente OpenType sin procesar (.ttf, .otf., .ttc, .otc) o fuentes empaquetadas en formatos de contenedor [WOFF](https://www.w3.org/TR/WOFF/) o [WOFF2.](https://www.w3.org/TR/WOFF2/) Las nuevas API se usan junto con las API existentes para hacer cola de solicitudes para descargar datos de fuente remotos y para controlar el proceso de descarga real.

Otras NUEVAS API facilitan que las aplicaciones funcionen con fuentes personalizadas que están almacenadas en el sistema de archivos local o que se cargan en un búfer de memoria.

Para obtener más información sobre las nuevas API para trabajar con fuentes remotas, conjuntos de fuentes personalizados o formatos de contenedor WOFF/WOFF2, vea el tema siguiente:

[Conjuntos de fuentes personalizadas](custom-font-sets-win10.md)

Consulte también los vínculos a los temas de referencia de API que se proporcionan en ese tema.  El uso de API nuevas y existentes para trabajar con fuentes personalizadas también se muestra en el ejemplo DirectWrite de conjuntos de fuentes [personalizados](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). En este ejemplo se muestra la implementación de código para varios escenarios diferentes, como fuentes locales en disco, fuentes remotas en la Web, datos de fuentes en memoria y fuentes en formatos WOFF o WOFF2 empaquetados.

### <a name="initial-support-for-opentype-font-variations"></a>Compatibilidad inicial con variaciones de fuente OpenType

La versión 1.8 de la especificación de formato de fuente OpenType introdujo una nueva extensión interesante para el formato conocido como Variaciones de fuente OpenType. DirectWrite se ha actualizado en el Windows 10 Creators Update para admitir instancias con nombre de fuentes de variables. Para obtener más información, consulte el siguiente tema:

[Fuentes variables OpenType](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Actualización de aniversario de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10, versión 1607 (10.0; Compilación 14393) &mdash; también conocida como actualización Windows 10 aniversario.

### <a name="improved-support-for-color-fonts"></a>Compatibilidad mejorada para las fuentes de color

A partir de la actualización de aniversario de Windows 10, DirectWrite proporciona compatibilidad integrada con una amplia variedad de formatos de fuente de color, lo que permite a los desarrolladores usar más tipos de fuentes en sus aplicaciones con tecnología DirectWrite que nunca. Esto incluye la compatibilidad para:

-   La tabla OpenType "COLR", que permite el contenido vectorial compacto en las fuentes. (Se admite desde Windows 8.1).
-   La tabla OpenType "SVG", que habilita el contenido SVG en las fuentes.
-   La tabla OpenType 'EDITABLET', que permite el contenido de mapa de bits de color en las fuentes.
-   La tabla OpenType "sbix", que permite el contenido de mapa de bits de color en las fuentes.

[Direct2D,](../direct2d/direct2d-portal.md)que usa DirectWrite para la representación de texto, admite estos formatos de fuente de color automáticamente cuando la marca [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) está habilitada. Para obtener más información, vea los temas siguientes:

-   [Fuentes de colores](color-fonts.md)
-   [DirectWrite de glifo de color](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Compatibilidad con Adobe Typekit y otros clientes de servicio de fuentes

Algunos servicios de fuente, como Adobe Typekit, tienen utilidades del lado cliente que permiten a un usuario cargar fuentes desde el servicio y usarlas en distintas aplicaciones en Windows máquina. Normalmente, estas utilidades funcionan mediante llamadas en tiempo de ejecución a GDI para cargar fuentes adicionales, en lugar de instalar fuentes de forma permanente en el sistema. Debido a ese diseño, en versiones anteriores Windows, las fuentes se pueden usar en aplicaciones basadas en GDI, pero no en DirectWrite aplicaciones. A partir de la Windows 10 de aniversario, las fuentes cargadas por estas utilidades también estarán disponibles en DirectWrite y en GDI.

Las fuentes cargadas por una utilidad de servicio de fuentes son visibles en la colección de fuentes del sistema obtenida mediante una llamada al [**método IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Dado que los servicios de fuentes suelen seguir un modelo de licencias por usuario, las fuentes cargadas por estas utilidades se administran por usuario. Como resultado, las aplicaciones de DirectWrite existentes pueden usar fuentes que los usuarios finales han obtenido mediante estos servicios, sin necesidad de realizar cambios en el código en la aplicación, lo que proporciona una experiencia más fluida para los usuarios.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Compatibilidad con colecciones OpenType mediante esquemas CFF

Los formatos de fuente OpenType y TrueType admiten desde hace tiempo la capacidad de empaquetar varias fuentes en un único archivo de fuente, conocido como "colección de fuentes". La especificación OpenType siempre ha permitido que las fuentes usen formatos TrueType o CFF para los datos de esquema de glifo. Sin embargo, hasta hace poco, la especificación solo permitía colecciones en las que los contornos de glifo usan el formato TrueType. La versión 1.7 de OpenType ahora permite que las colecciones usen formatos TrueType o CFF para los datos de esquema del glifo. A partir de la Windows 10 de aniversario, DirectWrite admitirá colecciones OpenType mediante datos de esquema CFF.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Windows integración del servicio de fuentes

A partir Windows 10, las fuentes que se incluyen con Windows están disponibles en un servicio en línea y son accesibles a través de DirectWrite en cualquier Windows 10 dispositivo. Esto se aplica a todas las Windows 10, incluidos Windows 10 Mobile, Xbox y HoloLens, así como al cliente de escritorio. Esto permite a las aplicaciones mostrar contenido con cualquier Windows fuente, incluso si la fuente no está instalada actualmente en el dispositivo.

La compatibilidad con DirectWrite de servicio de fuentes se ha implementado en el marco XAML, lo que significa que las aplicaciones que usan XAML no requieren ningún cambio de código para aprovechar las ventajas del servicio de fuentes. El ejemplo de código Fuentes descargables [(XAML)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) muestra esto. Las aplicaciones que llaman DirectWrite API directamente tendrán que usar nuevas API para usar los mecanismos de servicio de fuentes. Para obtener más información, vea los temas siguientes:

-   [**Método IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection)
-   [**Interfaz IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**Interfaz IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   [**Interfaz IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

El ejemplo de código Fuentes descargables [(DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) muestra el uso de varias de las nuevas API.

### <a name="font-set-apis"></a>API de conjunto de fuentes

las interfaces de colección de fuentes de DirectWrite proporcionan una vista a una colección de fuentes organizadas por familias de fuentes, usando el peso, el stretch y el estilo como atributos de subliblio. Internamente, DirectWrite la interfaz de colección de fuentes mediante una lista plana de fuentes con varios atributos. Este enfoque es más flexible, ya que en puede admitir la enumeración de familias de peso, extensión y estilo, pero también puede admitir la consulta y el filtrado mediante otros atributos de fuente.

En Windows 10, este mecanismo de control de fuentes más flexible está disponible para las aplicaciones a través de IDWriteFontSet y las API relacionadas. Las API del conjunto de fuentes se pueden usar, por ejemplo, para crear una interfaz de usuario de selector de fuentes personalizada que aproveche las propiedades de fuente personalizadas de la aplicación en un conjunto de fuentes personalizado.

Para obtener más información, vea los temas siguientes:

-   [**Interfaz IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**Interfaz IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ Enumeración FONT \_ PROPERTY \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   [**Método IDWriteFontFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset)

### <a name="new-text-layout-line-spacing-modes"></a>Nuevos modos de espaciado de línea de diseño de texto

DirectWrite el formato de texto y las interfaces de diseño de texto admiten nuevos modos de espaciado de línea. En versiones anteriores, la implementación de diseño de texto de DirectWrite permitía el espaciado de línea en el que el alto de cada línea se estableció automáticamente en función del elemento más alto dentro de una línea (el modo "predeterminado"), o el espaciado de línea con todas las líneas establecidas en un alto uniforme determinado por la aplicación (el modo "uniforme"). En Windows 10, se admite un modo de espaciado de línea "proporcional" adicional que proporciona a las aplicaciones más opciones para el comportamiento del espaciado de línea. Para obtener más información, vea los temas siguientes:

-   [**Interfaz IDWriteTextLayout3**](idwritetextlayout3.md)
-   [**Método IDWriteTextLayout3::SetLineSpacing**](idwritetextlayout3-setlinespacing.md)
-   [**DWRITE \_ ESTRUCTURA \_ ESPACIADO DE LÍNEA**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ ENUMERACIÓN \_ LINE SPACING \_ METHOD**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ Enumeración FONT \_ LINE \_ GAP \_ USAGE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   [**Método IDWriteTextLayout3::GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)
-   [**DWRITE \_ Estructura LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

El ejemplo de código Espaciado de línea [(DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) muestra el uso de varias de las nuevas API y también proporciona una visualización de todos los distintos modos de espaciado de línea que facilita mucho más la información sobre las distintas opciones de espaciado de línea disponibles.

### <a name="gdi-interop"></a>Interoperabilidad GDI

Desde su introducción en Windows 7, DirectWrite ha proporcionado una ruta de migración para las aplicaciones que se implementaron originalmente mediante el modelo de fuente, el diseño y la representación de texto de GDI. Esto se proporcionó a través de la \[ \[ interfaz IDWriteGdiInterop. \] \] En Windows 10, las API adicionales proporcionan funcionalidades de interoperabilidad GDI adicionales. Para obtener información adicional, vea el tema siguiente:

-   [**Interfaz IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Representación de fuentes de color

A partir de Windows Windows 8.1, DirectWrite admite las fuentes de color. [Direct2D,](../direct2d/direct2d-portal.md)que usa DirectWrite para la representación de texto, ha agregado el valor de enumeración D2D1 DRAW TEXT OPTIONS ENABLE COLOR FONT para habilitar esta característica al dibujar \_ \_ \_ \_ \_ \_ texto. Para obtener más información, vea los temas siguientes:

-   [**D2D1 \_ Draw \_ TEXT \_ OPTIONS (enumeración)**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   [**Método IDWriteFactory2::TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)

## <a name="windows-8"></a>Windows 8

Una nueva interfaz de generador, [**IDWriteFactory1,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)para crear interfaces adicionales disponibles.

Propiedades de fuente adicionales, como: super/subíndice, pendiente de símbolos de cargo, PANOSE e intervalos Unicode.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Mejoras de espaciado, como: controlar el espaciado de caracteres, los pares de kerning heredados y la justificación. Consulte el [tema Justification, Kerning, and Spacing (Justificación, kerning y](justification--kerning--and-spacing.md) espaciado) para obtener más información.

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Parámetros y destinos de representación mejorados.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Mejoras en el análisis de complejidad del texto.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Nuevas propiedades de script, nueva compatibilidad con scripts (Unicode 6), adiciones de reserva de fuentes, paréntesis emparejados y aumento de bidi.

Mejoras en el rendimiento de la caché de fuentes. A partir Windows 8 la caché de fuentes es global y se inicia cuando se inicia el equipo.

Nuevos modos de representación.

A partir Windows 8, [DirectWrite](direct-write-portal.md) admite una serie de características que le ayudan a crear aplicaciones para el mercado mundial.

Estas son varias áreas que le ayudan a implementar aplicaciones de texto enriquecido que se pueden adaptar a clientes de todo el mundo.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Extensiones de chino, japonés y coreano C & D

Cada pocos años, Unicode Consortium publica una lista estandarizada de adiciones al bloque ideograma unificado chino, japonés y coreano. Con la revisión Unicode 6.0, han publicado los bloques de extensión C y D. Estos bloques de ideogramas se pueden encontrar en la extensión [C](https://www.unicode.org/charts/PDF/U2A700.pdf) y la extensión D del sitio web [Unicode.](https://www.unicode.org/charts/PDF/U2B740.pdf)

A partir de Windows 8, [DirectWrite](direct-write-portal.md) admite los puntos de código Unicode para estos nuevos bloques de ideogramas CJK estandarizados, por lo que puede usarlos en DirectWrite aplicaciones.

### <a name="indian-rupee-symbol"></a>Símbolo rupia india

En marzo de 2005, el gobierno de la India anunció una competición para elegir un símbolo para la moneda rupia india. Después de una gran competencia, el 15 de julio de 2010, el gobierno de la India eligió el diseño creado por D. Udrada Kumar y [DirectWrite](direct-write-portal.md) incluye compatibilidad con el punto de código Unicode vinculado al símbolo. Por lo tanto, DirectWrite aplicaciones ahora admiten este símbolo de moneda.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) ahora admite el uso de emojis en las aplicaciones. Las versiones anteriores de DirectWrite, que presentaban un cuadro de glifo que faltaba si se intentaba representar un ideograma de emoji. A partir Windows 8, DirectWrite admite el bloque de código Unicode asociado a emoji, por lo que si la aplicación usa los puntos de código estándar Unicode para el emoji, muestra los glifos adecuados.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Idiomas de Hangul antiguo, Tiffinagh y Tiffinagh

A partir de Windows 8, [DirectWrite](direct-write-portal.md) admite el bloque de puntos de código Unicode que se corresponden con los glifos de los idiomas Unicode, Tiffinagh y Hangul antiguo, por lo que puede crear aplicaciones que incluyan texto de estos tres idiomas. Además de admitir estos caracteres, DirectWrite admite la forma única en que Old Hangul controla la separación de líneas.

### <a name="new-scripts"></a>Nuevos scripts

A partir Windows 8, el [**método GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) devuelve información para varios scripts nuevos. Esta es la lista de scripts que [DirectWrite](direct-write-portal.md) admite en Windows 8 y después.

-   Semán
-   Bamum
-   Batak
-   Brahmi
-   Hierogly svcs insondez
-   Querón Aramic
-   Pahlavi desenlazador
-   Parthian inerte
-   Javanés
-   Thi
-   Lisu (Fraser)
-   Obligaic
-   Meetei Mayek
-   Antiguo Sur de Corea del Sur
-   Turco antiguo (Orkhon)
-   Samaritano
-   Tai Tham (Lamira)
-   Tai Viet

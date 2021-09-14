---
title: Representación de texto con Direct2D y DirectWrite
description: A diferencia de otras API, como GDI, GDI+ o WPF, Direct2D interopera con otra API, DirectWrite, para manipular y representar texto. En este tema se describen las ventajas y la interoperación de estos componentes independientes.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c49a8f341377bcf78a9a99699a3bd4852411dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163401"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Representación de texto con Direct2D y DirectWrite

A diferencia de otras API, como [GDI](/windows/desktop/gdi/windows-gdi), GDI+ o WPF, [Direct2D](./direct2d-portal.md) interopera con otra API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), para manipular y representar texto. En este tema se describen las ventajas y la interoperación de estos componentes independientes.

En este tema se incluyen las siguientes secciones.

-   [Direct2D habilita la adopción incremental](#direct2d-enables-incremental-adoption)
-   [Servicios de texto frente a representación de texto](#text-services-versus-text-rendering)
-   [Glifos frente a texto](#glyphs-versus-text)
-   [DirectWrite y Direct2D](#directwrite-and-direct2d)
    -   [Drawtext](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Representación de glifos](#glyph-rendering)
-   [Conclusión](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D habilita la adopción incremental

Mover una aplicación de una API de gráficos a otra puede ser difícil o no lo que desea por varias razones. Esto puede deberse a que tiene que admitir complementos que todavía toman las interfaces anteriores, porque la propia aplicación es demasiado grande para portabilidad a una nueva API en una versión o porque alguna parte de la API más reciente es deseable, pero la API anterior funciona lo suficientemente bien para otras partes de la aplicación.

Dado [que Direct2D](./direct2d-portal.md) [y DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) se implementan como componentes independientes, puede actualizar todo el sistema de gráficos 2D o solo la parte de texto de él. Por ejemplo, podría actualizar una aplicación para usar DirectWrite texto pero seguir utilizando [GDI](/windows/desktop/gdi/windows-gdi) o GDI+ para la representación.

## <a name="text-services-versus-text-rendering"></a>Servicios de texto frente a representación de texto

A medida que las aplicaciones han evolucionado, sus requisitos de procesamiento de texto se han vuelto cada vez más complejos. Al principio, el texto se limitaba por lo general a la interfaz de usuario de diseño estático y el texto se representaba en un cuadro bien definido, como un botón. A medida que las aplicaciones empezaron a estar disponibles en un número creciente de idiomas, este enfoque se volvió más difícil de mantener porque tanto el ancho como el alto del texto traducido pueden variar significativamente entre los idiomas. Para adaptarse, las aplicaciones empezaron a crear dinámicamente su interfaz de usuario para que dependa del tamaño real representado del texto, en lugar de al revés.

Para ayudar a las aplicaciones a completar esta [tarea, DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) proporciona la [**interfaz IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) Esta API permite a una aplicación especificar un fragmento de texto con características complejas, como diferentes fuentes y tamaños de fuente, subrayados, tachados, texto bidireccional, efectos, puntos suspensivos e incluso caracteres no glifo incrustados (como un emoji de mapa de bits o un icono). A continuación, la aplicación puede cambiar varias características del texto a medida que determina iterativamente su diseño de interfaz de usuario. El [DirectWrite Hola mundo ejemplo](/samples/browse/?redirectedfrom=MSDN-samples), que se muestra en la siguiente ilustración y en el [tutorial: Tareas iniciales con DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) tema, muestra muchos de estos efectos.

![captura de pantalla del ejemplo "Hola mundo".](images/dwrite-hello-world.png)

El diseño puede colocar los glifos idealmente en función de sus anchos (como hace WPF), o puede ajustar los glifos a las posiciones de píxel más cercanas (como [hace GDI).](/windows/desktop/gdi/windows-gdi)

Además de obtener medidas de texto, la aplicación puede probar varias partes del texto. Por ejemplo, es posible que quiera saber que se hace clic en un hipervínculo del texto. (Para obtener más información sobre las pruebas de acceso, vea el tema Cómo realizar pruebas [de acceso en un diseño de](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) texto).

La interfaz de diseño de texto se desacopla de la API de representación que usa la aplicación, como se muestra en el diagrama siguiente:

![diagrama de api de gráficos y diseño de texto.](images/direct2d-directwrite1.png)

Esta separación es posible porque DirectWrite proporciona una interfaz de representación [**(IDWriteTextRenderer)**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)que las aplicaciones pueden implementar para representar texto mediante la API de gráficos que desee. La aplicación implementó el método de devolución de llamada [**IDWriteTextRenderer::D rawGlyph DirectWrite Run**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) al representar un diseño de texto. Es responsabilidad de este método realizar las operaciones de dibujo o pasarlas.

Para dibujar glifos, [Direct2D](./direct2d-portal.md) proporciona [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para dibujar en una superficie de Direct2D y [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) proporciona [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar en una superficie GDI que luego se puede transferir a una ventana mediante GDI. Cómodamente, **DrawGlyphRun** en Direct2D y DirectWrite tienen parámetros exactamente compatibles con el método [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) que la aplicación implementa en [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

Después de una separación similar, las características específicas del texto (como la enumeración y administración de fuentes, el análisis de glifos, entre otros) se controlan mediante DirectWrite [en](/windows/desktop/DirectWrite/direct-write-portal) lugar de [Direct2D](./direct2d-portal.md). Direct2D acepta directamente los objetos DirectWrite datos. Para ayudar a las aplicaciones GDI existentes a aprovechar las ventajas de DirectWrite, proporciona la interfaz de método [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) con métodos para hacer lo siguiente:

-   Cree una [fuente DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a partir de una fuente [lógica GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Convertir de una [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) de fuente a una fuente [lógica GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Recupere el [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) font face del que se selecciona en un HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Cree un destino [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**de representación de mapa de**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) bits en la memoria del sistema ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glifos frente a texto

El texto es un conjunto de puntos de código Unicode (caracteres), con varios modificadores estilísticos (fuentes, pesos, subrayados, tachados, entre otros) que se disponen en un rectángulo. Un glifo, en cambio, es un índice determinado en un archivo de fuente determinado. Un glifo define un conjunto de curvas que se pueden representar, pero no tiene ningún significado textual. Existe potencialmente una asignación de varios a varios entre glifos y caracteres. Una secuencia de glifos que proceden de la misma cara de fuente y que se disponen secuencialmente en una línea base se denomina [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). Tanto [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) como [Direct2D](./direct2d-portal.md) llaman a su API [**drawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) de representación de glifos más precisa y tienen firmas muy similares. Lo siguiente es de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) en Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Y este método es de [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) [en DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



La [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) mantiene el origen de línea base, el modo de medición y los parámetros de ejecución del glifo e incluye parámetros adicionales.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) también permite usar un representador personalizado para glifos mediante la implementación de la [**interfaz IDWriteTextRenderer.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) Esta interfaz también tiene un **método DrawGlyphRun,** como se muestra en el ejemplo de código siguiente.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Esta versión incluye más parámetros que son útiles al implementar un [representador de texto personalizado.](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) El parámetro final se usa para los efectos de dibujo personalizados implementados por la aplicación. (Para obtener más información sobre los efectos de dibujo de cliente, [vea How to Add Client Drawing Effects to a Text Layout](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Cada ejecución de glifo se inicia en un origen y se coloca en una línea a partir de este origen. La transformación del mundo actual y la configuración de representación de texto seleccionada en el destino de representación asociado cambian los glifos. Normalmente, solo las aplicaciones que hacen su propio diseño (por ejemplo, un procesador de palabras) o una aplicación que ha implementado la interfaz [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) suelen llamar directamente a esta API.

## <a name="directwrite-and-direct2d"></a>DirectWrite y Direct2D

[Direct2D proporciona](./direct2d-portal.md) servicios de representación de nivel de glifo [**a través de DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Sin embargo, esto requiere que la aplicación implemente los detalles de la representación, que básicamente reproduce la funcionalidad de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) API desde GDI por sí misma.

Por lo tanto, [Direct2D](./direct2d-portal.md) proporciona API que aceptan texto en lugar de glifos: [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) e [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Ambos métodos se representan en una superficie de Direct2D. Para representar en una superficie GDI, se proporciona [**IDWriteBitmapRenderTarget::D rawGlyphRun.**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Pero este método requiere que la aplicación implemente un representador de texto personalizado. (Para obtener más información, vea el tema [Representación en una superficie GDI).](/windows/desktop/DirectWrite/render-to-a-gdi-surface)

Normalmente, el uso de texto de una aplicación se inicia de forma sencilla: ponga **Aceptar** o **Cancelar en** un botón de diseño fijo, por ejemplo. Sin embargo, con el tiempo, se vuelve más compleja a medida que se agrega la internacionalización y otras características. Finalmente, muchas aplicaciones tendrán que [usar DirectWrite de diseño](/windows/desktop/DirectWrite/direct-write-portal) de texto e implementar el representador de texto.

Por lo tanto, [Direct2D](./direct2d-portal.md) proporciona API por capas que permiten que una aplicación se inicie simplemente y se vuelva más sofisticada sin tener que realizar un seguimiento o abandonar su código de trabajo. En el diagrama siguiente se muestra una vista simplificada:

![Diagrama de aplicaciones directwrite y direct2d.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>Drawtext

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) es la api más sencilla de usar. Toma una cadena Unicode, un pincel de primer plano, un objeto de formato único y un rectángulo de destino. Se delimitará y representará toda la cadena dentro del rectángulo de diseño y, opcionalmente, se recortará. Esto resulta útil cuando se coloca un fragmento de texto simple en una parte de la interfaz de usuario de diseño fijo.

### <a name="drawtextlayout"></a>DrawTextLayout

Al crear un objeto [**IDWriteTextLayout,**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) una aplicación puede empezar a medir y organizar el texto y otros elementos de la interfaz de usuario, y admitir varias fuentes, estilos, subrayados y tachados. [Direct2D proporciona](./direct2d-portal.md) la API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) que acepta directamente este objeto y representa el texto en un punto determinado. (El ancho y alto los proporciona el objeto de diseño). Además de implementar todas las características de diseño de texto esperadas, Direct2D interpretará cualquier objeto de efecto como un pincel y aplicará ese pincel al intervalo de glifos seleccionado. También llamará a cualquier objeto en línea. A continuación, una aplicación puede insertar caracteres no glifo (iconos) en el texto si lo desea. Otra ventaja de usar un objeto de diseño de texto es que las posiciones del glifo se almacenan en caché en él. Por lo tanto, es posible una gran ganancia de rendimiento al volver a usar el mismo objeto de diseño para varias llamadas a draw y evitar volver a calcular las posiciones del glifo para cada llamada. Esta funcionalidad no está presente para [**DrawText de**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Por último, la aplicación puede implementar la propia interfaz [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) y llamar a [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) y [**FillRectangle,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) o a cualquier otra API de representación. Toda la interacción existente con el objeto Text Layout permanecerá sin cambios.

Para obtener un ejemplo de cómo implementar un representador de texto personalizado, vea el tema [Representación mediante un representador de texto](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) personalizado.

## <a name="glyph-rendering"></a>Representación de glifos

Agregar [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a una aplicación GDI existente permite a la aplicación usar la API [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) para representar glifos. El [**método IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) que proporciona DirectWrite se representará en color sólido en un controlador de dominio de memoria sin necesidad de API adicionales, como [Direct2D.](./direct2d-portal.md)

Esto permite a la aplicación obtener características avanzadas de representación de texto como las siguientes:

-   ClearType de subpíxeles permite que una aplicación coloque glifos en posiciones de subpíxeles para permitir la representación de glifos nítidos y el diseño del glifo.
-   El suavizado de contorno de dirección Y permite una representación más fluida de curvas en glifos más grandes.

Una aplicación que se mueva [a Direct2D](./direct2d-portal.md) también obtendrá las siguientes características:

-   Aceleración de hardware.
-   La capacidad de rellenar texto con un pincel [direct2D](./direct2d-portal.md) arbitrario, como degradados radiales, degradados lineales y mapas de bits.
-   Más compatibilidad con la creación de capas y el recorte a través de las API [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)), [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))
-   La capacidad de admitir la representación de texto de escala de grises. Esto rellena correctamente el canal alfa de destino según la opacidad del pincel de texto y el suavizado de contorno del texto.

Para admitir de forma eficaz la aceleración de hardware, [Direct2D](./direct2d-portal.md) usa una aproximación ligeramente diferente a la corrección Gamma denominada *corrección alfa*. Esto no requiere Direct2D para inspeccionar el píxel de color del destino de representación al representar texto.

## <a name="conclusion"></a>Conclusión

En este tema se explican las diferencias y similitudes entre [Direct2D](./direct2d-portal.md) [y DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) y las motivaciones arquitectónicas para proporcionarlas como API cooperativas independientes.

 

 
---
title: Representación de texto con Direct2D y DirectWrite
description: A diferencia de otras API, como GDI, GDI+ o WPF, Direct2D interopera con otra API, DirectWrite, para manipular y representar texto. En este tema se describen las ventajas y la interoperabilidad de estos componentes independientes.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c49a8f341377bcf78a9a99699a3bd4852411dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567528"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Representación de texto con Direct2D y DirectWrite

A diferencia de otras API, como [GDI](/windows/desktop/gdi/windows-gdi), GDI+ o WPF, [Direct2D](./direct2d-portal.md) interopera con otra API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), para manipular y representar texto. En este tema se describen las ventajas y la interoperabilidad de estos componentes independientes.

En este tema se incluyen las siguientes secciones.

-   [Direct2D permite la adopción incremental](#direct2d-enables-incremental-adoption)
-   [Servicios de texto frente a representación de texto](#text-services-versus-text-rendering)
-   [Glifos frente a texto](#glyphs-versus-text)
-   [DirectWrite y Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Representación de glifos](#glyph-rendering)
-   [Conclusión](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D permite la adopción incremental

Mover una aplicación de una API de gráficos a otra puede ser difícil o no lo que desea por varias razones. Esto puede deberse a que tiene que admitir complementos que siguen teniendo las interfaces más antiguas, porque la propia aplicación es demasiado grande para migrar a una nueva API en una versión o porque se desea una parte de la API más reciente, pero la API anterior funciona lo suficiente para otras partes de la aplicación.

Dado que [Direct2D](./direct2d-portal.md) y [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) se implementan como componentes independientes, puede actualizar todo el sistema de gráficos 2D o simplemente la parte de texto de este. Por ejemplo, puede actualizar una aplicación para usar DirectWrite para el texto pero seguir usando [GDI](/windows/desktop/gdi/windows-gdi) o GDI+ para la representación.

## <a name="text-services-versus-text-rendering"></a>Servicios de texto frente a representación de texto

A medida que las aplicaciones han evolucionado, sus requisitos de procesamiento de texto han crecido cada vez más complejos. En primer lugar, el texto se limitó a la interfaz de usuario de forma estática y el texto se representó en un cuadro bien definido, como un botón. A medida que las aplicaciones empezaron a estar disponibles en un número cada vez mayor de lenguajes, este enfoque resultaba más difícil de sostener porque el ancho y el alto del texto traducido pueden variar significativamente entre los lenguajes. Para adaptarse, las aplicaciones empezaron a diseñar dinámicamente su interfaz de usuario para depender del tamaño representado real del texto, en lugar de hacerlo de otra manera.

Para ayudar a las aplicaciones a completar esta tarea, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) proporciona la interfaz [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Esta API permite a una aplicación especificar un fragmento de texto con características complejas, como fuentes y tamaños de fuente diferentes, subrayados, tachados, texto bidireccional, efectos, puntos suspensivos e incluso caracteres no glifos incrustados (como un emoticono de mapa de bits o un icono). A continuación, la aplicación puede cambiar varias características del texto a medida que determina de forma iterativa su diseño de la interfaz de usuario. En el [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples), que se muestra en la siguiente ilustración y en el tema [Tutorial: introducción con DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) , se muestran muchos de estos efectos.

![captura de pantalla del ejemplo "Hello World".](images/dwrite-hello-world.png)

El diseño puede ubicar los glifos idealmente en función de sus anchos (a medida que lo hace WPF), o bien puede ajustar los glifos a las posiciones de píxel más cercanas (como hace [GDI](/windows/desktop/gdi/windows-gdi) ).

Además de obtener las medidas de texto, la aplicación puede hacer una prueba de posicionamiento de varias partes del texto. Por ejemplo, puede que desee saber que se hace clic en un hipervínculo en el texto. (Para obtener más información acerca de las pruebas de posicionamiento, vea el tema [Cómo realizar pruebas de posicionamiento en un diseño de texto](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) ).

La interfaz de diseño de texto está desacoplada de la API de representación que usa la aplicación, como se muestra en el diagrama siguiente:

![diagrama de diseño de texto y de API de gráficos.](images/direct2d-directwrite1.png)

Esta separación es posible porque DirectWrite proporciona una interfaz de representación ([**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) que las aplicaciones pueden implementar para representar texto con cualquier API de gráficos que desee. DirectWrite ha implementado la aplicación [**IDWriteTextRenderer::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) método de devolución de llamada al representar un diseño de texto. Es responsabilidad de este método realizar las operaciones de dibujo o pasarlas.

En el caso de los glifos de dibujo, [Direct2D](./direct2d-portal.md) proporciona [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para dibujar en una superficie de Direct2D y [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) proporciona [**IDWriteBitmapRenderTarget::D RAWGLYPHRUN**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar en una superficie de GDI que se puede transferir a una ventana mediante GDI. Como es conveniente, **DrawGlyphRun** en Direct2D y en DirectWrite tienen parámetros exactamente compatibles con el método [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) que la aplicación implementa en [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

Tras una separación similar, las características específicas del texto (como la enumeración y administración de fuentes, el análisis de glifos, etc.) se controlan mediante [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) en lugar de [Direct2D](./direct2d-portal.md). Los objetos de DirectWrite se aceptan directamente mediante Direct2D. Para ayudar a las aplicaciones GDI existentes a aprovechar las ventajas de DirectWrite, proporciona la interfaz del método [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) con métodos para hacer lo siguiente:

-   Cree una fuente [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a partir de una fuente lógica de [GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Convertir un tipo de fuente de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) en una fuente lógica de [GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Recupera el tipo de fuente [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) de la que se selecciona en una HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Cree un [](/windows/desktop/DirectWrite/direct-write-portal) [**destino de representación de mapa de bits**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) de DirectWrite en la memoria del sistema ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glifos frente a texto

El texto es un conjunto de puntos de código Unicode (caracteres), con distintos modificadores de estilo (fuentes, pesos, subrayados, tachados, etc.) que se colocan en un rectángulo. En cambio, un glifo es un índice determinado en un archivo de fuente determinado. Un glifo define un conjunto de curvas que se pueden representar, pero no tiene ningún significado textual. Existe una asignación de varios a varios entre glifos y caracteres. Una secuencia de glifos que provienen de la misma fuente y que se colocan secuencialmente en una línea base se denomina [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). Tanto [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) como [Direct2D](./direct2d-portal.md) llaman a su [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) de API de representación de glifos más precisa y tienen firmas muy similares. A continuación se indican los elementos de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) en Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Y este método es de [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) en [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


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



La versión de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) mantiene el origen de la línea base, el modo de medición y los parámetros de ejecución del glifo, e incluye parámetros adicionales.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) también le permite usar un representador personalizado para los glifos implementando la interfaz [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) . Esta interfaz también tiene un método **DrawGlyphRun** , como se muestra en el ejemplo de código siguiente.


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



Esta versión incluye más parámetros que son útiles cuando se implementa un [representador de texto personalizado](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer). El parámetro final se usa para los efectos de dibujo personalizados implementados por la aplicación. (Para obtener más información sobre los efectos de dibujo de cliente, vea [Cómo agregar efectos de dibujo de cliente a un diseño de texto](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Cada ejecución del glifo comienza en un origen y se coloca en una línea a partir de este origen. La transformación mundo actual modifica los glifos y la configuración de representación de texto seleccionada en el destino de representación asociado. Normalmente, solo se llama a esta API directamente en las aplicaciones que realizan su propio diseño (por ejemplo, un procesador de textos) o una aplicación que ha implementado la interfaz [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) .

## <a name="directwrite-and-direct2d"></a>DirectWrite y Direct2D

[Direct2D](./direct2d-portal.md) proporciona servicios de representación de nivel de glifo a través de [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Sin embargo, esto requiere que la aplicación implemente los detalles de la representación, que básicamente reproduce la funcionalidad de la API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) de GDI por sí misma.

Por lo tanto, [Direct2D](./direct2d-portal.md) proporciona las API que aceptan texto en lugar de los glifos: [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) y [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Ambos métodos se representan en una superficie de Direct2D. Para representar en una superficie de GDI, se proporciona [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) . Pero este método requiere que la aplicación implemente un representador de texto personalizado. (Para obtener más información, vea el tema [representar en una superficie de GDI](/windows/desktop/DirectWrite/render-to-a-gdi-surface) ).

El uso de texto de una aplicación suele iniciarse de forma simple: colocar **Aceptar** o **Cancelar** en un botón de diseño fijo, por ejemplo. Sin embargo, con el tiempo, es más complejo a medida que se agregan internacionalización y otras características. Finalmente, muchas aplicaciones tendrán que usar los objetos [de diseño de texto de DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e implementar el representador de texto.

Por lo tanto, [Direct2D](./direct2d-portal.md) proporciona API en capas que permiten que una aplicación se inicie simplemente y crezca más sofisticada sin tener que hacer un seguimiento del código de trabajo ni abandonarlo. En el diagrama siguiente se muestra una vista simplificada:

![diagrama de aplicaciones de directwrite y direct2d.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) es la más sencilla de las API que se usan. Toma una cadena Unicode, un pincel de primer plano, un objeto de formato único y un rectángulo de destino. Diseñará y procesará toda la cadena dentro del rectángulo de diseño y, opcionalmente, la recortará. Esto resulta útil cuando se coloca un fragmento de texto simple en una parte de la interfaz de usuario de diseño fijo.

### <a name="drawtextlayout"></a>DrawTextLayout

Al crear un objeto [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) , una aplicación puede empezar a medir y organizar el texto y otros elementos de la interfaz de usuario, además de admitir varias fuentes, estilos, subrayados y tachados. [Direct2D](./direct2d-portal.md) proporciona la API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) que acepta directamente este objeto y representa el texto en un punto determinado. (El objeto de diseño proporciona el ancho y el alto). Además de implementar todas las características de diseño de texto esperadas, Direct2D interpretará cualquier objeto de efecto como un pincel y aplicará ese pincel al intervalo de glifos seleccionado. También llamará a todos los objetos insertados. Después, una aplicación puede insertar caracteres que no sean glifos (iconos) en el texto si así lo desea. Otra ventaja de usar un objeto de diseño de texto es que las posiciones del glifo se almacenan en la memoria caché. Por lo tanto, es posible una gran mejora del rendimiento si se vuelve a usar el mismo objeto de diseño para varias llamadas a Draw y se evita volver a calcular las posiciones del glifo para cada llamada. Esta funcionalidad no está presente para [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))de GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Por último, la aplicación puede implementar la propia interfaz [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) y llamar a [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) y [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) , o a cualquier otra API de representación. Toda la interacción existente con el objeto de diseño de texto permanecerá sin cambios.

Para obtener un ejemplo de cómo implementar un representador de texto personalizado, vea el tema [representar mediante un representador de texto personalizado](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) .

## <a name="glyph-rendering"></a>Representación de glifos

Agregar [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a una aplicación GDI existente permite que la aplicación use la API de [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) para representar glifos. El método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) que proporciona DirectWrite se representará en color sólido para un DC de memoria sin necesidad de ninguna API adicional, como [Direct2D](./direct2d-portal.md).

Esto permite a la aplicación obtener características de representación de texto avanzadas, como las siguientes:

-   ClearType de subpíxeles permite a una aplicación colocar glifos en posiciones de subpíxeles para permitir la representación de glifos nítida y el diseño del glifo.
-   El suavizado de contorno de la dirección Y permite una representación más fluida de las curvas en glifos más grandes.

Una aplicación que se mueva a [Direct2D](./direct2d-portal.md) también obtendrá las siguientes características:

-   Aceleración de hardware.
-   La capacidad de rellenar texto con un pincel de [Direct2D](./direct2d-portal.md) arbitrario, como degradados radiales, degradados lineales y mapas de bits.
-   Más compatibilidad para la disposición en capas y el recorte a través de las API [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)), [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .
-   La capacidad de admitir la representación de texto en escala de grises. Esto rellena correctamente el canal alfa de destino según la opacidad del pincel de texto y el suavizado de contorno del texto.

Para admitir de forma eficaz la aceleración de hardware, [Direct2D](./direct2d-portal.md) usa una aproximación ligeramente diferente a la corrección gamma denominada *corrección alfa*. Esto no requiere que Direct2D Inspeccione el píxel de color de destino de representación al representar texto.

## <a name="conclusion"></a>Conclusión

En este tema se explican las diferencias y similitudes entre [Direct2D](./direct2d-portal.md) y [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) y las motivaciones arquitectónicas para proporcionarlos como API cooperativa independientes.

 

 
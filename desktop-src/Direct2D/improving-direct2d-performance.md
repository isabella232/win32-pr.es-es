---
title: Mejora del rendimiento de las aplicaciones de Direct2D
description: Describe técnicas para mejorar el rendimiento de Direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, rendimiento
- Direct2D, mapas de bits
- Direct2D, uso de recursos
- Direct2D,Flush (método)
- Direct2D, contenido estático
- rendimiento de Direct2D
- mapas de bits para Direct2D
- Interoperación de Direct2D,GDI
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 34adfd708ef3c1b8d7a6af145d9d1c9505b01beb1ba9b31834e267123ad05b69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641505"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Mejora del rendimiento de las aplicaciones de Direct2D

Aunque [Direct2D está](./direct2d-portal.md) acelerado por hardware y está pensado para un alto rendimiento, debe usar las características correctamente para maximizar el rendimiento. Las técnicas que se muestran aquí se derivan del estudio de escenarios comunes y es posible que no se apliquen a todos los escenarios de aplicación. Por lo tanto, una comprensión cuidadosa del comportamiento de la aplicación y los objetivos de rendimiento puede ayudar a lograr los resultados que desee.

-   [Uso de recursos](#resource-usage)
    -   [Reutilización de recursos](#reuse-resources)
-   [Restringir el uso de vaciado](#restrict-the-use-of-flush)
-   [Mapas de bits](#create-large-bitmaps)
    -   [Creación de mapas de bits grandes](#create-large-bitmaps)
    -   [Creación de un atlas de mapas de bits](#create-an-atlas-of-bitmaps)
    -   [Creación de mapas de bits compartidos](#create-shared-bitmaps)
    -   [Copiar mapas de bits](#copying-bitmaps)
-   [Uso de mapa de bits en mosaico sobre guiones](#use-tiled-bitmap-over-dashing)
-   [Directrices generales para representar contenido estático complejo](#general-guidelines-for-rendering-complex-static-content)
    -   [Almacenamiento en caché completo de la escena mediante un mapa de bits de color](#full-scene-caching-using-a-color-bitmap)
    -   [Por almacenamiento en caché primitivo mediante un mapa de bits A8 y el método FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Almacenamiento en caché por primitiva mediante realizaciones de geometría](#per-primitive-caching-using-geometry-realizations)
-   [Representación de geometría](#geometry-rendering)
    -   [Uso de una primitiva de dibujo específica sobre la geometría de dibujo](#use-specific-draw-primitive-over-draw-geometry)
    -   [Representación de geometría estática](#rendering-static-geometry)
    -   [Uso de un contexto de dispositivo multiproceso](#use-a-multithreaded-device-context)
-   [Dibujar texto con Direct2D](#use-a-multithreaded-device-context)
    -   [DrawTextLayout frente a DrawText](#drawtextlayout-vs-drawtext)
    -   [Elección del modo de representación de texto correcto](#choosing-the-right-text-rendering-mode)
    -   [Almacenamiento en caché](#full-scene-caching-using-a-color-bitmap)
-   [Recorte de una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [PushLayer en Windows 8](#pushlayer-in-windows-8)
    -   [Clips alineados con el eje](#axis-aligned-clips)
-   [Interoperabilidad de DXGI: evitar conmutadores frecuentes](#dxgi-interoperability-avoid-frequent-switches)
-   [Conocer el formato de píxel](#know-your-pixel-format)
-   [Complejidad de la escena](#scene-complexity)
    -   [Comprender la complejidad de la escena](#understand-scene-complexity)
-   [Mejora del rendimiento de las aplicaciones de impresión de Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Establecer los valores de propiedad correctos al crear el control de impresión D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Evitar el uso de determinados patrones de dibujo de Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Dibujar texto de forma directa y sin formato](#draw-text-in-a-direct-and-plain-way)
    -   [Dibujar los mapas de bits originales cuando sea posible](#draw-the-original-bitmaps-when-possible)
-   [Conclusión](#conclusion)

## <a name="resource-usage"></a>Uso de recursos

Un recurso es una asignación de algún tipo, ya sea en memoria de vídeo o del sistema. Los mapas de bits y los pinceles son ejemplos de recursos.

En Direct2D, los recursos se pueden crear tanto en software como en hardware. La creación y eliminación de recursos en hardware son operaciones costosas porque requieren mucha sobrecarga para comunicarse con la tarjeta de vídeo. Veamos cómo Direct2D representa el contenido en un destino.

En Direct2D, todos los comandos de representación se incluyen entre una llamada a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y una llamada a [**EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Estas llamadas se realizan a un destino de representación. Debe llamar al método **BeginDraw** antes de llamar a las operaciones de representación . Después de llamar a **BeginDraw** , un contexto normalmente compila un lote de comandos de representación, pero retrasa el procesamiento de estos comandos hasta que se cumple una de estas instrucciones:

-   [**Se produjo EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Cuando **se llama a EndDraw,** hace que se completen las operaciones de dibujo por lotes y devuelve el estado de la operación.
-   Realiza una llamada explícita a [**Flush:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)el método **Flush** hace que el lote se procese y se emita todos los comandos pendientes.
-   El búfer que mantiene los comandos de representación está lleno. Si este búfer se llena antes de que se cumplan las dos condiciones anteriores, se vacían los comandos de representación.

Hasta que se vacían las primitivas, Direct2D mantiene las referencias internas a los recursos correspondientes, como mapas de bits y pinceles.

### <a name="reuse-resources"></a>Reutilización de recursos

Como ya se ha mencionado, la creación y eliminación de recursos es costosa en hardware. Por lo tanto, reutilice los recursos cuando sea posible. Tome el ejemplo de creación de mapas de bits en el desarrollo de juegos. Normalmente, los mapas de bits que crean una escena en un juego se crean al mismo tiempo con todas las distintas variaciones necesarias para la representación posterior de fotograma a fotograma. En el momento de representar y volver a representar la escena real, estos mapas de bits se reutilizan en lugar de volver a crearse.

> [!Note]  
> No se pueden reutilizar recursos para la operación de cambio de tamaño de ventana. Cuando se cambia el tamaño de una ventana, algunos recursos dependientes de la escala, como destinos de representación compatibles y posiblemente algunos recursos de capa, deben volver a crearse porque el contenido de la ventana debe volver a dibujarse. Esto puede ser importante para mantener la calidad general de la escena representada.

 

## <a name="restrict-the-use-of-flush"></a>Restringir el uso de vaciado

Dado que [**el método Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) hace que los comandos de representación por lotes se procese, se recomienda no usarlos. En los escenarios más comunes, deje la administración de recursos en Direct2D.

## <a name="bitmaps"></a>Mapas de bits

Como se mencionó anteriormente, la creación y eliminación de recursos son operaciones muy costosas en hardware. Un mapa de bits es un tipo de recurso que se usa con frecuencia. La creación de mapas de bits en la tarjeta de vídeo es costosa. Volver a usarlos puede ayudar a que la aplicación sea más rápida.

### <a name="create-large-bitmaps"></a>Creación de mapas de bits grandes

Las tarjetas de vídeo suelen tener un tamaño mínimo de asignación de memoria. Si se solicita una asignación que es menor que esta, se asigna un recurso de este tamaño mínimo y la memoria sobrante se desperdicia y no está disponible para otras cosas. Si necesita muchos mapas de bits pequeños, una mejor técnica consiste en asignar un mapa de bits grande y almacenar todo el contenido de mapa de bits pequeño en este mapa de bits grande. A continuación, se pueden leer subáreas del mapa de bits más grande donde se necesitan los mapas de bits más pequeños. A menudo, debe incluir relleno (píxeles negro transparentes) entre los mapas de bits pequeños para evitar cualquier interacción entre las imágenes más pequeñas durante las operaciones. Esto también se conoce como *atlas* y tiene la ventaja de reducir la sobrecarga de creación de mapas de bits y la pérdida de memoria de pequeñas asignaciones de mapa de bits. Se recomienda mantener la mayoría de los mapas de bits en al menos 64 KB y limitar el número de mapas de bits menores de 4 KB.

### <a name="create-an-atlas-of-bitmaps"></a>Creación de un atlas de mapas de bits

Hay algunos escenarios comunes para los que un atlas de mapa de bits puede servir muy bien. Los mapas de bits pequeños se pueden almacenar dentro de un mapa de bits grande. Estos mapas de bits pequeños se pueden sacar del mapa de bits más grande cuando los necesite especificando el rectángulo de destino. Por ejemplo, una aplicación tiene que dibujar varios iconos. Todos los mapas de bits asociados a los iconos se pueden cargar en un mapa de bits grande por adelantado. Y en el momento de la representación, se pueden recuperar del mapa de bits grande.

> [!Note]  
> Un mapa de bits de Direct2D creado en la memoria de vídeo se limita al tamaño máximo de mapa de bits admitido por el adaptador en el que se almacena. La creación de un mapa de bits mayor que podría dar lugar a un error.

 

> [!Note]  
> A partir Windows 8, Direct2D incluye un [efecto Atlas](atlas.md) que puede facilitar este proceso.

 

### <a name="create-shared-bitmaps"></a>Creación de mapas de bits compartidos

La creación de mapas de bits compartidos permite a los llamadores avanzados crear objetos de mapa de bits de Direct2D que están respaldos directamente por un objeto existente, ya compatible con el destino de representación. Esto evita la creación de varias superficies y ayuda a reducir la sobrecarga de rendimiento.

> [!Note]  
> Los mapas de bits compartidos suelen limitarse a destinos de software o a destinos interoperables con DXGI. Use los [**métodos CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))y [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear mapas de bits compartidos.

 

### <a name="copying-bitmaps"></a>Copiar mapas de bits

La creación de una superficie DXGI es una operación costosa, por lo que reutilice las superficies existentes cuando pueda. Incluso en el software, si un mapa de bits tiene principalmente el formato que desea, excepto una pequeña parte, es mejor actualizar esa parte que quitar todo el mapa de bits y volver a crearlo todo. Aunque puede usar [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) para lograr los mismos resultados, la representación suele ser una operación mucho más costosa que copiar. Esto se debe a que, para mejorar la localidad de la caché, el hardware no almacena realmente un mapa de bits en el mismo orden de memoria al que se dirige el mapa de bits. En su lugar, el mapa de bits podría deslizarse. El controlador (que es lento y solo se usa en partes inferiores) o el administrador de memoria de la GPU oculta el desdobado de la CPU. Debido a las restricciones en la forma en que los datos se escriben en un destino de representación al representar, los destinos de representación normalmente no se deslizan o se deslizan de una manera menos óptima de lo que se puede lograr si sabe que nunca tiene que representarse en la superficie. Por lo tanto, [los métodos CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) se proporcionan para copiar rectángulos de un \* origen al mapa de bits de Direct2D.

CopyFrom se puede usar en cualquiera de sus tres formas:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Uso de mapas de bits en mosaico sobre guiones

Representar una línea discontinua es una operación muy costosa debido a la alta calidad y precisión del algoritmo subyacente. En la mayoría de los casos que no implican geometrías rectilíneas, el mismo efecto se puede generar más rápido mediante mapas de bits en mosaico.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Directrices generales para representar contenido estático complejo

Almacenar en caché el contenido si representa el mismo marco de contenido sobre el marco, especialmente cuando la escena es compleja.

Hay tres técnicas de almacenamiento en caché que puede usar:

-   Almacenamiento en caché completo de la escena mediante un mapa de bits de color.
-   Por almacenamiento en caché primitivo mediante un mapa de bits A8 y [**el método FillOpacityMask.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f))
-   Almacenamiento en caché por primitiva mediante realizaciones de geometría.

Echemos un vistazo a cada uno de ellos con más detalle.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Almacenamiento en caché completo de la escena mediante un mapa de bits de color

Al representar contenido estático, en escenarios como la animación, cree otro mapa de bits de color completo en lugar de escribir directamente en el mapa de bits de la pantalla. Guarde el destino actual, establezca target en el mapa de bits intermedio y represente el contenido estático. A continuación, vuelva al mapa de bits de la pantalla original y dibuje el mapa de bits intermedio en él.

Veamos un ejemplo:


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



En este ejemplo se usan mapas de bits intermedios para almacenar en caché y se cambia el mapa de bits al que apunta el contexto del dispositivo cuando se representa. Esto evita la necesidad de crear un destino de representación compatible para el mismo propósito.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Por almacenamiento en caché primitivo mediante un mapa de bits A8 y el método FillOpacityMask

Cuando la escena completa no es estática, pero consta de elementos como geometría o texto que son estáticos, puede usar una técnica de almacenamiento en caché por primitiva. Esta técnica conserva las características de suavizado de contorno de la primitiva que se almacena en caché y funciona con tipos de pincel cambiantes. Usa un mapa de bits A8 donde A8 es un tipo de formato de píxel que representa un canal alfa con 8 bits. Los mapas de bits A8 son útiles para dibujar geometría o texto como máscara. Cuando debe manipular la opacidad del contenido estático, en lugar de manipular el propio contenido, puede traducir, girar, sesgar o escalar la opacidad de la máscara.

Veamos un ejemplo:


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>Almacenamiento en caché por primitiva mediante realizaciones de geometría

Otra técnica de almacenamiento en caché por primitiva, denominada realizaciones de geometría, proporciona mayor flexibilidad al tratar con la geometría. Si desea dibujar repetidamente geometrías con alias o con suavizado de alias, es más rápido convertirlos en realizaciones de geometría y dibujar repetidamente las realizaciones que dibujar repetidamente las propias geometrías. Las realizaciones de geometría también suelen consumir menos memoria que las máscaras de opacidad (especialmente para geometrías grandes) y son menos sensibles a los cambios en la escala. Para obtener más información, vea [Información general sobre las realizaciones de geometría.](geometry-realizations-overview.md)

Veamos un ejemplo:


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>Representación de geometría

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Usar una primitiva de dibujo específica sobre la geometría de dibujo

Use llamadas primitivas *de dibujo más* específicas, como [**DrawRectangle, en**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) llamadas a [**DrawGeometry genéricas.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) Esto se debe a **que, con DrawRectangle,** la geometría ya se conoce, por lo que la representación es más rápida.

### <a name="rendering-static-geometry"></a>Representación de geometría estática

En escenarios en los que la geometría es estática, use las técnicas de almacenamiento en caché por primitiva que se han explicado anteriormente. Las máscaras de opacidad y las realizaciones de geometría pueden mejorar en gran manera la velocidad de representación de las escenas que contienen geometría estática.

### <a name="use-a-multithreaded-device-context"></a>Uso de un contexto de dispositivo multiproceso

Las aplicaciones que esperan representar cantidades significativas de contenido geométrico complejo deben considerar la posibilidad de especificar la marca [**D2D1 \_ DEVICE CONTEXT OPTIONS ENABLE MULTI \_ \_ \_ \_ \_ THREADED \_ OPTIMIZATIONS**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) (HABILITAR OPTIMIZACIONES MULTIPROCESO) al crear un contexto de dispositivo [Direct2D.](./direct2d-portal.md) Cuando se especifica esta marca, Direct2D distribuirá la representación entre todos los núcleos lógicos presentes en el sistema, lo que puede reducir significativamente el tiempo de representación general.

Notas:

-   A Windows 8.1, esta marca solo afecta a la representación de geometría de ruta de acceso. No afecta a las escenas que contienen solo otros tipos primitivos (como texto, mapas de bits o realizaciones de geometría).
-   Esta marca tampoco tiene ningún impacto al representar en software (es decir, cuando se representa con un dispositivo WARP Direct3D). Para controlar el multithreading de software, los llamadores deben usar la marca CREATE DEVICE PREVENT INTERNAL THREADING OPTIMIZATIONS de D3D11 al crear el dispositivo \_ \_ WARP \_ \_ \_ \_ Direct3D.
-   La especificación de esta marca puede aumentar el máximo de trabajo durante la representación y también puede aumentar la contención de subprocesos en aplicaciones que ya aprovechan el procesamiento multiproceso.

## <a name="drawing-text-with-direct2d"></a>Dibujo de texto con Direct2D

La funcionalidad de representación de texto de Direct2D se ofrece en dos partes. La primera parte, expuesta como el [**método ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) permite a un autor de llamada pasar una cadena y parámetros de formato o un objeto de diseño de texto DWrite para varios formatos. Esto debe ser adecuado para la mayoría de los llamadores. La segunda manera de representar texto, expuesta como el método [**ID2D1RenderTarget::D rawGlyphRun,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) proporciona rasterización para los clientes que ya conocen la posición de los glifos que quieren representar. Las dos reglas generales siguientes pueden ayudar a mejorar el rendimiento del texto al dibujar en Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout frente a DrawText

DrawText [**y**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [**DrawTextLayout permiten**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) a una aplicación representar fácilmente el texto con el formato de DirectWrite [API.](/windows/desktop/DirectWrite/direct-write-portal) **DrawTextLayout** dibuja un objeto [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) existente en [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)y **DrawText** construye un diseño DirectWrite para el autor de la llamada, basándose en los parámetros que se pasan. Si el mismo texto se tiene que representar varias veces, use **DrawTextLayout** en lugar de **DrawText**, ya que **DrawText** crea un diseño cada vez que se llama.

### <a name="choosing-the-right-text-rendering-mode"></a>Elección del modo de representación de texto correcto

Establezca el modo de suavizado de contorno de texto en [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE \_ GRAYSCALE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) explícitamente. La calidad del texto de escala de grises de representación es comparable a ClearType, pero es mucho más rápida.

### <a name="caching"></a>Almacenamiento en memoria caché

Use la escena completa o el almacenamiento en caché de mapa de bits primitivo, como con el dibujo de otras primitivas.

## <a name="clipping-an-arbitrary-shape"></a>Recorte de una forma arbitraria

En la ilustración siguiente se muestra el resultado de aplicar un clip a una imagen.

![una imagen que muestra un ejemplo de una imagen antes y después de un clip.](images/clip.png)

Puede obtener este resultado mediante capas con una máscara de geometría o el [**método FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de opacidad.

Este es un ejemplo en el que se usa una capa:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Este es un ejemplo que usa el [**método FillGeometry:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



En este ejemplo de código, cuando se llama al método PushLayer, no se pasa una capa creada por la aplicación. Direct2D crea una capa automáticamente. Direct2D puede administrar la asignación y destrucción de este recurso sin intervención de la aplicación. Esto permite a Direct2D reutilizar capas internamente y aplicar optimizaciones de administración de recursos.

En Windows 8 se han realizado muchas optimizaciones para el uso de capas y se recomienda intentar usar las API de capa en lugar de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) siempre que sea posible.

### <a name="pushlayer-in-windows-8"></a>PushLayer en Windows 8

La interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) se deriva de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y es clave para mostrar contenido de Direct2D en Windows 8. Para obtener más información sobre esta interfaz, vea Dispositivos y [contextos de dispositivo.](devices-and-device-contexts.md) Con la interfaz de contexto del dispositivo, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar NULL al [**método ID2D1DeviceContext::P ushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) Direct2D administra automáticamente el recurso de capa y puede compartir recursos entre capas y gráficos de efectos.

### <a name="axis-aligned-clips"></a>Clips alineados con ejes

Si la región que se va a recortar está alineada con el eje de la superficie de dibujo, en lugar de arbitraria. Este caso es adecuado para usar un rectángulo de recorte en lugar de una capa. La ganancia de rendimiento es más para la geometría con alias que la geometría suavizada. Para obtener más información sobre los clips alineados en el eje, vea el [**tema PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interoperabilidad de DXGI: evitar conmutadores frecuentes

Direct2D puede interoperar sin problemas con superficies de Direct3D. Esto es muy útil para crear aplicaciones que representan una mezcla de contenido 2D y 3D. Pero cada cambio entre dibujar contenido de Direct2D y Direct3D afecta al rendimiento.

Al representar en una superficie DXGI, Direct2D guarda el estado de los dispositivos Direct3D mientras se representa y lo restaura cuando se completa la representación. Cada vez que se completa un lote de representación de Direct2D, se paga el costo de este ahorro y restauración y el costo de vaciar todas las operaciones 2D y, sin embargo, el dispositivo Direct3D no se vacía. Por lo tanto, para aumentar el rendimiento, limite el número de conmutadores de representación entre Direct2D y Direct3D.

## <a name="know-your-pixel-format"></a>Conocer el formato de píxel

Al crear un destino de representación, puede usar la estructura [**D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) para especificar el formato de píxel y el modo alfa que usa el destino de representación. Un canal alfa forma parte del formato de píxel que especifica el valor de cobertura o la información de opacidad. Si un destino de representación no usa el canal alfa, debe crearse mediante el modo alfa [**D2D1 \_ ALPHA MODE \_ \_ IGNORE.**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Esto ahorra el tiempo dedicado a representar un canal alfa que no es necesario.

Para obtener más información sobre los formatos de píxel y los modos alfa, vea [Formatos de píxeles y modos alfa admitidos.](supported-pixel-formats-and-alpha-modes.md)

## <a name="scene-complexity"></a>Complejidad de la escena

Al analizar las zonas de acceso más populares de rendimiento de una escena que se representará, saber si la escena está enlazada a velocidad de relleno o enlazada a vértices puede proporcionar información útil.

-   Tasa de relleno: la tasa de relleno hace referencia al número de píxeles que una tarjeta gráfica puede representar y escribir en la memoria de vídeo por segundo.
-   Vértice enlazado: una escena está enlazada a vértices cuando contiene una gran cantidad de geometría compleja.

### <a name="understand-scene-complexity"></a>Comprender la complejidad de la escena

Puede analizar la complejidad de la escena modificando el tamaño del destino de representación. Si las mejoras de rendimiento son visibles para una reducción proporcional del tamaño del destino de representación, la aplicación está enlazada a la tasa de relleno. De lo contrario, la complejidad de la escena es el cuello de botella de rendimiento.

Cuando una escena está enlazada a la velocidad de relleno, reducir el tamaño del destino de representación puede mejorar el rendimiento. Esto se debe a que el número de píxeles que se van a representar se reducirá proporcionalmente con el tamaño del destino de representación.

Cuando una escena está enlazada a vértices, reduzca la complejidad de la geometría. Pero recuerde que esto se hace a costa de la calidad de la imagen. Por lo tanto, se debe tomar una cuidadosa decisión de equilibrio entre la calidad deseada y el rendimiento necesario.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Mejora del rendimiento de las aplicaciones de impresión de Direct2D

[Direct2D ofrece](./direct2d-portal.md) compatibilidad con la impresión. Puede enviar los mismos comandos de dibujo de Direct2D (en forma de listas de comandos de Direct2D) al control de impresión de Direct2D para imprimir, si no sabe en qué dispositivos está dibujando o cómo se traduce el dibujo a impresión.

Puede ajustar aún más su uso del control de impresión [de Direct2D](./direct2d-portal.md) y los comandos de dibujo de Direct2D para ofrecer resultados de impresión con un mejor rendimiento.

El control de impresión de [Direct2D](./direct2d-portal.md) genera mensajes de depuración cuando ve un patrón de código direct2D que conduce a una menor calidad o rendimiento de impresión (por ejemplo, patrones de código enumerados más adelante en este tema) para recordar dónde puede evitar problemas de rendimiento. Para ver esos mensajes de depuración, debe habilitar la capa de depuración de [Direct2D](direct2ddebuglayer-portal.md) en el código. Consulte [Depurar mensajes para](direct2ddebuglayer-debugmessages.md) obtener instrucciones para habilitar la salida de mensajes de depuración.

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Establecer los valores de propiedad correctos al crear el control de impresión D2D

Hay tres propiedades que puede establecer al crear el control [de impresión de Direct2D.](./direct2d-portal.md) Dos de estas propiedades afectan al modo en que el control de impresión de Direct2D controla determinados comandos de Direct2D y, a su vez, afectan al rendimiento general.

-   Modo de subconjunto de fuentes: los subconjuntos de fuentes de los subconjuntos de control de impresión de [Direct2D](./direct2d-portal.md) que se usan en cada página antes de enviar la página que se va a imprimir. Este modo reduce el tamaño de los recursos de página necesarios para imprimir. En función del uso de fuentes en la página, puede elegir diferentes modos de subconjunto de fuentes para obtener el mejor rendimiento.
    -   [**D2D1 \_ PRINT \_ FONT SUBSET MODE DEFAULT \_ \_ \_ proporciona**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) el mejor rendimiento de impresión en la mayoría de los casos. Cuando se establece en este modo, el control [de impresión de Direct2D](./direct2d-portal.md) usa una estrategia heurística para decidir cuándo se deben crear subconjuntos de fuentes.
    -   Para trabajos de impresión cortos con 1 o 2 páginas, se recomienda [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , donde el control de impresión [direct2D](./direct2d-portal.md) inserta los recursos de fuente en cada página y, a continuación, descarta ese subconjunto de fuentes después de que se imprima la página. Esta opción se asegura de que cada página se pueda imprimir inmediatamente después de generarse, pero aumenta ligeramente el tamaño de los recursos de página necesarios para imprimir (con normalmente grandes subconjuntos de fuentes).
    -   Para trabajos de impresión con muchas páginas de texto y tamaños de fuente pequeños (como 100 páginas de texto que usa una sola fuente), se recomienda [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), donde el control de impresión de [Direct2D](./direct2d-portal.md) no crea un subconjunto de recursos de fuente; en su lugar, envía los recursos de fuente originales junto con la página que usa primero la fuente y vuelve a usar los recursos de fuente para páginas posteriores sin reenviarlos.
-   PPP de rasterización: cuando el control de impresión de [Direct2D](./direct2d-portal.md) necesita rasterizar comandos de Direct2D durante la conversión de Direct2D-XPS, usa este PPP para la rasterización. En otras palabras, si la página no tiene ningún contenido rasterizado, el establecimiento de cualquier PPP no cambiará el rendimiento y la calidad. En función del uso de rasterización en la página, puede elegir diferentes DPI de rasterización para obtener el mejor equilibrio entre fidelidad y rendimiento.
    -   150 es el valor predeterminado si no se especifica un valor al crear el control de impresión [de Direct2D,](./direct2d-portal.md) que es el mejor equilibrio entre la calidad de impresión y el rendimiento de impresión en la mayoría de los casos.
    -   Los valores de PPP más altos suelen dar lugar a una mejor calidad de impresión (como se conserva en más detalles), pero un rendimiento menor debido a los mapas de bits más grandes que genera. No se recomienda ningún valor de PPP mayor que 300, ya que eso no introducirá información adicional que puedan obtener los ojos humanos visualmente.
    -   Un valor de PPP inferior puede significar un mejor rendimiento, pero también puede producir una calidad inferior.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Evitar el uso de determinados patrones de dibujo de Direct2D

Hay diferencias entre lo [que Direct2D](./direct2d-portal.md) puede representar visualmente y lo que el subsistema de impresión puede mantener y transportar a lo largo de toda la canalización de impresión. El control de impresión de Direct2D une esas brechas mediante la aproximación o rasterización de primitivas de Direct2D que el subsistema de impresión no admite de forma nativa. Esta aproximación suele tener como resultado una menor fidelidad de impresión, un rendimiento de impresión inferior o ambos. Por lo tanto, aunque un cliente puede usar los mismos patrones de dibujo para la representación de pantalla e impresión, no es ideal en todos los casos. Es mejor no usar tales primitivos y patrones de Direct2D tanto como sea posible para la ruta de impresión, o bien para hacer que sea propietario de la rasterización, donde tenga control total de la calidad y el tamaño de las imágenes rasterizadas.

Esta es una lista de casos en los que el rendimiento y la calidad de impresión no serán ideales y es posible que quiera considerar la posibilidad de cambiar la ruta de acceso del código para obtener un rendimiento de impresión óptimo.

-   Evite usar el modo de mezcla primitivo distinto de [**D2D1 \_ PRIMITIVE \_ BLEND \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Evite usar modos de composición al dibujar una imagen que no sea [**D2D1 \_ COMPOSITE MODE SOURCE \_ \_ \_ OVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) y **D2D1 \_ COMPOSITE MODE DESTINATION \_ \_ \_ OVER**.
-   Evite dibujar un metarchivo GDI.
-   Evite insertar un recurso de capa que copie el fondo de origen (llamando a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) pasando [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) al **struct D2D1 \_ LAYER \_ PARAMETERS1).**
-   Evite crear un pincel de mapa de bits o un pincel de imagen con D2D1 \_ EXTEND \_ MODE \_ CLAMP. Se recomienda usar D2D1 EXTEND MODE MIRROR si no le importan los píxeles fuera de la imagen enlazada (como, se sabe que la imagen asociada al pincel es mayor que la región de destino \_ \_ \_ rellenada).
-   Evite dibujar mapas de bits con [transformaciones de perspectiva.](3d-perspective-transform.md)

### <a name="draw-text-in-a-direct-and-plain-way"></a>Dibujar texto de forma directa y sin formato

Direct2D tiene varias optimizaciones al representar textos para mostrar para mejorar el rendimiento o una mejor calidad visual. Pero no todas las optimizaciones mejoran el rendimiento y la calidad de impresión, ya que la impresión en papel suele tener un valor de PPP mucho mayor y la impresión no necesita adaptarse a escenarios como la animación. Por lo tanto, se recomienda dibujar directamente el texto o glifos originales y evitar cualquiera de las siguientes optimizaciones al crear la lista de comandos para imprimir.

-   Evite dibujar texto con [**el método FillOpacityMask.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask)
-   Evite dibujar texto en modo con alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Dibujar los mapas de bits originales cuando sea posible

Si el mapa de bits de destino es JPEG, PNG, TIFF o JPEG-XR, puede crear un mapa de bits de WIC desde un archivo de disco o desde una secuencia en memoria, crear un mapa de bits de [Direct2D](./direct2d-portal.md) a partir de ese mapa de bits de WIC mediante [**ID2D1DeviceContext::CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))y, por último, pasar directamente ese mapa de bits de Direct2D al control de impresión de Direct2D sin más manipulación. Al hacerlo, el control de impresión de Direct2D puede reutilizar la secuencia de mapa de bits, lo que normalmente conduce a un mejor rendimiento de impresión (omitiendo la codificación y la codificación de mapas de bits redundantes) y una mejor calidad de impresión (cuando se conservarán los metadatos, como los perfiles de color, en el mapa de bits).

Dibujar el mapa de bits original proporciona la siguiente ventaja para las aplicaciones.

-   En general, la impresión [de Direct2D](./direct2d-portal.md) conserva la información original (sin pérdida ni ruido) hasta el final de la canalización, especialmente cuando las aplicaciones no conocen (o no quieren saber) los detalles de la canalización de impresión (como la impresora en la que se imprime, qué PPP es la impresora de destino, y así sucesivamente).
-   En muchos casos, retrasar la rasterización de mapa de bits significa un mejor rendimiento (como al imprimir una foto de 96dpi en una impresora de 600dpi).
-   En algunos casos, pasar las imágenes originales es la única manera de respetar la alta fidelidad (como los perfiles de color incrustados).

Sin embargo, no puede participar en esta optimización porque:

-   Al consultar la información de la impresora y la rasterización temprana, puede rasterizar el contenido ellos mismos con control total de la apariencia final en papel.
-   En algunos casos, la rasterización temprana podría mejorar realmente el rendimiento de un extremo a otro de una aplicación (como imprimir fotos de tamaño de cartera).
-   En algunos casos, pasar los mapas de bits originales requiere un cambio significativo de la arquitectura de código existente (como la carga retrasada de imágenes y las rutas de actualización de recursos que se encuentran en determinadas aplicaciones).

## <a name="conclusion"></a>Conclusión

Aunque Direct2D está acelerado por hardware y está pensado para un alto rendimiento, debe usar las características correctamente para maximizar el rendimiento. Las técnicas que hemos visto aquí se derivan del estudio de escenarios comunes y es posible que no se apliquen a todos los escenarios de aplicación.

 

 

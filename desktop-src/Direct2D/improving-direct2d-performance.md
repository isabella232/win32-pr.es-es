---
title: Mejorar el rendimiento de las aplicaciones de Direct2D
description: Describe técnicas para mejorar el rendimiento de Direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, rendimiento
- Direct2D, mapas de bits
- Direct2D, uso de recursos
- Direct2D, método Flush
- Direct2D, contenido estático
- rendimiento de Direct2D
- mapas de bits para Direct2D
- Direct2D, interoperación de GDI
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2020
ms.locfileid: "104488477"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Mejorar el rendimiento de las aplicaciones de Direct2D

Aunque [Direct2D](./direct2d-portal.md) tiene aceleración de hardware y está pensado para un alto rendimiento, debe usar las características correctamente para maximizar el rendimiento. Las técnicas que se muestran aquí se derivan del estudio de escenarios comunes y es posible que no se apliquen a todos los escenarios de aplicaciones. Por lo tanto, una comprensión minuciosa del comportamiento de la aplicación y de los objetivos de rendimiento puede ayudarle a lograr los resultados que desea.

-   [Uso de recursos](#resource-usage)
    -   [Reutilizar recursos](#reuse-resources)
-   [Restringir el uso de Flush](#restrict-the-use-of-flush)
-   [Mapas de bits](#create-large-bitmaps)
    -   [Crear mapas de bits grandes](#create-large-bitmaps)
    -   [Crear un Atlas de mapas de bits](#create-an-atlas-of-bitmaps)
    -   [Crear mapas de bits compartidos](#create-shared-bitmaps)
    -   [Copiar mapas de bits](#copying-bitmaps)
-   [Usar un mapa de bits en mosaico en guiones](#use-tiled-bitmap-over-dashing)
-   [Directrices generales para la representación de contenido estático complejo](#general-guidelines-for-rendering-complex-static-content)
    -   [Almacenamiento en caché completo de escenas con un mapa de bits de color](#full-scene-caching-using-a-color-bitmap)
    -   [Por almacenamiento en caché primitivo mediante un mapa de bits A8 y el método FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Almacenamiento en caché por primitivo mediante la realización de geometría](#per-primitive-caching-using-geometry-realizations)
-   [Representación de geometría](#geometry-rendering)
    -   [Usar una primitiva de dibujo específica sobre la geometría de dibujo](#use-specific-draw-primitive-over-draw-geometry)
    -   [Representación de geometría estática](#rendering-static-geometry)
    -   [Usar un contexto de dispositivo multiproceso](#use-a-multithreaded-device-context)
-   [Dibujar texto con Direct2D](#use-a-multithreaded-device-context)
    -   [DrawTextLayout frente a DrawText](#drawtextlayout-vs-drawtext)
    -   [Elección del modo de representación de texto correcto](#choosing-the-right-text-rendering-mode)
    -   [Almacenamiento en caché](#full-scene-caching-using-a-color-bitmap)
-   [Recortar una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [PushLayer en Windows 8](#pushlayer-in-windows-8)
    -   [Clips alineados con el eje](#axis-aligned-clips)
-   [Interoperabilidad de DXGI: evitar modificadores frecuentes](#dxgi-interoperability-avoid-frequent-switches)
-   [Conozca el formato de píxel](#know-your-pixel-format)
-   [Complejidad de la escena](#scene-complexity)
    -   [Descripción de la complejidad de la escena](#understand-scene-complexity)
-   [Mejorar el rendimiento de las aplicaciones de impresión en Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Establecer los valores de propiedad correctos al crear el control de impresión D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Evite usar determinados patrones de dibujo de Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Dibujar texto de forma directa y sin formato](#draw-text-in-a-direct-and-plain-way)
    -   [Dibujar los mapas de bits originales siempre que sea posible](#draw-the-original-bitmaps-when-possible)
-   [Conclusión](#conclusion)

## <a name="resource-usage"></a>Uso de recursos

Un recurso es una asignación de algún tipo, ya sea en la memoria de vídeo o del sistema. Los mapas de bits y los pinceles son ejemplos de recursos.

En Direct2D, los recursos se pueden crear en software y hardware. La creación y eliminación de recursos en el hardware son operaciones costosas porque requieren una gran sobrecarga para la comunicación con la tarjeta de vídeo. Veamos cómo Direct2D representa el contenido en un destino.

En Direct2D, todos los comandos de representación se incluyen entre una llamada a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y una llamada a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Estas llamadas se realizan a un destino de representación. Debe llamar al método **BeginDraw** antes de llamar a las operaciones de representación. Después de llamar a **BeginDraw** , un contexto normalmente crea un lote de comandos de representación, pero retrasa el procesamiento de estos comandos hasta que una de estas instrucciones sea verdadera:

-   Error de [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Cuando se llama a **EndDraw** , hace que todas las operaciones de dibujo por lotes se completen y devuelva el estado de la operación.
-   Realiza una llamada explícita a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush): el método **Flush** hace que el lote se procese y se emitan todos los comandos pendientes.
-   El búfer que contiene los comandos de representación está lleno. Si este búfer se llena antes de que se cumplan las dos condiciones anteriores, los comandos de representación se vacían.

Hasta que se vacíen los primitivos, Direct2D mantiene las referencias internas a los recursos correspondientes, como mapas de bits y pinceles.

### <a name="reuse-resources"></a>Reutilizar recursos

Como ya se mencionó, la creación y eliminación de recursos es costosa en hardware. Por tanto, reutilice los recursos siempre que sea posible. Tome el ejemplo de creación de mapas de bits en el desarrollo de juegos. Normalmente, los mapas de bits que componen una escena en un juego se crean al mismo tiempo con todas las variaciones que son necesarias para la representación de fotogramas de fotogramas posterior. En el momento de la representación y rerepresentación de la escena real, estos mapas de bits se reutilizan en lugar de volver a crearlos.

> [!Note]  
> No se pueden volver a usar los recursos para la operación de cambiar el tamaño de la ventana. Cuando se cambia el tamaño de una ventana, algunos recursos dependientes de la escala, como los destinos de representación compatibles y, posiblemente, algunos recursos de capa se deben volver a crear porque se debe volver a dibujar el contenido de la ventana. Esto puede ser importante para mantener la calidad general de la escena representada.

 

## <a name="restrict-the-use-of-flush"></a>Restringir el uso de Flush

Dado que el método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) hace que se procesen los comandos de representación por lotes, se recomienda no usarlos. Para los escenarios más comunes, deje la administración de recursos en Direct2D.

## <a name="bitmaps"></a>Mapas de bits

Como se mencionó anteriormente, la creación y eliminación de recursos son operaciones muy costosas en el hardware. Un mapa de bits es un tipo de recurso que se usa con frecuencia. La creación de mapas de bits en la tarjeta de vídeo es costosa. La reutilización puede ayudar a agilizar la aplicación.

### <a name="create-large-bitmaps"></a>Crear mapas de bits grandes

Las tarjetas de vídeo suelen tener un tamaño mínimo de asignación de memoria. Si se solicita una asignación menor que esta, se asigna un recurso de este tamaño mínimo y la memoria excedente se desperdicia y no está disponible para otras cosas. Si necesita muchos mapas de bits pequeños, una técnica mejor consiste en asignar un mapa de bits grande y almacenar todo el contenido del mapa de bits pequeño en este mapa de bits grande. A continuación, se pueden leer las subáreas del mapa de bits más grande donde se necesiten los mapas de bits más pequeños. A menudo, debe incluir el relleno (píxeles negros transparentes) entre los mapas de bits pequeños para evitar cualquier interacción entre las imágenes más pequeñas durante las operaciones. Esto también se conoce como *Atlas* y tiene la ventaja de reducir la sobrecarga de creación de mapas de bits y los residuos de memoria de pequeñas asignaciones de mapas de bits. Le recomendamos que mantenga la mayoría de los mapas de bits en al menos 64 KB y limite el número de mapas de bits que tienen menos de 4 KB.

### <a name="create-an-atlas-of-bitmaps"></a>Crear un Atlas de mapas de bits

Hay algunos escenarios comunes en los que un Atlas de mapas de bits puede servir muy bien. Los mapas de bits pequeños se pueden almacenar en un mapa de bits grande. Estos mapas de bits pequeños se pueden extraer del mapa de bits más grande cuando se necesitan especificando el rectángulo de destino. Por ejemplo, una aplicación tiene que dibujar varios iconos. Todos los mapas de bits asociados a los iconos se pueden cargar en un mapa de bits de gran tamaño. Y en el momento de la representación, se pueden recuperar del mapa de bits grande.

> [!Note]  
> Un mapa de bits de Direct2D creado en la memoria de vídeo se limita al tamaño máximo de mapa de bits admitido por el adaptador en el que se almacena. La creación de un mapa de bits mayor que esto podría producir un error.

 

> [!Note]  
> A partir de Windows 8, Direct2D incluye un [efecto de Atlas](atlas.md) que puede facilitar este proceso.

 

### <a name="create-shared-bitmaps"></a>Crear mapas de bits compartidos

La creación de mapas de bits compartidos permite a los autores de llamadas avanzados crear objetos de mapa de bits de Direct2D que están respaldados directamente por un objeto existente, ya compatibles con el destino de representación. Esto evita la creación de varias superficies y ayuda a reducir la sobrecarga de rendimiento.

> [!Note]  
> Normalmente, los mapas de bits compartidos se limitan a los destinos de software o a los destinos interoperables con DXGI. Use los métodos [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))y [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear mapas de bits compartidos.

 

### <a name="copying-bitmaps"></a>Copiar mapas de bits

Crear una superficie de DXGI es una operación costosa, por lo que puede reutilizar las superficies existentes cuando sea posible. Incluso en el software, si un mapa de bits está principalmente en el formato que desea, salvo en el caso de una pequeña parte, es mejor actualizar esa parte que para producir todo el mapa de bits y volver a crear todo. Aunque puede usar [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) para lograr los mismos resultados, la representación suele ser una operación mucho más costosa que copiar. Esto se debe a que, para mejorar la ubicación de la memoria caché, el hardware no almacena realmente un mapa de bits en el mismo orden de memoria al que se dirige el mapa de bits. En su lugar, el mapa de bits podría ser swizzled. El permutación está oculto en la CPU, ya sea por el controlador (que es lento y se usa solo en partes inferiores), o por el administrador de memoria de la GPU. Debido a las restricciones sobre cómo se escriben los datos en un destino de representación durante la representación, los destinos de representación normalmente no son swizzled o swizzled de una manera menos óptima que se puede lograr si sabe que nunca tiene que representarse en la superficie. Por lo tanto [](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) , \* se proporcionan los métodos CopyFrom para copiar los rectángulos de un origen al mapa de bits de Direct2D.

CopyFrom se puede usar en cualquiera de las tres formas siguientes:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Usar un mapa de bits en mosaico en guiones

La representación de una línea discontinua es una operación muy costosa debido a la alta calidad y la precisión del algoritmo subyacente. Para la mayoría de los casos que no implican geometrías rectilíneas, se puede generar el mismo efecto más rápido mediante el uso de mapas de bits en mosaico.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Directrices generales para la representación de contenido estático complejo

Contenido de la memoria caché si se representa el mismo marco de contenido sobre el marco, especialmente cuando la escena es compleja.

Hay tres técnicas de almacenamiento en caché que puede usar:

-   Almacenamiento en caché completo de escenas con un mapa de bits de color.
-   Por almacenamiento en caché primitivo mediante un mapa de bits A8 y el método [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) .
-   Almacenamiento en caché por primitivo mediante la realización de geometría.

Echemos un vistazo a cada uno de ellos con más detalle.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Almacenamiento en caché completo de escenas con un mapa de bits de color

Al representar contenido estático, en escenarios como animación, cree otro mapa de bits de color completo en lugar de escribir directamente en el mapa de bits de la pantalla. Guarde el destino actual, establezca el destino en el mapa de bits intermedio y represente el contenido estático. A continuación, vuelva al mapa de bits de la pantalla original y dibuje el mapa de bits intermedio en él.

Este es un ejemplo:


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



En este ejemplo se usan mapas de bits intermedios para el almacenamiento en caché y se cambia el mapa de bits al que apunta el contexto de dispositivo cuando se representa. Esto evita la necesidad de crear un destino de representación compatible con el mismo propósito.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Por almacenamiento en caché primitivo mediante un mapa de bits A8 y el método FillOpacityMask

Cuando la escena completa no es estática, pero se compone de elementos como Geometry o Text que son estáticos, puede usar una técnica de almacenamiento en caché por primitiva. Esta técnica conserva las características de suavizado de contorno de la primitiva que se almacenan en caché y funciona con los tipos de pincel cambiantes. Utiliza un mapa de bits A8 donde A8 es un tipo de formato de píxel que representa un canal alfa con 8 bits. Los mapas de bits A8 son útiles para dibujar geometría o texto como una máscara. Cuando debe manipular la opacidad del contenido estático, en lugar de manipular el contenido, puede trasladar, girar, sesgar o escalar la opacidad de la máscara.

Este es un ejemplo:


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



## <a name="per-primitive-caching-using-geometry-realizations"></a>Almacenamiento en caché por primitivo mediante la realización de geometría

Otra técnica de almacenamiento en caché por primitivo, denominada Geometry conversiones, proporciona mayor flexibilidad al tratar con Geometry. Si desea dibujar repetidamente geometrías con alias o suavizado de contorno, es más rápido convertirlas en conversiones de geometría y dibujar repetidas veces las supuestos que se van a dibujar repetidamente las propias geometrías. Las contrataciones de geometría también utilizan normalmente menos memoria que las máscaras de opacidad (especialmente para las geometrías grandes) y son menos sensibles a los cambios de escala. Para obtener más información, vea [información general sobre la realización de geometrías](geometry-realizations-overview.md).

Este es un ejemplo:


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

Usar llamadas *primitivas* Draw más específicas como [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) sobre llamadas [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) genéricas. Esto se debe a que with **DrawRectangle**, la geometría ya se conoce, por lo que la representación es más rápida.

### <a name="rendering-static-geometry"></a>Representación de geometría estática

En escenarios en los que la geometría sea estática, use las técnicas de almacenamiento en caché por primitivos explicadas anteriormente. Las máscaras de opacidad y las supuestos de geometría pueden mejorar considerablemente la velocidad de representación de escenas que contienen geometría estática.

### <a name="use-a-multithreaded-device-context"></a>Usar un contexto de dispositivo multiproceso

Las aplicaciones que esperan presentar grandes cantidades de contenido geométrico complejo deben considerar la posibilidad de especificar las [**Opciones de contexto de dispositivo D2D1 habilitar la marca de \_ \_ \_ \_ \_ \_ \_ optimizaciones multiproceso**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) al crear un contexto de dispositivo de [Direct2D](./direct2d-portal.md) . Cuando se especifica esta marca, Direct2D distribuirá la representación en todos los núcleos lógicos presentes en el sistema, lo que puede reducir significativamente el tiempo de representación global.

Notas:

-   A partir de Windows 8.1, esta marca solo afecta a la representación de geometría de ruta de acceso. No tiene ningún impacto en las escenas que solo contienen otros tipos primitivos (como texto, mapas de bits o realización de geometría).
-   Esta marca tampoco tiene ningún impacto en la representación en software (es decir, cuando se representa con un dispositivo Direct3D de ALABEo). Para controlar el multithreading de software, los autores de la llamada deben usar la \_ marca D3D11 crear \_ dispositivo \_ impedir las \_ \_ optimizaciones de subprocesos internas \_ al crear el dispositivo Direct3D de alabeo.
-   Si se especifica este marcador, se puede aumentar el espacio de trabajo máximo durante la representación y también se puede aumentar la contención de subprocesos en aplicaciones que ya aprovechan el procesamiento multiproceso.

## <a name="drawing-text-with-direct2d"></a>Dibujar texto con Direct2D

La funcionalidad de representación de texto de Direct2D se ofrece en dos partes. La primera parte, expuesta como el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , permite que un llamador pase una cadena y parámetros de formato o un objeto de diseño de texto DWrite para varios formatos. Debe ser adecuado para la mayoría de los llamadores. La segunda manera de representar texto, expuesta como el método [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) , proporciona rasterización para los clientes que ya conocen la posición de los glifos que desean representar. Las dos reglas generales siguientes pueden ayudar a mejorar el rendimiento del texto al dibujar en Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout frente a DrawText

Tanto [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) como [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) permiten a una aplicación representar fácilmente texto con formato de la API de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) . **DrawTextLayout** dibuja un objeto [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) existente en [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)y **DrawText** crea un diseño de DirectWrite para el llamador, basándose en los parámetros que se pasan. Si el mismo texto se tiene que representar varias veces, use **DrawTextLayout** en lugar de **DrawText**, porque **DrawText** crea un diseño cada vez que se llama.

### <a name="choosing-the-right-text-rendering-mode"></a>Elección del modo de representación de texto correcto

Establezca el modo de suavizado de contorno de texto en el modo de [**\_ \_ desalias de texto \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) de forma explícita. La calidad de la representación de texto de escala de grises es comparable a ClearType pero es mucho más rápida.

### <a name="caching"></a>Almacenamiento en memoria caché

Use la escena completa o el almacenamiento en caché de mapas de bits primitivo como con el dibujo de otros primitivos.

## <a name="clipping-an-arbitrary-shape"></a>Recortar una forma arbitraria

En la ilustración siguiente se muestra el resultado de aplicar un clip a una imagen.

![imagen que muestra un ejemplo de una imagen antes y después de un clip.](images/clip.png)

Puede obtener este resultado mediante el uso de capas con una máscara de geometría o el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de opacidad.

A continuación se muestra un ejemplo en el que se usa una capa:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Este es un ejemplo que usa el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


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



En este ejemplo de código, cuando se llama al método PushLayer, no se pasa una capa creada de la aplicación. Direct2D crea una capa. Direct2D es capaz de administrar la asignación y destrucción de este recurso sin ninguna implicación de la aplicación. Esto permite a Direct2D volver a usar las capas internamente y aplicar optimizaciones de administración de recursos.

En Windows 8 se han realizado muchas optimizaciones para el uso de capas y se recomienda intentar usar las API de capa en lugar de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) siempre que sea posible.

### <a name="pushlayer-in-windows-8"></a>PushLayer en Windows 8

La interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) se deriva de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y es la clave para mostrar el contenido de Direct2D en Windows 8. para obtener más información sobre esta interfaz, consulte [dispositivos y contextos de dispositivos](devices-and-device-contexts.md). Con la interfaz de contexto del dispositivo, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar null al método [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D administra automáticamente el recurso de capa y puede compartir recursos entre capas y gráficos de efectos.

### <a name="axis-aligned-clips"></a>Clips alineados con el eje

Si la región que se va a recortar se alinea con el eje de la superficie de dibujo, en lugar de arbitrario. Este caso es adecuado para usar un rectángulo de recorte en lugar de una capa. La ganancia de rendimiento es más para la geometría con alias que la geometría con suavizado de contorno. Para obtener más información sobre los clips alineados del eje, vea el tema [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interoperabilidad de DXGI: evitar modificadores frecuentes

Direct2D puede interoperar sin problemas con las superficies de Direct3D. Esto es muy útil para crear aplicaciones que presentan una mezcla de contenido 2D y 3D. Pero cada cambio entre dibujar contenido de Direct2D y Direct3D afecta al rendimiento.

Al representar en una superficie de DXGI, Direct2D guarda el estado de los dispositivos de Direct3D durante su representación y lo restaura cuando se completa la representación. Cada vez que se completa un lote de representación de Direct2D, se paga el costo de esta operación de guardar y restaurar y el costo de vaciar todas las operaciones 2D y, sin embargo, el dispositivo Direct3D no se vacía. Por lo tanto, para aumentar el rendimiento, limite el número de conmutadores de representación entre Direct2D y Direct3D.

## <a name="know-your-pixel-format"></a>Conozca el formato de píxel

Al crear un destino de representación, puede usar la estructura [**de \_ \_ formato de píxel de D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) para especificar el formato de píxel y el modo alfa utilizados por el destino de representación. Un canal alfa forma parte del formato de píxel que especifica el valor de cobertura o la información de opacidad. Si un destino de representación no utiliza el canal alfa, debe crearse mediante el modo [**alfa D2D1 \_ \_ \_ omitir**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) el modo alfa. Esto revierte el tiempo dedicado a la representación de un canal alfa que no es necesario.

Para obtener más información sobre los formatos de píxeles y los modos alfa, vea [formatos de píxeles compatibles y modos alfa](supported-pixel-formats-and-alpha-modes.md).

## <a name="scene-complexity"></a>Complejidad de la escena

Cuando se analizan las zonas activas de rendimiento en una escena que se va a representar, se sabe si la escena está limitada por el límite de velocidad de relleno o el límite de vértices puede proporcionar información útil.

-   Velocidad de relleno: la velocidad de relleno hace referencia al número de píxeles que una tarjeta gráfica puede representar y escribir en la memoria de vídeo por segundo.
-   Límite de vértice: una escena está enlazada al vértice cuando contiene mucha geometría compleja.

### <a name="understand-scene-complexity"></a>Descripción de la complejidad de la escena

Puede analizar la complejidad de la escena modificando el tamaño del destino de representación. Si las mejoras de rendimiento están visibles para una reducción proporcional del tamaño del destino de representación, la aplicación tiene un límite de velocidad de relleno. De lo contrario, la complejidad de la escena es el cuello de botella del rendimiento.

Cuando una escena tiene un límite de velocidad de relleno, reducir el tamaño del destino de representación puede mejorar el rendimiento. Esto se debe a que el número de píxeles que se va a representar se reducirá proporcionalmente con el tamaño del destino de representación.

Cuando una escena está enlazada a vértices, reduzca la complejidad de la geometría. Pero recuerde que esto se hace a costa de la calidad de la imagen. Por lo tanto, se debe tomar una decisión exhaustiva sobre el compromiso entre la calidad deseada y el rendimiento necesario.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Mejorar el rendimiento de las aplicaciones de impresión en Direct2D

[Direct2D](./direct2d-portal.md) ofrece compatibilidad con la impresión. Puede enviar los mismos comandos de dibujo de Direct2D (en forma de listas de comandos de Direct2D) al control de impresión de Direct2D para la impresión, si no sabe a qué dispositivos está dibujando o cómo se traduce el dibujo a la impresión.

Puede ajustar aún más el uso del control de impresión de [direct2d](./direct2d-portal.md) y los comandos de dibujo de direct2d para ofrecer resultados de impresión con un mejor rendimiento.

El control de impresión de [direct2d](./direct2d-portal.md) genera mensajes de depuración cuando ve un patrón de código de direct2d que conduce a una menor calidad de impresión o rendimiento (por ejemplo, los patrones de código que se enumeran más adelante en este tema) para recordarle dónde puede evitar problemas de rendimiento. Para ver los mensajes de depuración, debe habilitar la [capa de depuración de Direct2D](direct2ddebuglayer-portal.md) en el código. Consulte [depuración de mensajes](direct2ddebuglayer-debugmessages.md) para obtener instrucciones para habilitar la salida de mensajes de depuración.

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Establecer los valores de propiedad correctos al crear el control de impresión D2D

Existen tres propiedades que se pueden establecer al crear el control de impresión de [Direct2D](./direct2d-portal.md) . Dos de estas propiedades afectan al modo en que el control de impresión de Direct2D controla determinados comandos de Direct2D y, a su vez, afecta al rendimiento general.

-   Modo de subconjunto de fuentes: el control de impresión de [Direct2D](./direct2d-portal.md) subdefine los recursos de fuente usados en cada página antes de enviar la página que se va a imprimir. Este modo reduce el tamaño de los recursos de página necesarios para imprimir. En función del uso de fuentes de la página, puede elegir diferentes modos de subconjunto de fuentes para obtener el mejor rendimiento.
    -   [**D2D1 \_ IMPRIMIR \_ el \_ modo de subconjunto de fuentes \_ \_ predeterminado**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) proporciona el mejor rendimiento de impresión en la mayoría de los casos. Cuando se establece en este modo, el control de impresión de [Direct2D](./direct2d-portal.md) usa una estrategia heurística para decidir cuándo se deben subconjuntos de las fuentes.
    -   En el caso de los trabajos de impresión cortos con una o dos páginas, se recomienda [**D2D1 \_ imprimir el modo de \_ \_ subconjunto de fuentes \_ \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , donde el control de impresión de [Direct2D](./direct2d-portal.md) crea e inserta recursos de fuentes en cada página y, a continuación, descarta ese subconjunto de fuentes después de imprimir la página. Esta opción garantiza que cada página se puede imprimir inmediatamente después de que se genere, pero aumenta ligeramente el tamaño de los recursos de página necesarios para la impresión (con los subconjuntos de fuentes grandes normalmente).
    -   Para los trabajos de impresión con muchas páginas de texto y tamaños de fuente pequeños (como 100 páginas de texto que usan una sola fuente), se recomienda [**D2D1 \_ imprimir el modo de \_ \_ subconjunto de fuentes \_ \_ ninguno**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), donde el control de impresión de [Direct2D](./direct2d-portal.md) no represente los recursos de fuente; en su lugar, envía los recursos de fuente originales junto con la página que usa la fuente por primera vez y vuelve a usar los recursos de fuente para páginas posteriores sin reenviarlos.
-   PPP de rasterización: cuando el control de impresión de [direct2d](./direct2d-portal.md) debe rasterizar comandos de direct2d durante la conversión de DIRECT2D-XPS, usa este PPP para la rasterización. En otras palabras, si la página no tiene ningún contenido rasterizado, el establecimiento de un valor de PPP no cambiará el rendimiento y la calidad. En función del uso de la rasterización en la página, puede elegir diferentes PPP de rasterización para el mejor equilibrio entre fidelidad y rendimiento.
    -   150 es el valor predeterminado si no se especifica un valor al crear el control de impresión de [Direct2D](./direct2d-portal.md) , que es el mejor equilibrio de la calidad de impresión y el rendimiento de impresión en la mayoría de los casos.
    -   Los valores de PPP más altos suelen dar lugar a una mejor calidad de impresión (al igual que en los detalles conservados), pero menor rendimiento debido a los mapas de bits más grandes que genera. No se recomienda ningún valor de PPP superior a 300, ya que no presentará información adicional que sea perceptible visualmente por los ojos humanos.
    -   Los PPP inferiores pueden significar un mejor rendimiento, pero también pueden producir una calidad inferior.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Evite usar determinados patrones de dibujo de Direct2D

Hay diferencias entre lo que [Direct2D](./direct2d-portal.md) puede representar visualmente y lo que el subsistema de impresión puede mantener y transportar a lo largo de toda la canalización de impresión. El control de impresión de Direct2D une estos huecos, ya sea aproximando o rasterizando primitivas de Direct2D que el subsistema de impresión no admite de forma nativa. Esta aproximación suele dar lugar a una menor fidelidad de impresión, menor rendimiento de la impresión o ambos. Por lo tanto, aunque un cliente puede usar los mismos patrones de dibujo para la representación de pantalla y de impresión, no es idóneo en todos los casos. Es mejor no usar modelos y primitivos de Direct2D tanto como sea posible para la ruta de impresión, o para hacer su propia rasterización en la que tenga control total sobre la calidad y el tamaño de las imágenes rasterizadas.

A continuación se muestra una lista de los casos en los que el rendimiento y la calidad de la impresión no son ideales y es posible que desee considerar la posibilidad de variar la ruta de acceso del código para obtener un rendimiento óptimo de la impresión.

-   Evite usar el modo de mezcla primitivo que no sea [**D2D1 \_ primitiva \_ Blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Evite el uso de modos de composición al dibujar una imagen que no sea el [**\_ origen de modo compuesto D2D1 \_ \_ \_ sobre**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) y el **destino de \_ modo compuesto D2D1 \_ \_ \_ sobre**.
-   Evite dibujar un archivo de metadatos GDI.
-   Evite insertar un recurso de capa que copie el fondo de origen (llamando a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) con el paso [**de la \_ capa D2D1 \_ OPTIONS1 \_ Initialize \_ de \_ background**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) a la **\_ capa D2D1 \_ PARAMETERS1** struct).
-   Evite crear un pincel de mapa de bits o un pincel de imagen con la \_ abrazadera del modo de extensión D2D1 \_ \_ . Se recomienda usar el reflejo del modo de extensión de D2D1 \_ \_ \_ si no le interesan los píxeles que se encuentran fuera de la imagen enlazada (por ejemplo, la imagen conectada al pincel se sabe que es mayor que la región de destino rellena).
-   Evite dibujar mapas de bits con [transformaciones de perspectiva](3d-perspective-transform.md).

### <a name="draw-text-in-a-direct-and-plain-way"></a>Dibujar texto de forma directa y sin formato

Direct2D tiene varias optimizaciones al representar textos para mostrar un mejor rendimiento y/o una mejor calidad visual. Pero no todas las optimizaciones mejoran el rendimiento y la calidad de la impresión, ya que la impresión en papel está normalmente en un valor de PPP mucho mayor, y la impresión no necesita incluir escenarios como la animación. Por lo tanto, se recomienda que dibuje directamente el texto o glifos originales y que evite cualquiera de las siguientes optimizaciones al crear la lista de comandos para imprimir.

-   Evite dibujar texto con el método [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) .
-   Evite dibujar texto en modo de alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Dibujar los mapas de bits originales siempre que sea posible

Si el mapa de bits de destino es JPEG, PNG, TIFF o JPEG-XR, puede crear un mapa de bits de WIC desde un archivo de disco o desde una secuencia en memoria, crear un mapa de bits de [direct2d](./direct2d-portal.md) a partir de ese mapa de bits de WIC mediante [**ID2D1DeviceContext:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))y, finalmente, pasar directamente ese mapa Al hacerlo, el control de impresión de Direct2D puede volver a usar la secuencia de mapa de bits, lo que suele provocar un mejor rendimiento de la impresión (omitiendo la codificación y descodificación de mapas de bits redundantes) y una mejor calidad de impresión (cuando se conservan los metadatos, como los perfiles de color, en el mapa de bits).

El dibujo del mapa de bits original proporciona las siguientes ventajas para las aplicaciones.

-   En general, la impresión de [Direct2D](./direct2d-portal.md) conserva la información original (sin pérdida o ruido) hasta el final de la canalización, especialmente cuando las aplicaciones no saben (o no quieren saber) los detalles de la canalización de impresión (por ejemplo, la impresora en la que se imprime, qué PPP es la impresora de destino, etc.).
-   En muchos casos, retrasar la rasterización de mapas de bits supone un mejor rendimiento (como cuando se imprime una foto de 96DPI en una impresora 600dpi).
-   En algunos casos, el paso de las imágenes originales es la única manera de respetar la alta fidelidad (como los perfiles de color incrustados).

Sin embargo, no puede optar por esta optimización porque:

-   Al consultar la información de la impresora y la rasterización temprana, puede rasterizar el contenido por sí mismo con control total sobre el aspecto final del papel.
-   En algunos casos, la rasterización temprana podría mejorar realmente el rendimiento de un extremo a otro (por ejemplo, la impresión de las fotos de tamaño).
-   En algunos casos, el paso de los mapas de bits originales requiere un cambio significativo en la arquitectura de código existente (como las rutas de carga de retardo de imagen y de actualización de recursos que se encuentran en determinadas aplicaciones).

## <a name="conclusion"></a>Conclusión

Aunque Direct2D tiene aceleración de hardware y está pensado para un alto rendimiento, debe usar las características correctamente para maximizar el rendimiento. Las técnicas que examinamos aquí se derivan del estudio de escenarios comunes y es posible que no se apliquen a todos los escenarios de aplicaciones.

 

 

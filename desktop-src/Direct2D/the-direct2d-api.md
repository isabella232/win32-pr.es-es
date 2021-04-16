---
title: Introducción a la API de Direct2D
description: Proporciona información general sobre el modelo de objetos de Direct2D.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, acerca de
- Direct2D, archivos de encabezado
- Direct2D, modelo de objetos
- Direct2D, interfaces
- Interfaz ID2D1Factory
- Direct2D, destinos de representación
- destinos de representación, acerca de
- Direct2D, dibujar comandos
- destinos de representación, dibujar comandos
- Direct2D, control de errores
- destinos de representación, control de errores
- el control de errores
- pinceles
- destinos de representación, pinceles
- geometries
- Direct2D, geometrías
- mapas de bits para Direct2D
- Direct2D, mapas de bits
- Primitives
- Direct2D, primitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858d03f626fe337b174f074d7725dcb1a636b463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685746"
---
# <a name="direct2d-api-overview"></a>Introducción a la API de Direct2D

Direct2D proporciona una API, similar a Direct3D, para su uso con C o C++. La API expone una variedad de funcionalidades relacionadas con el dibujo:

-   Representan los destinos para la presentación y la representación fuera de la pantalla mediante Direct2D, Direct3D o GDI.
-   Objetos para administrar el estado del dibujo, como transformaciones del espacio de coordenadas y modos de suavizado de contorno.
-   Representaciones para datos geométricos y funciones para el procesamiento de geometría.
-   Funcionalidad de representación de mapas de bits, geometrías y texto.
-   Aprovisiona el uso de contenido gráfico creado con GDI o Direct3D.

En este tema se proporciona información general sobre los objetos que componen la API de Direct2D. Contiene las secciones siguientes:

-   [Archivos de encabezado de Direct2D](#direct2d-header-files)
-   [Interfaces de Direct2D](#direct2d-interfaces)
-   [La interfaz ID2D1Factory](#the-id2d1factory-interface)
-   [Destinos de representación](#render-targets)
    -   [Características de destino de representación](#render-target-features)
    -   [Representar recursos de destino](#render-target-resources)
    -   [Dibujar comandos](#drawing-commands)
    -   [Tratamiento de errores](#error-handling)
-   [Dibujar recursos](#drawing-resources)
    -   [Pinceles](#brushes)
    -   [Geometrías](#geometries)
    -   [Mapas de bits](#bitmaps)
-   [Dibujar texto](#drawing-text)
-   [Primitivas de Direct2D](#direct2d-primitives)
-   [Temas relacionados](#related-topics)

## <a name="direct2d-header-files"></a>Archivos de encabezado de Direct2D

La API de Direct2D se define mediante los siguientes archivos de encabezado.

| Archivo de encabezado         | Descripción                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1. h              | Define las versiones de C y C++ de la API de Direct2D principal.                                                                      |
| d2d1helper. h        | Define las funciones auxiliares, las clases y las estructuras de C++.                                                                       |
| d2dbasetypes. h      | Define primitivos de dibujo para Direct2D, como puntos y rectángulos. Este encabezado está incluido en d2d1. h.                 |
| d2derr. h            | Define los códigos de error para Direct2D. Este encabezado está incluido en d2d1. h.                                                   |
| d2d1 \_ 1. h           | Define las versiones de C y C++ de la API de Direct2D principal para Windows 8 y versiones posteriores.                                              |
| d2d1 \_ 1helper. h     | Define las funciones auxiliares, las clases y las estructuras de C++ para Windows 8 y versiones posteriores.                                               |
| d2d1effects. h       | Define las versiones de C y C++ de la parte de efectos de imagen de la API de Direct2D para Windows 8 y versiones posteriores.                            |
| d2d1effecthelpers. h | Define las funciones auxiliares de C++, las clases y las estructuras de la parte de efectos de imagen de la API de Direct2D para Windows 8 y versiones posteriores. |



 

Para usar Direct2D, la aplicación debe incluir el archivo de encabezado d2d1. h.

Para compilar una aplicación de Direct2D, agregue d2d1. lib a la lista de bibliotecas. Puede encontrar d2d1. h y d2d1. lib en el [Kit de desarrollo de software (SDK) de Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

En las secciones siguientes se describen algunas de las interfaces comunes que proporciona la API de Direct2D.

## <a name="direct2d-interfaces"></a>Interfaces de Direct2D

En la raíz de la API de Direct2D se encuentran las interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) y [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) . Un objeto **ID2D1Factory** crea objetos **ID2D1Resource** y sirve como punto de partida para usar Direct2D. Todos los demás objetos de Direct2D heredan de la interfaz **ID2D1Resource** . Hay dos tipos de recursos de Direct2D: recursos independientes del dispositivo y recursos dependientes del dispositivo.

-   Los recursos independientes del dispositivo no están asociados a un dispositivo de representación determinado y pueden persistir durante la vida de una aplicación.
-   Los recursos dependientes del dispositivo se asocian a un dispositivo de representación determinado y dejan de funcionar si se quita ese dispositivo.

(Para obtener más información acerca de los recursos y el uso compartido de recursos, consulte la [Introducción a los recursos](resources-and-resource-domains.md)).

## <a name="the-id2d1factory-interface"></a>La interfaz ID2D1Factory

La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) es el punto de partida para usar Direct2D. Se usa un **ID2D1Factory** para crear instancias de recursos de Direct2D. Para crear un ID2D1Factory, use uno de los métodos [**CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) .

Un generador define un conjunto de métodos de creación de *recursos* que pueden generar los siguientes recursos de dibujo:

-   Los destinos de representación son objetos que representan comandos de dibujo.
-   Los bloques de estado de dibujo son objetos que almacenan información de estado de dibujo, como el modo de transformación y suavizado de contorno actual.
-   Las geometrías son objetos que representan formas simples y potencialmente complejas.

Uno de los objetos más útiles que puede crear un generador es el [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que se describe en la sección siguiente.

## <a name="render-targets"></a>Destinos de representación

Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo. Hay varios tipos de destinos de representación que se pueden usar para representar gráficos de las siguientes maneras:

-   Los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representan el contenido en una ventana.
-   Los objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) se representan en un contexto de dispositivo GDI.
-   Los objetos de destino de representación de mapas de bits representan el contenido en un mapa de bits fuera de la pantalla.
-   Los objetos de destino de representación de DXGI se representan en una superficie de DXGI para su uso con Direct3D.

Dado que un destino de representación está asociado a un dispositivo de representación determinado, es un recurso dependiente del dispositivo y deja de funcionar si se quita el dispositivo.

### <a name="render-target-features"></a>Características de destino de representación

Puede especificar si un destino de representación debe usar la aceleración de hardware y si el equipo local o remoto debe representar la pantalla remota. Los destinos de representación pueden configurarse para la representación con alias o con suavizado de contorno. En el caso de las escenas de representación con un gran número de primitivas, un desarrollador también puede representar gráficos 2D en modo de alias y usar el suavizado de contorno de muestreo múltiple para lograr una mayor escalabilidad.

Los destinos de representación también pueden agrupar las operaciones de dibujo en capas representadas por la interfaz [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . Las capas son útiles para recopilar operaciones de dibujo que se van a componer juntas al representar un fotograma. En algunos escenarios, puede ser una alternativa útil a la representación en un destino de representación de mapas de bits y, a continuación, volver a usar el contenido del mapa de bits, ya que los costos de asignación para la disposición en capas son menores que para un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Los destinos de representación pueden crear nuevos destinos de representación que son compatibles con ellos mismos, lo que resulta útil para la representación fuera de pantalla intermedia, a la vez que conserva las distintas propiedades de representación y destino que se establecieron en el original.

También es posible representar usando GDI en un destino de representación de Direct2D llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un destino de representación para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tiene los métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) y [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) en él que se pueden usar para recuperar un contexto de dispositivo GDI. La representación a través de GDI solo es posible si el destino de representación se creó con el conjunto de marcadores [**compatible con GDI de uso de destino de representación de D2D1 \_ \_ \_ \_ \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Esto resulta útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de presentar con GDI. Para obtener más información, vea [información general sobre la interoperabilidad de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Representar recursos de destino

Al igual que un generador, un destino de representación puede crear recursos de dibujo. Los recursos creados por un destino de representación son recursos dependientes del dispositivo (al igual que el destino de representación). Un destino de representación puede crear los siguientes tipos de recursos:

-   Mapas de bits
-   Pinceles
-   Capas
-   Mallas

### <a name="drawing-commands"></a>Dibujar comandos

Para representar el contenido, se usan los métodos de dibujo del destino de representación. Antes de empezar a dibujar, se llama al método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Una vez finalizado el dibujo, se llama al método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre estas llamadas, se usan los métodos Draw y Fill para representar los recursos de dibujo. La mayoría de los métodos Draw y Fill toman una forma (una primitiva o una geometría) y un pincel para rellenar o esquematizar la forma.

Los destinos de representación también proporcionan métodos para recortar, aplicar máscaras de opacidad y transformar el espacio de coordenadas.

Direct2D usa un sistema de coordenadas de la mano izquierda: los valores positivos del eje x pasan a los valores correctos y positivos del eje y continúan hacia abajo.

### <a name="error-handling"></a>Tratamiento de errores

Los comandos de dibujo de destino de representación no indican si la operación solicitada se realizó correctamente. Para averiguar si se han producido errores de dibujo, llame al método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) del destino de representación o al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obtener un **HRESULT**.

## <a name="drawing-resources"></a>Dibujar recursos

En las secciones siguientes se describen algunos de los recursos que pueden crear las interfaces de generador y destino de representación.

### <a name="brushes"></a>Pinceles

Un pincel, representado por la interfaz [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) , es un recurso dependiente del dispositivo, creado por un destino de representación, que pinta un área con su salida. Distintos pinceles tienen tipos de salida diferentes. Algunos pinceles pintan un área con un color sólido, otros con un degradado o una imagen. Direct2D proporciona cuatro tipos de pinceles:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta un área con un color sólido.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta un área con un degradado lineal que combina dos o más colores en una línea, el eje de degradado.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta un área con un degradado radial que combina dos o más colores alrededor de una elipse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta un área con un mapa de bits.

Para crear un pincel, se usa uno de los métodos de pincel [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create *<Type>* , como [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)). Los pinceles se pueden usar con los métodos de dibujo y relleno de destino de representación, ya sea para pintar un trazo o un contorno de forma, o como una máscara de opacidad.

Para obtener más información sobre los pinceles, vea [información general sobre los pinceles](direct2d-brushes-overview.md).

### <a name="geometries"></a>Geometrías

Además de los primitivos básicos de dibujo, como puntos, rectángulos y elipses, Direct2D proporciona la interfaz [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para describir formas simples y complejas. Las interfaces que heredan de **ID2D1Geometry** definen distintos tipos de formas, como [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) para representar rectángulos, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) para representar rectángulos redondeados y [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) para representar puntos suspensivos.

Se pueden crear formas más complejas mediante la interfaz [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) para especificar una serie de figuras compuestas de líneas, curvas y arcos. **ID2D1GeometrySink** se pasa al método Open de un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para generar una geometría compleja. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) también se puede usar con la API de DirectWrite para extraer los contornos de ruta de acceso del texto con formato para la representación artística.

Las interfaces Geometry proporcionan métodos para manipular formas mediante la ampliación o la simplificación de las geometrías existentes, o mediante la generación de la intersección o unión de varias geometrías. También proporcionan métodos para determinar si las geometrías se intersectan o superponen, recuperan información de los límites, calculan el área o la longitud de una geometría y interpolan ubicaciones a lo largo de una geometría. Direct2D también proporciona la capacidad de crear una malla de triángulos que se tesela desde una geometría.

Para crear una geometría, se usa uno de los métodos [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory):: Create *<Type>* Geometry, como [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Un objeto Geometry es un recurso independiente del dispositivo.

Para representar una geometría, se usan los métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) de un destino de representación.

Para obtener más información sobre las geometrías, vea la [información general sobre las geometrías](direct2d-geometries-overview.md).

### <a name="bitmaps"></a>Mapas de bits

Direct2D no proporciona métodos para cargar o almacenar mapas de bits; en su lugar, permite crear mapas de bits mediante el [componente de creación de imágenes de Windows (WIC)](../wic/-wic-about-windows-imaging-codec.md). Los recursos de mapa de bits se pueden cargar mediante WIC y luego usarse para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a través del método [**ID2D1RenderTarget:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) .

Los mapas de bits también se pueden crear a partir de datos en memoria que se configuraron a través de otros medios. Una vez creado un mapa de bits, se puede dibujar mediante el método [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) de destino de representación o con un pincel de mapa de bits.

Dado que la creación de recursos de mapa de bits en destinos de representación de hardware suele ser una operación costosa, Direct2D puede actualizar el contenido de un mapa de bits (o parte del mapa de bits) mediante los métodos [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)y [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) . El uso de estos métodos puede ahorrar potencialmente los costos asociados a las asignaciones de texturas de GPU adicionales.

## <a name="drawing-text"></a>Dibujar texto

Direct2D se diseñó para trabajar con las operaciones de texto de la nueva API de texto, DirectWrite. Para que el uso de la API de DirectWrite sea más sencillo, los destinos de representación proporcionan tres métodos para representar los recursos de texto de DirectWrite: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)y [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Dado que Direct2D usa la GPU para el proceso de representación de texto ClearType, Direct2D proporciona menor uso de CPU que GDI para las operaciones de texto y una mejor escalabilidad a medida que se dispone de más capacidad de procesamiento de GPU.

[**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) está diseñado para los escenarios más sencillos que implican la representación de una cadena de texto Unicode con un formato mínimo. Se proporciona un diseño más complejo y una flexibilidad tipográfica a través del método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , que usa un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para especificar el contenido y el formato que se va a representar. **IDWriteTextLayout** permite especificar el formato individual de las subcadenas de texto y otras opciones avanzadas de tipografía.

En escenarios en los que se requiere un control preciso del diseño de nivel de glifo, el método [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) se puede usar junto con los recursos de medida proporcionados por [DirectWrite](../directwrite/direct-write-portal.md).

Para usar la API de DirectWrite, incluya el encabezado dwrite. h. Como Direct2D, DirectWrite usa un generador, [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para crear objetos de texto. Use la función [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para crear un generador y, a continuación, use los métodos Create para crear recursos de DirectWrite (como [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))).

Para obtener más información sobre DirectWrite, consulte el tema [Introducing directwrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Primitivas de Direct2D

Direct2D define un conjunto de primitivos que son similares a los proporcionados por otras API de dibujo. Proporciona una estructura de color, una estructura de matriz para realizar transformaciones y versiones de punto flotante y entero de puntos, rectángulos, elipses y estructuras de tamaño. Normalmente, se usan las versiones de punto flotante de estas estructuras.

No se usa un generador ni un destino de representación para crear instancias de primitivas de Direct2D. Puede crearlas directamente o usar los métodos auxiliares definidos en d2d1helper. h para crearlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[Ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introducción a DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Información general sobre recursos](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
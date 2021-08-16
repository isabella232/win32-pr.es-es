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
- Direct2D, comandos de dibujo
- destinos de representación, comandos de dibujo
- Direct2D, control de errores
- destinos de representación, control de errores
- el control de errores
- pinceles
- destinos de representación, pinceles
- geometries
- Direct2D, geometrías
- mapas de bits para Direct2D
- Direct2D, mapas de bits
- Primitivas
- Direct2D, primitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f318e3542d54ee92817193ef6b749a3ba1cf4678407ca7a12f28c6c187ae86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074999"
---
# <a name="direct2d-api-overview"></a>Introducción a la API de Direct2D

Direct2D proporciona una API, similar a Direct3D, para su uso con C o C++. La API expone una variedad de funcionalidades relacionadas con el dibujo:

-   Representar destinos para la representación en pantalla y fuera de la pantalla mediante Direct2D, Direct3D o GDI.
-   Objetos para administrar el estado de dibujo, como transformaciones de espacio de coordenadas y modos de suavizado de contorno.
-   Representaciones para datos geométricos y funciones para el procesamiento de geometría.
-   Funcionalidad de representación para mapas de bits, geometrías y texto.
-   Aprovisiona para usar contenido gráfico creado mediante GDI o Direct3D.

En este tema se proporciona información general sobre los objetos que integran la API de Direct2D. Contiene las secciones siguientes:

-   [Archivos de encabezado de Direct2D](#direct2d-header-files)
-   [Direct2D Interfaces](#direct2d-interfaces)
-   [La interfaz ID2D1Factory](#the-id2d1factory-interface)
-   [Destinos de representación](#render-targets)
    -   [Representar características de destino](#render-target-features)
    -   [Representación de recursos de destino](#render-target-resources)
    -   [Comandos de dibujo](#drawing-commands)
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
| d2d1.h              | Define las versiones de C y C++ de la API principal de Direct2D.                                                                      |
| d2d1helper.h        | Define funciones auxiliares, clases y estructuras de C++.                                                                       |
| d2dbasetypes.h      | Define primitivas de dibujo para Direct2D, como puntos y rectángulos. Este encabezado se incluye con d2d1.h.                 |
| d2derr.h            | Define los códigos de error de Direct2D. Este encabezado se incluye con d2d1.h.                                                   |
| d2d1 \_ 1.h           | Define las versiones de C y C++ de la API principal de Direct2D para Windows 8 y versiones posteriores.                                              |
| d2d1 \_ 1helper.h     | Define funciones auxiliares, clases y estructuras de C++ para Windows 8 y versiones posteriores.                                               |
| d2d1effects.h       | Define las versiones de C y C++ de los efectos de imagen que forman parte de la API de Direct2D para Windows 8 y versiones posteriores.                            |
| d2d1effecthelpers.h | Define funciones auxiliares, clases y estructuras de C++ de la parte de efectos de imagen de la API de Direct2D para Windows 8 y versiones posteriores. |



 

Para usar Direct2D, la aplicación debe incluir el archivo de encabezado d2d1.h.

Para compilar una aplicación de Direct2D, agregue d2d1.lib a la lista de bibliotecas. Puede encontrar d2d1.h y d2d1.lib en [Windows Software Development Kit (SDK) para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

En las secciones siguientes se describen algunas de las interfaces comunes proporcionadas por la API de Direct2D.

## <a name="direct2d-interfaces"></a>Direct2D Interfaces

En la raíz de la API de Direct2D se encuentran las interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) e [**ID2D1Resource.**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) Un **objeto ID2D1Factory** crea objetos **ID2D1Resource** y actúa como punto de partida para usar Direct2D. Todos los demás objetos de Direct2D heredan de **la interfaz ID2D1Resource.** Hay dos tipos de recursos de Direct2D: recursos independientes del dispositivo y recursos dependientes del dispositivo.

-   Los recursos independientes del dispositivo no están asociados a un dispositivo de representación determinado y pueden conservarse durante la vida útil de una aplicación.
-   Los recursos dependientes del dispositivo están asociados a un dispositivo de representación determinado y dejan de funcionar si se quita ese dispositivo.

(Para obtener más información sobre los recursos y el uso compartido de recursos, vea Información [general sobre recursos).](resources-and-resource-domains.md)

## <a name="the-id2d1factory-interface"></a>La interfaz ID2D1Factory

La [**interfaz ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) es el punto de partida para usar Direct2D. Se usa **id2D1Factory para** crear instancias de recursos de Direct2D. Para crear una instancia de ID2D1Factory, use uno de los [**métodos CreateFactory.**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory)

Un generador define un conjunto de métodos Create *Resource* que pueden generar los siguientes recursos de dibujo:

-   Los destinos de representación son objetos que representan comandos de dibujo.
-   Los bloques de estado de dibujo son objetos que almacenan información de estado de dibujo, como la transformación actual y el modo de suavizado de contorno.
-   Las geometrías son objetos que representan formas simples y potencialmente complejas.

Uno de los objetos más útiles que puede crear un generador [**es id2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)que se describe en la sección siguiente.

## <a name="render-targets"></a>Destinos de representación

Un destino de representación es un recurso que hereda de la [**interfaz ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo. Hay varios tipos de destinos de representación que se pueden usar para representar gráficos de las maneras siguientes:

-   [**Los objetos ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representan el contenido en una ventana.
-   [**Los objetos ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) se representan en un contexto de dispositivo GDI.
-   Los objetos de destino de representación de mapa de bits representan el contenido en un mapa de bits fuera de la pantalla.
-   Los objetos de destino de representación DXGI se representan en una superficie DXGI para su uso con Direct3D.

Dado que un destino de representación está asociado a un dispositivo de representación determinado, es un recurso dependiente del dispositivo y deja de funcionar si se quita el dispositivo.

### <a name="render-target-features"></a>Representar características de destino

Puede especificar si un destino de representación debe usar la aceleración de hardware y si el equipo local o remoto debe representar la pantalla remota. Los destinos de representación se pueden configurar para la representación con alias o suavizado de contorno. Para representar escenas con un gran número de primitivas, un desarrollador también puede representar gráficos 2D en modo con alias y usar el suavizado de contorno de múltiples muestras D3D para lograr una mayor escalabilidad.

Los destinos de representación también pueden agrupar las operaciones de dibujo en capas representadas por la [**interfaz ID2D1Layer.**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) Las capas son útiles para recopilar operaciones de dibujo que se van a componer juntas al representar un marco. En algunos escenarios, esto puede ser una alternativa útil a la representación en un destino de representación de mapa de bits y, a continuación, volver a usar el contenido del mapa de bits, ya que los costos de asignación de capas son inferiores a los de [**id2D1BitmapRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)

Los destinos de representación pueden crear nuevos destinos de representación compatibles con ellos mismos, lo que resulta útil para la representación intermedia fuera de la pantalla, al tiempo que se conservan las distintas propiedades de destino de representación establecidas en el original.

También es posible representar mediante GDI en un destino de representación de Direct2D llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un destino de representación para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tiene métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) y [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que se pueden usar para recuperar un contexto de dispositivo GDI. La representación a través de GDI solo es posible si el destino de representación se creó con la marca COMPATIBLE de [**\_ \_ \_ \_ GDI \_ RENDER TARGET USAGE de D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) establecida. Esto es útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de representar con GDI. Para obtener más información, vea Introducción a la interoperabilidad de [Direct2D y GDI.](direct2d-and-gdi-interoperation-overview.md)

### <a name="render-target-resources"></a>Representación de recursos de destino

Al igual que un generador, un destino de representación puede crear recursos de dibujo. Los recursos creados por un destino de representación son recursos dependientes del dispositivo (al igual que el destino de representación). Un destino de representación puede crear los siguientes tipos de recursos:

-   Mapas de bits
-   Pinceles
-   Capas
-   Mallas

### <a name="drawing-commands"></a>Comandos de dibujo

Para representar el contenido, use los métodos de dibujo de destino de representación. Antes de empezar a dibujar, llame al [**método ID2D1RenderTarget::BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Cuando haya terminado de dibujar, llame al [**método ID2D1RenderTarget::EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Entre estas llamadas, se usan los métodos Draw y Fill para representar los recursos de dibujo. La mayoría de los métodos Draw y Fill toman una forma (primitiva o geometría) y un pincel para rellenar o delinear la forma.

Los destinos de representación también proporcionan métodos para recortar, aplicar máscaras de opacidad y transformar el espacio de coordenadas.

Direct2D usa un sistema de coordenadas con la mano izquierda: los valores positivos del eje X se dirigen a la derecha y los valores positivos del eje Y avanzan hacia abajo.

### <a name="error-handling"></a>Tratamiento de errores

Los comandos de dibujo de destino de representación no indican si la operación solicitada se ha realizado correctamente. Para averiguar si hubo errores de dibujo, llame al método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino de representación o [**al método EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obtener **un HRESULT**.

## <a name="drawing-resources"></a>Dibujar recursos

En las secciones siguientes se describen algunos de los recursos que se pueden crear mediante las interfaces de destino de representación e generador.

### <a name="brushes"></a>Pinceles

Un pincel, representado por la interfaz [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) es un recurso dependiente del dispositivo, creado por un destino de representación, que pinta un área con su salida. Distintos pinceles tienen tipos de salida diferentes. Algunos pinceles pintan un área con un color sólido, otros con un degradado o una imagen. Direct2D proporciona cuatro tipos de pinceles:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta un área con un color sólido.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta un área con un degradado lineal que combina dos o más colores en una línea, el eje de degradado.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta un área con un degradado radial que combina dos o más colores alrededor de una elipse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta un área con un mapa de bits.

Para crear un pincel, use uno de los [**métodos ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create Brush, como *<Type>* [**CreateRadialGradientBrush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) Los pinceles se pueden usar con los métodos Draw y Fill de destino de representación, ya sea para pintar un trazo o contorno de forma, o como una máscara de opacidad.

Para obtener más información sobre los pinceles, vea Información [general sobre pinceles.](direct2d-brushes-overview.md)

### <a name="geometries"></a>Geometrías

Además de los primitivos de dibujo básicos, como puntos, rectángulos y elipses, Direct2D proporciona la interfaz [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para describir formas simples y complejas. Las interfaces que heredan de **ID2D1Geometry** definen diferentes tipos de formas, como [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) para representar rectángulos, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) para representar rectángulos redondeados e [**ID2D1PxpseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) para representar elipses.

Se pueden crear formas más complejas mediante la interfaz [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) para especificar una serie de figuras compuestas de líneas, curvas y arcos. **Id2D1GeometrySink** se pasa al método Open de [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para generar una geometría compleja. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) también se puede usar con la API de DirectWrite para extraer los contornos de ruta de acceso del texto con formato para la representación en desenlazado.

Las interfaces de geometría proporcionan métodos para manipular formas ampliando o simplificando geometrías existentes, o generando la intersección o unión de varias geometrías. También proporcionan métodos para determinar si las geometrías se cruzan o se superponen, recuperan información de límites, computan el área o longitud de una geometría e interpolan ubicaciones a lo largo de una geometría. Direct2D también proporciona la capacidad de crear una malla de triángulos que se tesela a partir de una geometría.

Para crear una geometría, use uno de los métodos [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)::Create *<Type>* Geometry, como [**CreatePathGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) Una geometría es un recurso independiente del dispositivo.

Para representar una geometría, use los métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) de un destino de representación.

Para obtener más información sobre las geometrías, vea Información [general sobre geometrías.](direct2d-geometries-overview.md)

### <a name="bitmaps"></a>Mapas de bits

Direct2D no proporciona métodos para cargar o almacenar mapas de bits; en su lugar, le permite crear mapas de bits mediante [Windows Imaging Component (WIC).](../wic/-wic-about-windows-imaging-codec.md) Los recursos de mapa de bits se pueden cargar mediante WIC y, a continuación, se pueden usar para crear un [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a través del [**método ID2D1RenderTarget::CreateBitmapFromWicBitmap.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap))

Los mapas de bits también se pueden crear a partir de datos en memoria que se configuraron a través de otros medios. Una vez creado un mapa de bits, se puede dibujar mediante el método [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) de destino de representación o con un pincel de mapa de bits.

Dado que la creación de recursos de mapa de bits en destinos de representación de hardware suele ser una operación costosa, Direct2D puede actualizar el contenido de un mapa de bits (o parte del mapa de bits) mediante los métodos [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget) [**y CopyFromMemory.**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) El uso de estos métodos puede ahorrar posiblemente los costos asociados con asignaciones de textura de GPU adicionales.

## <a name="drawing-text"></a>Dibujar texto

Direct2D se diseñó para trabajar con las operaciones de texto de la nueva API de texto, DirectWrite. Para que el uso de DirectWrite API sea más sencillo, los destinos de representación proporcionan tres métodos para representar DirectWrite recursos de texto: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)y [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Dado que Direct2D usa la GPU para el proceso de representación de texto ClearType, Direct2D proporciona un menor uso de CPU que GDI para las operaciones de texto y una mejor escalabilidad a medida que hay más capacidad de procesamiento de GPU disponible.

[**Id2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) está diseñado para los escenarios más sencillos que implican la representación de una cadena de texto Unicode con formato mínimo. Se proporciona un diseño más complejo y flexibilidad tipográfica a través del método [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) que usa un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para especificar el contenido y el formato que se va a representar. **IDWriteTextLayout permite** especificar formatos individuales para subcadenas de texto y otras opciones avanzadas de tipografía.

En escenarios en los que se requiere un control preciso del diseño de nivel de glifo, el método [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) se puede usar junto con las instalaciones de medida proporcionadas [por DirectWrite](../directwrite/direct-write-portal.md).

Para usar la API DirectWrite, incluya el encabezado dwrite.h. Al igual que Direct2D, DirectWrite un generador, [**IDWriteFactory,**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para crear objetos de texto. Use la [**función DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para crear un generador y, a continuación, use sus métodos Create para crear DirectWrite recursos (como [**IDWriteTextFormat).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))

Para obtener más información sobre DirectWrite, vea el tema [Introducing DirectWrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Primitivas de Direct2D

Direct2D define un conjunto de primitivas que son similares a las proporcionadas por otras API de dibujo. Proporciona una estructura de color, una estructura de matriz para realizar transformaciones y versiones de punto flotante y entero de puntos, rectángulos, puntos suspensivos y estructuras de tamaño. Normalmente, se usan las versiones de punto flotante de estas estructuras.

No se usa un generador ni un destino de representación para crear instancias de primitivas de Direct2D. Puede crearlos directamente o usar los métodos auxiliares definidos en d2d1helper.h para crearlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> <dt>

[DirectWrite Hola mundo ejemplo](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introducción a DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Introducción a los recursos](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
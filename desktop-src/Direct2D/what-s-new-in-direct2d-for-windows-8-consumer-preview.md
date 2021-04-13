---
title: Novedades de Direct2D
description: Estas son algunas de las nuevas adiciones a Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359146"
---
# <a name="whats-new-in-direct2d"></a>Novedades de Direct2D

Estas son algunas de las nuevas adiciones a Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Novedades de Windows 10 Creators Update

Se agregaron o actualizaron las siguientes características y API para Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Compatibilidad con la representación de imágenes SVG

A partir de Windows 10 Creators Update, Direct2D proporciona compatibilidad para analizar y dibujar imágenes SVG, lo que permite a los desarrolladores representar los recursos que se producen en sus herramientas de arte vectorial favoritas sin convertirlos primero en imágenes de trama. Use esta característica para mejorar la superficie del disco y el comportamiento de escalado de su iconografía en la aplicación, y use Direct2d nuevas API del modelo de objetos SVG para realizar cambios mediante programación en SVG de la aplicación. Tenga en cuenta que Direct2D solo admite un subconjunto limitado de SVG adecuado para imágenes y no es compatible con todas las características de dibujo SVG. Si necesita compatibilidad con SVG de nivel de explorador o características orientadas a Web de SVG, considere la posibilidad de usar el [control WebView XAML](/uwp/api/Windows.UI.Xaml.Controls.WebView) en su lugar. Para obtener más información, vea los temas siguientes:

-   [Ejemplo de representación de imagen SVG de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Compatibilidad con SVG](svg-support.md)
-   [**ID2D1DeviceContext5:: CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) (método)
-   [**ID2D1DeviceContext5::D método rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   Interfaz [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Compatibilidad mejorada para la administración del color

A partir de Windows 10 Creators Update, Direct2D proporciona capacidades mejoradas de administración del color. Los desarrolladores ya no necesitan un perfil de ICC para usar el efecto de administración del color de Direct2d. ahora pueden usar los espacios de colores de DXGI o crear su propia definición de espacio de colores con parámetros. Para obtener más información, vea los temas siguientes:

-   [Efecto de administración del color](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Novedades de la actualización de aniversario de Windows 10

Las siguientes características y API se agregaron o actualizaron para la actualización de aniversario de Windows 10.

### <a name="improved-support-for-color-fonts"></a>Compatibilidad mejorada para las fuentes de color

A partir de la actualización de aniversario de Windows 10, Direct2D ahora admite la representación de una mayor variedad de formatos de fuente de color, lo que permite a los desarrolladores usar más tipos de fuentes en sus aplicaciones basadas en Direct2D que nunca. Esto incluye la compatibilidad para:

-   La tabla OpenType ' COLR ', que habilita el contenido de vectores compactos en las fuentes. (Se admite desde Windows 8.1).
-   La tabla OpenType ' SVG ', que habilita el contenido SVG en las fuentes.
-   La tabla OpenType ' CBDT ', que permite el contenido del mapa de bits de color en las fuentes.
-   La tabla OpenType ' sbix ', que permite el contenido del mapa de bits de color en las fuentes.

Direct2D admite estos formatos de fuente de color automáticamente cuando está habilitada la marca de [**D2D1 \_ dibujar \_ Opciones de texto \_ \_ habilitar \_ \_ fuente**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) de color. Para obtener más información, vea los temas siguientes:

-   [Fuentes de colores](/windows/desktop/DirectWrite/color-fonts)
-   [Ejemplo de glifo de color de DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Nuevos efectos de imagen

A partir de la actualización de aniversario de Windows 10, Direct2D incluye los efectos AlphaMask, desvanecimiento, opacidad y matiz. Esta funcionalidad estaba previamente disponible a partir de configuraciones específicas de efectos compuestos, ArithmeticComposite y ColorMatrix, pero los nuevos efectos integrados hacen que sea más fácil realizar estas operaciones comunes.

## <a name="whats-new-for-windows-10"></a>Novedades de Windows 10

Se agregaron o actualizaron las siguientes características y API para Windows 10.

### <a name="sprite-batches"></a>Lotes de Sprite

A partir de Windows 10, Direct2D proporciona compatibilidad para crear y representar lotes de Sprite. En comparación con el método [**DrawImage**](id2d1devicecontext-drawimage-overload.md) de uso general, los lotes de Sprite incurren mucho menos por una sobrecarga de CPU por imagen. Esto los hace idóneos en escenarios que implican cientos o miles de imágenes simultáneas, como sprites de juegos o sistemas de partículas. Para obtener más información, vea los temas siguientes:

-   [**ID2D1DeviceContext3:: CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) (método)
-   [**ID2D1DeviceContext3::D rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) métodos)
-   Interfaz [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Mallas de degradado

A partir de Windows 10, Direct2D proporciona un nuevo primitivo para las mallas de degradado. Los ilustradores profesionales suelen usar las mallas de degradado en el software de diseño gráfico, y permiten a los artistas representar formas complejas (incluso fotográficamente realistas) con todas las ventajas de memoria y escalabilidad de vectores. Para obtener más información, vea los temas siguientes:

-   [Muestra de malla de degradado Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ Estructura \_ de \_ revisión de malla de gradiente**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2::D método rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>API de carga de imágenes mejorada

A partir de Windows 10, Direct2D ofrece una nueva API para cargar imágenes, ID2D1ImageSource. El origen de la imagen mejora en las API de carga de imágenes existentes, como CreateBitmapFromWicBitmap, el efecto de origen del mapa de bits y el efecto YCbCr. El origen de la imagen de Direct2D combina las funcionalidades de estas API con la compatibilidad con imágenes arbitrariamente grandes, una fácil integración con la impresión y los efectos, y numerosas optimizaciones, como YCbCr JPEG y JPEG indexado. Para más información, consulte los temas siguientes:

-   [Ejemplo de SDK de ajuste fotográfico de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Compatibilidad mejorada para la representación de entradas manuscritas

A partir de Windows 10, Direct2D proporciona un nuevo primitivo para representar trazos de tinta. Los trazos de lápiz de Direct2D se definen mediante curvas de Bézier, admiten diferentes formas y transformaciones de NIB y pueden tener un grosor fijo o variable. La compatibilidad integrada de Direct2d con los trazos de lápiz permite a las aplicaciones representar fácilmente una tinta más rápida y atractiva que los enfoques anteriores, lo que normalmente requiere que las aplicaciones administren la tinta por sí mismas, como una serie de puntos suspensivos y quadrilaterals. Para obtener más información, vea los temas siguientes:

-   [**Interfaz ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2::D método rawInk**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interfaz ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Vinculación de sombreador de efectos

Los efectos de Direct2D se implementan mediante píxeles HLSL, vértices y/o sombreadores de cálculo. A partir de Windows 10, Direct2D ahora analiza automáticamente los gráficos de efectos para oportunidades de combinar y ejecutar sombreadores individuales juntos. Esto puede proporcionar un aumento significativo del rendimiento. Los consumidores de efectos integrados no tienen que hacer nada para beneficiarse de la vinculación del sombreador de efectos, pero los desarrolladores que creen sus propios efectos personalizados deben seguir las prácticas recomendadas actualizadas para aprovechar la vinculación del sombreador de efectos. Para obtener más información, vea los temas siguientes:

-   [Vinculación del sombreador de efectos](effect-shader-linking.md)
-   [Aplicaciones auxiliares de HLSL para Direct2D](hlsl-helpers.md)
-   [Ejemplo de SDK de efectos personalizados de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

La vinculación del sombreador de efectos está diseñada para no afectar a la salida visual de efectos. Sin embargo, esto no siempre es posible debido a un comportamiento específico en torno a la precisión del efecto y al recorte numérico. Para obtener más información sobre cómo controlar estos comportamientos, vea:

-   [Controlar el recorte numérico y de precisión en los gráficos de efectos](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Nuevos efectos integrados

A partir de Windows 10, Direct2D incluye un amplio conjunto de nuevos efectos integrados que abordan las principales solicitudes de desarrollador y permiten nuevos tipos de escenarios visuales. Los nuevos efectos son:

### <a name="color"></a>Color:

-   [Efecto de RGB a matiz](rgb-to-hue-effect.md)
-   [Efecto de matiz a RGB](hue-to-rgb-effect.md)
-   [efecto de tabla de búsqueda 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Álbum

-   [Efecto de contraste](contrast-effect.md)
-   [Efecto de exposición](exposure-effect.md)
-   [Efecto de escala de grises](grayscale-effect.md)
-   [Efecto resaltado y sombras](highlights-and-shadows-effect.md)
-   [Invertir efecto](invert-effect.md)
-   [Efecto sepia](sepia-effect.md)
-   [Nitidez del efecto](sharpen-effect.md)
-   [Enderezar efecto](straighten-effect.md)
-   [Efecto de temperatura y matiz](temperature-and-tint-effect.md)
-   [Efecto de viñetas](vignette-effect.md)

### <a name="filter"></a>Filtro:

-   [Efecto de detección perimetral](edge-detection-effect.md)

### <a name="stylize"></a>Aplicar

-   [Efecto de relieve](emboss-effect.md)
-   [Efecto de posterización](posterize-effect.md)

### <a name="transparency"></a>Transparencia:

-   [Efecto de clave de croma](chromakey-effect.md)

Los efectos enderezar, saturación, contraste, resaltados y sombras, y temperatura y matiz se muestran en el [ejemplo del SDK de ajuste fotográfico de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).

## <a name="whats-new-for-windows-81"></a>Novedades de Windows 8.1

Las siguientes características y API se agregaron o actualizaron para Windows 8.1.

A partir de Windows 8.1, Direct2D se basa en Direct3D 11,2.

### <a name="geometry-realizations"></a>Realización de geometría

A partir de Windows 8.1, Direct2D ofrece la realización de geometría. Las supuestos de geometría permiten a las aplicaciones mejorar el rendimiento de la representación de geometría en determinadas situaciones, sin algunas de las desventajas de la rasterización de la geometría a un mapa de bits. Para obtener más información, vea los temas siguientes:

-   Interfaz [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**ID2D1DeviceContext1::D método rawgeometryrealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Compatibilidad con imágenes de JPEG YCbCr

A partir de Windows 8.1, Direct2D proporciona compatibilidad para representar datos de imagen en formato JPEG Y'CbCr. Las aplicaciones pueden representar contenido JPEG en su representación Y'CbCr nativa en lugar de descomprimir en BGRA. Esto puede reducir significativamente el consumo de memoria de gráficos y el tiempo de creación de recursos. Para obtener más información, vea los temas siguientes:

-   [Efecto YCbCr](ycbcr-effect.md) de Direct2D
-   Interfaz [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Compatibilidad con formatos comprimidos de bloques (archivos DDS)

A partir de Windows 8.1, Direct2D proporciona compatibilidad con los mapas de bits que contienen los datos de formato de DXGI \_ \_ BC1 \_ UNORM, formato de dxgi \_ \_ BC2 \_ UNORM y el formato de dxgi \_ \_ BC3 \_ UNORM de píxeles. Las aplicaciones pueden reemplazar sus recursos de imagen con imágenes DDS comprimidas en bloque. Esto puede reducir significativamente el consumo de memoria de gráficos y el tiempo de creación de recursos. Para obtener más información, vea los temas siguientes:

-   [**ID2D1DeviceContext:: CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) (método)
-   Interfaz [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Prioridad de representación

A partir de Windows 8.1, Direct2D proporciona compatibilidad con la prioridad de representación por dispositivo. Esta nueva característica permite que las aplicaciones cambien el dispositivo entre la prioridad de representación normal (la predeterminada) y la prioridad de representación baja (en la que el dispositivo no bloqueará otras tareas de representación en el sistema). Se recomienda que las aplicaciones usen una prioridad de representación baja para las tareas que no son críticas para la capacidad de respuesta del usuario, como el contenido de la representación previa, la representación minimizada y otras operaciones que normalmente se realizan en segundo plano. Para obtener más información, vea los temas siguientes:

-   [**ID2D1Device1:: SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) (método)
-   [**D2D1 \_ \_**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority) Enumeración de prioridad de representación

## <a name="whats-new-for-windows-8"></a>Novedades de Windows 8

Se agregaron o actualizaron las siguientes características y API para Windows 8.

Las nuevas interfaces de Direct2D se admiten en Windows 7 con la [actualización de plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) instalada.

La semántica de Direct2d de los dispositivos y los contextos de dispositivo se ha actualizado para que se parezca más a la semántica usada por Direct3D y para proporcionar un funcionamiento conciso en las aplicaciones de la tienda Windows. Consulte [dispositivos y contextos de dispositivo](devices-and-device-contexts.md) para obtener más información.

API relacionadas seleccionadas:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

La API de la lista de comandos permite compartir la ruta de representación de en la representación e impresión de la pantalla. También permite usar primitivas para crear un pincel de imagen para rellenar los primitivos.

API relacionadas seleccionadas:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

Los [efectos de Direct2D](effects-overview.md) son un conjunto de API, nuevo en Windows 8, para aplicar efectos de alta calidad a las imágenes. También incluye las API que le permiten crear sus propios efectos personalizados.

API relacionadas seleccionadas:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

A partir de Windows 8, Direct2D incluye API adicionales para compilar aplicaciones multiproceso. Para más información, consulte [aplicaciones multiproceso de Direct2D](multi-threaded-direct2d-apps.md) .

API relacionadas seleccionadas:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**\_Tipo de fábrica D2D1 \_ \_ \_ multiproceso**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 
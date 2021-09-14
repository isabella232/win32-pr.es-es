---
title: Novedades de Direct2D
description: Estas son algunas de las nuevas adiciones a Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162513"
---
# <a name="whats-new-in-direct2d"></a>Novedades de Direct2D

Estas son algunas de las nuevas adiciones a Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Novedades de Windows 10 Creators Update

Las siguientes características y API se agregaron o actualizaron para Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Compatibilidad con la representación de imágenes SVG

A partir de Windows 10 Creators Update, Direct2D proporciona compatibilidad para analizar y dibujar imágenes SVG, lo que permite a los desarrolladores representar los recursos generados en sus herramientas de arte vectorial favoritas sin convertirlos primero en imágenes de trama. Use esta característica para mejorar la superficie del disco y el comportamiento de escalado de la iconografía en la aplicación, y use las nuevas API del modelo de objetos SVG de Direct2D para realizar cambios mediante programación en svg de la aplicación. Tenga en cuenta que Direct2D solo admite un subconjunto limitado de SVG adecuado para imágenes y no admite todas las características de dibujo SVG. Si necesita compatibilidad SVG de nivel de explorador o características orientadas a web de SVG, considere la posibilidad de usar el [control WebView xaml](/uwp/api/Windows.UI.Xaml.Controls.WebView) en su lugar. Para obtener más información, vea los temas siguientes:

-   [Ejemplo de representación de imágenes SVG de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Compatibilidad con SVG](svg-support.md)
-   [**Método ID2D1DeviceContext5::CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**Método ID2D1DeviceContext5::D rawSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   [**Interfaz ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Compatibilidad mejorada con la administración de colores

A partir Windows 10 Creators Update, Direct2D proporciona funcionalidades mejoradas de administración de colores. Los desarrolladores ya no necesitan un perfil DEER PARA usar el efecto de administración de color de Direct2D. ahora pueden usar espacios de color DXGI o construir su propia definición de espacio de color con parámetros. Para obtener más información, vea los temas siguientes:

-   [Efecto de administración del color](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Novedades de la actualización Windows 10 aniversario

Las siguientes características y API se agregaron o actualizaron para Windows 10 de aniversario.

### <a name="improved-support-for-color-fonts"></a>Compatibilidad mejorada para las fuentes de color

A partir de Windows 10 Anniversary Update, Direct2D ahora admite la representación de una variedad más amplia de formatos de fuente de color, lo que permite a los desarrolladores usar más tipos de fuentes en sus aplicaciones con tecnología Direct2D que nunca. Esto incluye la compatibilidad para:

-   La tabla OpenType "COLR", que permite el contenido vectorial compacto en las fuentes. (Se admite desde Windows 8.1).
-   La tabla OpenType "SVG", que habilita el contenido SVG en las fuentes.
-   La tabla OpenType 'EDITABLET', que habilita el contenido de mapa de bits de color en las fuentes.
-   La tabla OpenType "sbix", que habilita el contenido de mapa de bits de color en las fuentes.

Direct2D admite estos formatos de fuente de color automáticamente cuando la marca [**D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) está habilitada. Para obtener más información, vea los temas siguientes:

-   [Fuentes de colores](/windows/desktop/DirectWrite/color-fonts)
-   [DirectWrite de glifo de color](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Nuevos efectos de imagen

A partir Windows 10 de aniversario, Direct2D incluye los efectos AlphaMask, CrossFade, Opacity y Tint. Esta funcionalidad estaba disponible previamente en configuraciones específicas de los efectos Compuesto, ArithmeticComposite y ColorMatrix, pero los nuevos efectos integrados facilitan la realización de estas operaciones comunes.

## <a name="whats-new-for-windows-10"></a>Novedades de Windows 10

Las siguientes características y API se agregaron o actualizaron para Windows 10.

### <a name="sprite-batches"></a>Lotes de sprite

A partir Windows 10, Direct2D proporciona compatibilidad para crear y representar lotes de sprites. En comparación con el método [**DrawImage**](id2d1devicecontext-drawimage-overload.md) de uso general, los lotes de sprite incurren en una sobrecarga considerablemente menor de CPU por imagen. Esto los hace ideales para escenarios que implican cientos o miles de imágenes simultáneas, como sprites de juegos o sistemas de partículas. Para obtener más información, vea los temas siguientes:

-   [**Método ID2D1DeviceContext3::CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**Métodos ID2D1DeviceContext3::D rawSpriteBatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   [**Interfaz ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Mallas de degradado

A partir Windows 10, Direct2D proporciona una nueva primitiva para mallas de degradado. Los ilustradores profesionales suelen usar mallas de degradado en software de diseño gráfico y permiten a los dibujantes representar formas complejas (incluso fotorealistas) con todas las ventajas de memoria y escalabilidad de los vectores. Para obtener más información, vea los temas siguientes:

-   [Muestra de malla de degradado Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ Estructura DE \_ REVISIÓN \_ DE MALLA DE**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) DEGRADADO
-   [**Método ID2D1DeviceContext2::D rawGradientMesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>API de carga de imágenes mejoradas

A partir Windows 10, Direct2D ofrece una nueva API para cargar imágenes, ID2D1ImageSource. El origen de la imagen mejora las API de carga de imágenes existentes, como CreateBitmapFromWicBitmap, el efecto Bitmap Source y el efecto YCbCr. El origen de imágenes de Direct2D combina las funcionalidades de estas API con compatibilidad con imágenes arbitrariamente grandes, integración sencilla con impresión y efectos, y numerosas optimizaciones, como YCbCr JPEG y JPEG indexado. Para más información, consulte los temas siguientes:

-   [Ejemplo del SDK de ajuste de fotos de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICPlantegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Compatibilidad mejorada con la representación de lápiz

A partir Windows 10, Direct2D proporciona una nueva primitiva para representar trazos de entrada de lápiz. Los trazos de entrada de lápiz de Direct2D se definen mediante curvas Bézier, admiten diferentes formas y transformaciones de nib y pueden tener un grosor fijo o variable. La compatibilidad integrada de Direct2D con trazos de entrada de lápiz permite que las aplicaciones representen fácilmente una entrada de lápiz más rápida y más cómoda que los enfoques anteriores, que normalmente requerían aplicaciones para administrar la entrada de lápiz, como una serie de elipses y cuadríteros. Para obtener más información, vea los temas siguientes:

-   [**Interfaz ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**Método ID2D1DeviceContext2::D rawInk**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interfaz ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Vinculación del sombreador de efectos

Los efectos de Direct2D se implementan mediante sombreadores de cálculo, vértices o píxeles HLSL. A partir Windows 10, Direct2D ahora analiza automáticamente los gráficos de efectos para obtener oportunidades de combinar y ejecutar sombreadores individuales. Esto puede proporcionar un aumento significativo en el rendimiento del efecto. Los consumidores de efectos integrados no necesitan hacer nada para beneficiarse de la vinculación del sombreador de efectos, pero los desarrolladores que crean sus propios efectos personalizados deben seguir los procedimientos recomendados actualizados para aprovechar la vinculación del sombreador de efectos. Para obtener más información, vea los temas siguientes:

-   [Vinculación del sombreador de efectos](effect-shader-linking.md)
-   [Asistentes de HLSL de Direct2D](hlsl-helpers.md)
-   [Ejemplo del SDK de efectos personalizados de Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

La vinculación del sombreador de efectos está diseñada para no afectar a la salida visual de los efectos. Sin embargo, esto no siempre es posible debido a un comportamiento específico en torno a la precisión de efecto y el recorte numérico. Para obtener más información sobre cómo controlar estos comportamientos, vea:

-   [Controlar la precisión y el recorte numérico en gráficos de efecto](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Nuevos efectos integrados

A partir Windows 10, Direct2D incluye un amplio conjunto de nuevos efectos integrados que abordan las principales solicitudes de los desarrolladores y habilitan nuevos tipos de escenarios visuales. Los nuevos efectos son:

### <a name="color"></a>Color:

-   [Efecto RGB a Hue](rgb-to-hue-effect.md)
-   [Efecto de matiz a RGB](hue-to-rgb-effect.md)
-   [Efecto de tabla de búsqueda 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Foto:

-   [Efecto de contraste](contrast-effect.md)
-   [Efecto de exposición](exposure-effect.md)
-   [Efecto de escala de grises](grayscale-effect.md)
-   [Efecto de resaltado y sombras](highlights-and-shadows-effect.md)
-   [Invert effect](invert-effect.md)
-   [Efecto Sepia](sepia-effect.md)
-   [Efecto de ajuste](sharpen-effect.md)
-   [Efecto de enderez](straighten-effect.md)
-   [Temperatura y efecto de tono](temperature-and-tint-effect.md)
-   [Efecto de la viñeta](vignette-effect.md)

### <a name="filter"></a>Filtro:

-   [Efecto de detección perimetral](edge-detection-effect.md)

### <a name="stylize"></a>Estilizar:

-   [Efecto de relieve](emboss-effect.md)
-   [Efecto de pósterización](posterize-effect.md)

### <a name="transparency"></a>Transparencia:

-   [Efecto de clave de sonido](chromakey-effect.md)

Los efectos de endulz, saturación, contraste, resaltado y sombras, y los efectos de temperatura y tono se muestran en el ejemplo del SDK de ajuste de fotos de [Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).

## <a name="whats-new-for-windows-81"></a>Novedades de Windows 8.1

Las siguientes características y API se agregaron o actualizaron para Windows 8.1.

A partir Windows 8.1, Direct2D se basa en Direct3D 11.2.

### <a name="geometry-realizations"></a>Realizaciones de geometría

A partir Windows 8.1, Direct2D ofrece realizaciones de geometría. Las realizaciones de geometría permiten a las aplicaciones mejorar el rendimiento de la representación de geometría en determinadas situaciones, sin algunas de las desventajas de la rasterización de la geometría a un mapa de bits. Para obtener más información, vea los temas siguientes:

-   [**Interfaz ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**Método ID2D1DeviceContext1::D rawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Compatibilidad con imágenes JPEG YCbCr

A partir Windows 8.1, Direct2D proporciona compatibilidad para representar datos de imagen en el formato JPEG Y'CbCr. Las aplicaciones pueden representar contenido JPEG en su representación nativa de Y'CbCr en lugar de descomprimir en BGRA. Esto puede reducir significativamente el consumo de memoria de gráficos y el tiempo de creación de recursos. Para obtener más información, vea los temas siguientes:

-   Efecto [YCbCr de](ycbcr-effect.md) Direct2D
-   [**IWICPlanarBitmapSourceTransform (interfaz)**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Compatibilidad con formatos comprimidos en bloques (archivos DDS)

A partir de Windows 8.1, Direct2D proporciona compatibilidad con mapas de bits que contienen datos de píxeles UNORM DE DXGI \_ FORMAT \_ \_ BC1, DXGI FORMAT \_ BC2 UNORM y \_ \_ DXGI FORMAT \_ \_ BC3 \_ UNORM. Las aplicaciones pueden reemplazar sus recursos de imagen por imágenes DDS comprimidas en bloque. Esto puede reducir significativamente el consumo de memoria de gráficos y el tiempo de creación de recursos. Para obtener más información, vea los temas siguientes:

-   [**Método ID2D1DeviceContext::CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   [**IWICDdsFrameDecode (interfaz)**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Prioridad de representación

A partir Windows 8.1, Direct2D proporciona compatibilidad con la prioridad de representación por dispositivo. Esta nueva característica permite a las aplicaciones cambiar un dispositivo entre la prioridad de representación normal (la predeterminada) y la prioridad de representación baja (en la que el dispositivo no bloqueará otras tareas de representación en el sistema). Se recomienda que las aplicaciones usen una prioridad de representación baja para las tareas que no son críticas para la capacidad de respuesta del usuario, como la representación previa del contenido, la representación mientras se minimiza y otras operaciones que normalmente se realizan en segundo plano. Para obtener más información, vea los temas siguientes:

-   [**Método ID2D1Device1::SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2D1 \_ ENUMERACIÓN \_ DE PRIORIDAD DE REPRESENTACIÓN**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Novedades de Windows 8

Las siguientes características y API se agregaron o actualizaron para Windows 8.

Las nuevas interfaces de Direct2D se admiten en Windows 7 con la actualización de plataforma [Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) instalada.

La semántica de Direct2D para dispositivos y contextos de dispositivo se ha actualizado para que se parezca más a la semántica usada por Direct3D y para proporcionar una operación concisa en las aplicaciones de Windows Store. Consulte [Dispositivos y contextos de dispositivo para](devices-and-device-contexts.md) obtener más información.

API relacionadas seleccionadas:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

La API de lista de comandos permite compartir la ruta de representación para en la representación e impresión en pantalla. También permite usar primitivas para crear un pincel de imagen para rellenar primitivas.

API relacionadas seleccionadas:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Efectos de Direct2D](effects-overview.md) es un conjunto de API, nueva en Windows 8, para aplicar efectos de alta calidad a las imágenes. También incluye API que le permiten crear sus propios efectos personalizados.

API relacionadas seleccionadas:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

A partir Windows 8, Direct2D incluye API adicionales para compilar aplicaciones multiproceso. Consulte [Aplicaciones Direct2D multiproceso](multi-threaded-direct2d-apps.md) para obtener más información.

API relacionadas seleccionadas:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**D2D1 \_ FACTORY \_ TYPE \_ MULTI \_ THREADED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 
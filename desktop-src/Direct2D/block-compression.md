---
title: Compresión de bloques
description: Describe cómo funciona la compresión de bloque y cómo se usa en WIC y Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: aeb6ba9427a04f7a251a1d59062be508e4249b41
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104547238"
---
# <a name="block-compression"></a>Compresión de bloques

A partir de Windows 8.1, Direct2D admite varios formatos de píxel comprimidos en bloques. Además, Windows 8.1 contiene un nuevo códec DDS de Windows Imaging Component (WIC) para habilitar la carga y el almacenamiento de imágenes comprimidas en bloques en el formato de archivo DDS. La compresión de bloque es una técnica para reducir la cantidad de memoria de gráficos consumida por el contenido del mapa de bits. Mediante el uso de la compresión de bloque, la aplicación puede reducir el consumo de memoria y los tiempos de carga de las mismas imágenes de resolución. O bien, la aplicación puede usar imágenes de más o más resolución mientras se sigue consumiendo la misma superficie de memoria de la GPU.

Las aplicaciones de Direct3D han utilizado la compresión de bloque durante mucho tiempo y, con Windows 8.1, también está disponible para los desarrolladores de aplicaciones estándar y de Direct2D.

En este tema se describe cómo funciona la compresión por bloques y cómo se usa en WIC y Direct2D.

## <a name="about-block-compression"></a>Acerca de la compresión de bloque

La [compresión por bloques](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) hace referencia a una clase de técnicas de compresión para reducir los tamaños de textura. Direct3D 11 admite hasta 7 formatos de BC diferentes en función del nivel de características. En Windows 8.1 Direct2D incluye compatibilidad con los formatos BC1, BC2 y BC3 que están disponibles en todos los niveles de características.

### <a name="how-block-compression-works"></a>Cómo funciona la compresión por bloques

Los formatos comprimidos de bloque usan la misma técnica básica para reducir el espacio consumido por los datos de color. En esta sección se resume el algoritmo más sencillo, BC1. Para obtener una explicación más detallada, consulte [bloquear la compresión](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

En primer lugar, la imagen se divide en bloques de 4 por 4 píxeles. Cada bloque se comprime por separado.

> [!Note]  
> Esto significa que el ancho y el alto de una imagen deben ser un múltiplo de 4 píxeles para que se compriman en bloque.

 

En esta imagen de ejemplo se muestra un bloque de píxeles de 4x4 dentro de una imagen.

![una imagen de ejemplo muestra un bloque de píxeles de 4x4 dentro de una imagen.](images/dds1.png)

Después, dentro de un bloque de 4 por 4, se seleccionan dos colores de "referencia" y se codifican como valores de 2 16 bits (5 bits rojo, 6 bits verde, 5 bits azul). La elección de estos colores afecta significativamente a la calidad de la imagen y no es trivial. Dos colores intermedios se calculan mediante la interpolación lineal entre los dos colores de referencia del espacio de colores RGB. Esto produce un total de 4 colores posibles diferentes; a cada color se le asigna un valor de índice de dos bits. Sin embargo, tenga en cuenta que solo es necesario almacenar los dos colores del punto de conexión cuando la interpolación es fija.

En esta ilustración, los colores 0 y 3 se seleccionan como colores de "referencia" para el bloque, mientras que los colores 1 y 2 se calculan mediante la interpolación lineal.

![Diagrama que muestra el cálculo de 4 valores de color para representar el bloque.](images/dds2.png)

Por último, cada píxel del bloque se asigna a uno de los cuatro colores calculados anteriormente y cada píxel se codifica mediante el valor de índice de dos bits.

La cantidad total de datos que se usa para representar estos 16 píxeles es:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Esto da como resultado una densidad media de 4 bits por píxel. Para la comparación, el formato de B8G8R8A8 de formato de DXGI común \_ \_ UNORM de \_ píxeles consume 32 bits por píxel.

En este diagrama se muestra que cada píxel se codifica como un índice de 2 bits. El bloque completo se codifica en 64 bits.

![calcular 4 valores de color para representar el bloque.](images/dds3.png)

Hay variaciones que admiten datos alfa y números variables de canales de color. BC6H y BC7 usan algoritmos significativamente diferentes para admitir contenido de intervalo dinámico alto (HDR) y aumentar la calidad de la imagen, respectivamente.

### <a name="directdraw-surface-dds-file-format"></a>Formato de archivo de DirectDraw Surface (DDS)

Los datos comprimidos en bloques normalmente se almacenan en archivos de [DirectDraw Surface (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) . Es posible que esté familiarizado con los archivos DDS si es un desarrollador de Direct3D. Tenga en cuenta que Direct2D solo admite ciertas características DDS; para obtener más información, consulte [requisitos de DDS](#dds-requirements).

### <a name="advantages-of-block-compression"></a>Ventajas de la compresión de bloque

Los formatos comprimidos en bloques difieren de los formatos de compresión de imagen de la industria, como JPEG, ya que son compatibles de forma nativa con las GPU modernas. Esto significa que puede cargar directamente una imagen comprimida en bloque en la GPU sin descodificación o descompresión. Los formatos BC consumen de 4 a 8 bits por píxel en promedio; Cuando se comparan con un mapa de bits de BGRA de bits sin 32 comprimir típico por píxel, esto da como resultado un ahorro de memoria del 75% al 87,5%. Además, dado que no hay ningún paso de descodificación, el tiempo para cargar una imagen de BC se reduce significativamente en comparación con formatos como JPEG.

### <a name="when-to-use-block-compression"></a>Cuándo usar la compresión de bloque

Considere la posibilidad de usar imágenes comprimidas en bloque en la aplicación en lugar de otros formatos como JPEG si desea reducir el consumo de memoria de los mapas de bits o desea reducir los tiempos de descodificación y carga.

Sin embargo, la compresión de bloque no es adecuada para todos los casos y requiere algunos inconvenientes. En primer lugar, se pierden los algoritmos de compresión de bloque. La compresión de bloque funciona bien con el contenido fotográfico natural, pero puede introducir artefactos visuales no deseados en imágenes con límites nítidos y de contraste alto, como capturas de pantallas generadas por el equipo. Debe asegurarse de que los recursos de la imagen comprimida en bloque tienen una calidad de imagen aceptable antes de usarlos.

En segundo lugar, bloquear los archivos DDS comprimidos suele consumir más espacio en disco que las imágenes JPEG comparables. Esto, a su vez, aumentará el tamaño de paquete de la aplicación y los requisitos de ancho de banda de red.

## <a name="using-block-compression"></a>Usar la compresión de bloque

En esta sección se explica cómo generar y usar recursos comprimidos en bloques en una aplicación de Direct2D.

### <a name="overview"></a>Información general

Los archivos DDS comprimidos en bloques son un formato optimizado en tiempo de ejecución, lo que significa que están optimizados específicamente para un buen rendimiento en el tiempo de ejecución de la aplicación. Le recomendamos que siga usando la canalización de creación y edición de recursos existente y que solo convierta en un formato comprimido de bloque al importarlos en el proyecto de aplicación, o en el momento de la compilación.

### <a name="dds-requirements"></a>Requisitos de DDS

El formato de archivo DDS se diseñó para admitir una amplia gama de características usadas en Direct3D. Direct2D solo usa un subconjunto de estas características. Por lo tanto, al crear imágenes DDS para su uso con Direct2D, debe tener en cuenta las siguientes restricciones:

-   Solo se permiten los siguientes valores de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :
    -   Formato de DXGI \_ \_ BC1 \_ UNORM
    -   Formato de DXGI \_ \_ BC2 \_ UNORM
    -   Formato de DXGI \_ \_ BC3 \_ UNORM
-   Se deben usar los datos alfa premultiplicados. Esto incluye los archivos DDS heredados que usan formatos que definen explícitamente alfa premultiplicado (DXT1, DXT2, DXT4), así como archivos DDS que usan el encabezado de DDS \_ \_ contenido DX10 estructura con los \_ \_ \_ \_ \_ \_ valores PREmultiplicados de modo alfa opaco y DDS de modo alfa.
-   Las dimensiones X e y deben ser múltiplos de 4 píxeles.
-   No se admiten las texturas de volumen, cubemaps, MIP ni matrices de textura. Solo debe usar imágenes de origen de un solo fotograma.

### <a name="generating-block-compressed-assets"></a>Generación de recursos comprimidos en bloques

Hay una variedad de herramientas de creación de DDS disponibles para crear o convertir archivos DDS comprimidos en bloques. Nota no todas las herramientas admiten los requisitos para usar archivos DDS con Direct2D, tal como se detallan en la sección anterior.

A partir de Visual Studio 2013, puede hacer que Visual Studio convierta los recursos visuales existentes, como JPEG y PNG, al formato comprimido de bloque DDS correcto como parte automática del proceso de compilación. Esto se logra mediante el paso de compilación personalizada de la tarea de contenido de la imagen.

Para obtener información sobre cómo configurar esto para el proyecto, vea: [Cómo: exportar una textura para usarla con aplicaciones de Direct2D o javascipt](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).

### <a name="direct2d-apis"></a>API de Direct2D

Direct2D se actualiza en Windows 8.1 para admitir los siguientes formatos de píxel:

-   Formato de DXGI \_ \_ BC1 \_ UNORM
-   Formato de DXGI \_ \_ BC2 \_ UNORM
-   Formato de DXGI \_ \_ BC3 \_ UNORM

En el caso de los formatos anteriores, debe utilizar alfa premultiplicado. Además, estos formatos solo son válidos para su uso como origen, no como destino. Por ejemplo, esto significa que puede crear un mapa de bits de Direct2D mediante BC1, pero no un contexto de dispositivo.

Los métodos siguientes se actualizan en Windows 8.1 para admitir formatos de BC:

-   [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget::CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Tenga en cuenta que [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) toma [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) como una interfaz; sin embargo, en Windows 8.1 WIC no admite la obtención de datos comprimidos en bloques de **IWICBitmapSource** y no hay ningún formato de píxel de WIC correspondiente al formato de DXGI \_ \_ BC1 \_ UNORM, etc. En su lugar, **CreateBitmapFromWicBitmap** determina si **IWICBitmapSource** es un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) de DDS válido y carga directamente los datos comprimidos del bloque. Puede especificar explícitamente el formato de píxel en el [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct o permitir que Direct2D determine automáticamente el formato correcto.

### <a name="windows-imaging-component-apis"></a>API de componentes de Windows Imaging

El componente de creación de imágenes de Windows (WIC) agrega un nuevo códec DDS en Windows 8.1. Además, agrega nuevas interfaces que admiten el acceso a datos específicos de DDS, incluidos los datos de píxeles comprimidos en bloques:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Bloquear formatos de píxeles WIC comprimidos

No hay nuevos formatos de píxeles comprimidos de bloque WIC en Windows 8.1. En su lugar, si obtiene un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) del descodificador de DDS y llama a [**copyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels), recibirá píxeles estándar sin comprimir, como WICPixelFormat32bppPBGRA. Puede usar [**IWICDdsFrameDecode:: CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) para obtener los datos comprimidos de bloques sin formato en forma de búfer de memoria de un archivo DDS.

### <a name="multi-frame-dds-access"></a>Acceso a DDS de varios marcos

El formato de archivo DDS permite almacenar varias imágenes relacionadas en un único archivo. Por ejemplo, un archivo DDS puede contener un mapa, una textura de volumen o una matriz de textura, y todos ellos pueden ser mipmapped. En Direct3D, estas varias imágenes se exponen como Subrecursos. En WIC, se exponen varias imágenes como marcos ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) y [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

WIC solo admite la noción de una matriz de fotogramas unidimensional, mientras que DDS admite tres dimensiones independientes (aunque solo se pueden usar dos en un archivo). WIC proporciona métodos útiles para ayudar con la asignación entre un subrecurso DDS y un marco WIC. Para la descodificación, [**IWICDdsDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) le permite especificar el índice de matriz, el nivel de MIP y el índice de segmento del subrecurso, y devuelve el marco WIC correcto.

Para la codificación, [**IWICDdsEncoder:: CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) calcula el índice de matriz resultante, el nivel de MIP y el índice de segmento cuando se crea un nuevo marco. Debe haber llamado primero a [**IWICDdsEncoder:: SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) para definir los parámetros de archivo específicos de DDS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo: Exportar una textura para usarla con aplicaciones de Direct2D o Javascript](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Referencia de DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compresión de bloque](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 
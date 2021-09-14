---
title: Compresión de bloques
description: Describe cómo funciona la compresión de bloques y cómo usarla en WIC y Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: aeb6ba9427a04f7a251a1d59062be508e4249b41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164233"
---
# <a name="block-compression"></a>Compresión de bloques

A partir Windows 8.1, Direct2D admite varios formatos de píxel comprimidos en bloque. Además, Windows 8.1 un nuevo códec DDS del componente de creación de imágenes de Windows (WIC) para habilitar la carga y el almacenamiento de imágenes comprimidas en bloque en el formato de archivo DDS. La compresión de bloques es una técnica para reducir la cantidad de memoria de gráficos que consume el contenido del mapa de bits. Mediante la compresión de bloques, la aplicación puede reducir el consumo de memoria y los tiempos de carga para las mismas imágenes de resolución. O bien, la aplicación puede usar más o más imágenes de resolución mientras sigue consumiendo la misma superficie de memoria de GPU.

Las aplicaciones de Direct3D han usado la compresión de bloques durante mucho tiempo y con Windows 8.1 está disponible también para los desarrolladores de aplicaciones estándar y Direct2D.

En este tema se describe cómo funciona la compresión de bloques y cómo usarla en WIC y Direct2D.

## <a name="about-block-compression"></a>Acerca de la compresión de bloques

[La compresión de](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) bloques (BC) hace referencia a una clase de técnicas de compresión para reducir los tamaños de textura. Direct3D 11 admite hasta 7 formatos bc diferentes en función del nivel de característica. En Windows 8.1 Direct2D presenta compatibilidad con los formatos BC1, BC2 y BC3 que están disponibles en todos los niveles de características.

### <a name="how-block-compression-works"></a>Funcionamiento de la compresión de bloques

Todos los formatos comprimidos en bloque usan la misma técnica básica para reducir el espacio consumido por los datos de color. En esta sección se resume el algoritmo más sencillo, BC1. Para obtener una explicación más detallada, vea [Compresión de bloques](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

En primer lugar, la imagen se divide en bloques de 4 por 4 píxeles. Cada bloque se comprime por separado.

> [!Note]  
> Esto significa que el ancho y el alto de una imagen deben ser un múltiplo de 4 píxeles para que se comprima en bloque.

 

Esta imagen de ejemplo muestra un bloque de 4 x 4 píxeles dentro de una imagen.

![una imagen de ejemplo muestra un bloque de 4 x 4 píxeles dentro de una imagen.](images/dds1.png)

A continuación, dentro de un bloque de 4 por 4, se seleccionan dos colores de "referencia" y se codifican como dos valores de 16 bits (5 bits rojos, 6 bits verdes y 5 bits azules). La elección de estos colores afecta significativamente a la calidad de la imagen y no es interesante. Dos colores intermedios se calculan mediante la interpolación lineal entre los dos colores de referencia en el espacio de colores RGB. Esto genera un total de 4 colores posibles diferentes; A cada color se le asigna un valor de índice de dos bits. Sin embargo, tenga en cuenta que solo se deben almacenar los dos colores del punto de conexión a medida que se corrigió la interpolación.

En esta ilustración, los colores 0 y 3 se seleccionan como colores de "referencia" para el bloque, mientras que los colores 1 y 2 se calculan mediante interpolación lineal.

![Diagrama que muestra el cálculo de 4 valores de color para representar el bloque.](images/dds2.png)

Por último, cada píxel del bloque se asigna a uno de los cuatro colores calculados previamente y cada píxel se codifica con el valor de índice de dos bits.

La cantidad total de datos que se usan para representar estos 16 píxeles es:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Esto da como resultado una densidad media de 4 bits por píxel. En comparación, el formato de píxel DXGI \_ FORMAT \_ B8G8R8A8 UNORM común consume \_ 32 bits por píxel.

En este diagrama se muestra que cada píxel se codifica como un índice de 2 bits. Todo el bloque se codifica en 64 bits.

![calcular 4 valores de color para representar el bloque.](images/dds3.png)

Hay variaciones para admitir datos alfa y diferentes números de canales de color. BC6H y BC7 usan algoritmos significativamente diferentes para admitir contenido de alto rango dinámico (HDR) y aumentar la calidad de la imagen, respectivamente.

### <a name="directdraw-surface-dds-file-format"></a>Formato de archivo de DirectDraw Surface (DDS)

Los datos comprimidos en bloques normalmente se almacenan [en archivos de DirectDraw Surface (DDS).](/windows/desktop/direct3ddds/dx-graphics-dds-reference) Es posible que esté familiarizado con los archivos DDS si es desarrollador de Direct3D. Tenga en cuenta que Direct2D solo admite determinadas características de DDS; Para obtener más información, [vea Requisitos de DDS.](#dds-requirements)

### <a name="advantages-of-block-compression"></a>Ventajas de la compresión de bloques

Los formatos comprimidos en bloques difieren de los formatos de compresión de imágenes comunes del sector, como JPEG, en que los formatos BC son compatibles de forma nativa con las GPU modernas. Esto significa que puede cargar directamente una imagen comprimida por bloques en la GPU sin necesidad de descomprimir ni descomprimir. Los formatos BC consumen de 4 a 8 bits por píxel en promedio. Cuando se compara con un mapa de bits de BGRA típico de 32 bits por píxel sin comprimir, esto da como resultado un ahorro de memoria del 75 % al 87,5 %. Además, dado que no hay ningún paso de descodificación, el tiempo para cargar una imagen bc se reduce significativamente en comparación con formatos como JPEG.

### <a name="when-to-use-block-compression"></a>Cuándo usar la compresión de bloques

Debe considerar el uso de imágenes comprimidas en bloque en la aplicación en lugar de otros formatos como JPEG si desea reducir el consumo de memoria de los mapas de bits o quiere reducir los tiempos de descodificación y carga.

Sin embargo, la compresión de bloques no es adecuada para todos los casos y requiere algunos contras. En primer lugar, los algoritmos de compresión de bloques pierden. La compresión de bloques funciona bien con contenido de fotografía natural, pero puede introducir artefactos visuales no deseados en imágenes con límites de contraste alto y nítido, como capturas de pantalla generadas por el equipo. Debe asegurarse de que los recursos de imagen comprimidos en bloque tienen una calidad de imagen aceptable antes de usarlos.

En segundo lugar, los archivos DDS comprimidos en bloque suelen consumir más espacio en disco que las imágenes JPEG comparables. Esto a su vez aumentará el tamaño del paquete de la aplicación y los requisitos de ancho de banda de red.

## <a name="using-block-compression"></a>Uso de la compresión de bloques

En esta sección se explica cómo generar y usar recursos comprimidos en bloques en una aplicación de Direct2D.

### <a name="overview"></a>Información general

Los archivos DDS comprimidos en bloques son un formato optimizado para tiempo de ejecución, lo que significa que están optimizados específicamente para un buen rendimiento en tiempo de ejecución de la aplicación. Se recomienda seguir usando la canalización de creación y edición de recursos existente y convertirla solo a un formato comprimido en bloque al importarlos en el proyecto de aplicación o en tiempo de compilación.

### <a name="dds-requirements"></a>Requisitos de DDS

El formato de archivo DDS se diseñó para admitir una amplia gama de características usadas en Direct3D. Direct2D solo usa un subconjunto de estas características. Por lo tanto, al crear imágenes de DDS para su uso con Direct2D, debe tener en cuenta las restricciones siguientes:

-   Solo se permiten [**los siguientes valores DE FORMATO \_ DXGI:**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
    -   DXGI \_ FORMAT \_ BC1 \_ UNORM
    -   DXGI \_ FORMAT \_ BC2 \_ UNORM
    -   DXGI \_ FORMAT \_ BC3 \_ UNORM
-   Se deben usar datos alfa premultiplicados. Esto incluye archivos DDS heredados que usan formatos que definen explícitamente alfa premultiplicado (DXT1, DXT2, DXT4), así como archivos DDS que usan la estructura DDS HEADER DX10 con los valores \_ \_ \_ \_ \_ \_ \_ \_ PREMULTIPLIED del modo ALFA de DDS.
-   Las dimensiones X e Y deben ser múltiplo de 4 píxeles.
-   No se permiten texturas de volumen, mapas de cubos, mapas mip ni matrices de texturas. Solo debe usar imágenes de origen de fotograma único.

### <a name="generating-block-compressed-assets"></a>Generación de recursos comprimidos en bloques

Hay una variedad de herramientas de creación de DDS disponibles para crear o convertir archivos DDS comprimidos en bloques. Tenga en cuenta que no todas las herramientas admiten los requisitos para usar archivos DDS con Direct2D, como se detalla en la sección anterior.

A partir Visual Studio 2013, puede hacer que Visual Studio recursos visuales existentes, como JPEG y PNG, al formato comprimido del bloque DDS correcto como parte automática del proceso de compilación. Esto se logra mediante el paso de compilación personalizada tarea de contenido de imagen.

Para obtener información sobre cómo configurar esto para el proyecto, vea: Cómo: Exportar una textura para su uso con [Aplicaciones Direct2D o Javascipt.](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))

### <a name="direct2d-apis"></a>API de Direct2D

Direct2D se actualiza en Windows 8.1 para admitir los siguientes formatos de píxel:

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   DXGI \_ FORMAT \_ BC3 \_ UNORM

Para los formatos anteriores, debe usar alfa premultiplicado. Además, estos formatos solo son válidos para su uso como origen, no como destino. Por ejemplo, esto significa que puede crear un mapa de bits de Direct2D mediante BC1, pero no un contexto de dispositivo.

Los métodos siguientes se actualizan en Windows 8.1 para admitir formatos BC:

-   [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget::CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Tenga en [**cuenta que CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) toma [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) como interfaz; sin embargo Windows 8.1 WIC no admite la obtención de datos comprimidos en bloque de **IWICBitmapSource** y no hay ningún formato de píxel WIC correspondiente a DXGI \_ FORMAT \_ BC1 \_ UNORM, etc. En su lugar, **CreateBitmapFromWicBitmap** determina si **IWICBitmapSource** es un DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) válido y carga directamente los datos comprimidos en bloque. Puede especificar explícitamente el formato de píxel en la estructura [**D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) o permitir que Direct2D determine automáticamente el formato correcto.

### <a name="windows-imaging-component-apis"></a>Windows API de componentes de creación de imágenes

El Windows Imaging Component (WIC) agrega un nuevo códec DDS en Windows 8.1. Además, agrega nuevas interfaces que admiten el acceso a datos específicos de DDS, incluidos los datos de píxeles comprimidos en bloque:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Bloquear formatos de píxeles WIC comprimidos

No hay nuevos formatos de píxeles comprimidos de bloque WIC en Windows 8.1. En su lugar, si obtiene un [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) del descodificador DDS y llama a [**CopyPixels,**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)recibirá píxeles estándar sin comprimir, como WICPixelFormat32bppPBGRA. Puede usar [**IWICDdsFrameDecode::CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) para obtener los datos comprimidos de bloque sin formato en forma de búfer de memoria de un archivo DDS.

### <a name="multi-frame-dds-access"></a>Acceso DDS de varios fotogramas

El formato de archivo DDS permite almacenar varias imágenes relacionadas en un único archivo. Por ejemplo, un archivo DDS puede contener un mapa de cubos, una textura de volumen o una matriz de texturas, todos los cuales se pueden aplicar a mipmapped. En Direct3D, estas varias imágenes se exponen como subrecursos. En WIC, varias imágenes se exponen como fotogramas [**(IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

WIC solo admite la noción de una matriz unidimensional de fotogramas, mientras que DDS admite tres dimensiones independientes (aunque solo se pueden usar dos en cualquier archivo). WIC proporciona métodos prácticos para ayudar con la asignación entre un subrecurso de DDS y un marco WIC. Para la descodificación, [**IWICDdsDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) permite especificar el índice de matriz, el nivel de mip y el índice de segmento del subcurso, y devuelve el marco WIC correcto.

Para la codificación, [**IWICDdsEncoder::CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) calcula el índice de matriz, el nivel de mip y el índice de segmento resultantes al crear un marco. Primero debe haber llamado a [**IWICDdsEncoder::SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) para definir los parámetros de archivo específicos de DDS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo: Exportar una textura para usarla con aplicaciones de Direct2D o Javascript](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Referencia de DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compresión de bloques](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 
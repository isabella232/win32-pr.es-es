---
description: A partir Windows 8.1, el códec JPEG Windows Imaging Component (WIC) admite la lectura y escritura de datos de imagen en su forma nativa de YCbCr.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: JPEG YCbCr Support
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f8548a458f70265d248e1d686ad3bc300d7cfee2bc1e0ab2262ee652f0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086798"
---
# <a name="jpeg-ycbcr-support"></a>JPEG YCbCr Support

A partir Windows 8.1, el códec JPEG [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) admite la lectura y escritura de datos de imagen en su formato nativo de YC<sub>b</sub>C<sub>r.</sub> La compatibilidad con WIC YC<sub>b</sub>C<sub>r</sub> se puede usar junto con [Direct2D](../direct2d/direct2d-portal.md) para representar los datos de píxeles de YC<sub>b</sub>C<sub>r</sub> con un efecto de imagen. Además, el códec WIC JPEG puede consumir datos de píxeles YC<sub>b</sub>C<sub>r</sub> generados por determinados controladores de cámara a través de Media Foundation.

Los datos<sub>de píxeles</sub>de YC b C<sub>r</sub> consumen significativamente menos memoria que los formatos de píxeles BGRA estándar. Además, el acceso a los datos de YC<sub>b</sub>C<sub>r</sub> permite descargar algunas fases de la canalización de descodificación/codificación JPEG en Direct2D, que está acelerada por GPU. Mediante el uso de YC<sub>b</sub>C<sub>r,</sub>la aplicación puede reducir el consumo de memoria JPEG y los tiempos de carga de las mismas imágenes de tamaño y calidad. O bien, la aplicación puede usar más imágenes JPEG de mayor resolución sin sufrir penalizaciones de rendimiento.

En este tema se describe cómo funcionan los datos de YC<sub>b</sub>C<sub>r</sub> y cómo usarlos en WIC y Direct2D.

-   [Acerca de JPEG YC<sub>b</sub>C<sub>r</sub> Data](#about-jpeg-ycbcr-data)
    -   [YC<sub>b</sub>C<sub>r</sub> Color Model](#ycbcr-color-model)
    -   [Diseños de memoria plana frente a intercalados](#planar-versus-interleaved-memory-layouts)
    -   [Submuestreo Desamueba](#chroma-subsampling)
    -   [Uso jpeg de YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Uso de JPEG YC<sub>b</sub>C<sub>r</sub> Data](#using-jpeg-ycbcr-data)
    -   [Uso de imágenes YC<sub>b</sub>C<sub>r</sub> JPEG](#using-ycbcr-jpeg-images)
    -   [Windows API de componentes de creación de imágenes](#windows-imaging-component-apis)
    -   [API de Direct2D](#direct2d-apis)
    -   [Determinar si se admite la configuración de YC<sub>b</sub>C<sub>r</sub>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decoding YC<sub>b</sub>C<sub>r</sub> Pixel Data](#decoding-ycbcr-pixel-data)
    -   [Transformación de datos de<sub>píxeles</sub>de YC b C<sub>r</sub>](#transforming-ycbcr-pixel-data)
    -   [Codificación de datos de píxeles de YC<sub>b</sub><sub>C r</sub>](#encoding-ycbcr-pixel-data)
    -   [Decoding YC<sub>b</sub>C<sub>r</sub> pixel data in Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Temas relacionados](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Acerca de JPEG YC<sub>b</sub>C<sub>r</sub> Data

En esta sección se explican algunos conceptos clave necesarios para comprender cómo funciona la compatibilidad con YC<sub>b</sub>C<sub>r</sub> en WIC y sus principales ventajas.

### <a name="ycsubbsubcsubrsub-color-model"></a>YC<sub>b</sub>C<sub>r</sub> Color Model

WIC en Windows 8 y versiones anteriores admite cuatro modelos de [color](-wic-codec-native-pixel-formats.md)diferentes, el más común es RGB/BGR. Este modelo de color define los datos de color mediante componentes rojo, verde y azul; También se puede usar un cuarto componente alfa.

Esta es una imagen descompuesta en sus componentes rojo, verde y azul.

![una imagen descomponeda en sus componentes rojo, verde y azul.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r es</sub> un modelo de color alternativo que define los datos de color mediante un componente de luminosidad (Y) y dos componentes de chrominance (C<sub>b</sub> y C<sub>r</sub>). Se usa normalmente en escenarios de vídeo y creación de imágenes digitales. El término YC<sub>b</sub>C<sub>r se</sub> suele usar indistintamente con YUV, aunque los dos son técnicamente distintos.

Hay varias variaciones de YC<sub>b</sub>C<sub>r</sub> que difieren en el espacio de colores y las definiciones de intervalo dinámico: WIC admite específicamente los datos jpeg JFIF YC<sub>b</sub>C<sub>r.</sub> Para obtener más información, consulte la [especificación JPEG ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

Esta es una imagen descompuesta en sus componentes Y, C<sub>b</sub>y C<sub>r.</sub>

![una imagen descompuesta en sus componentes y, cb y cr.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Diseños de memoria plana frente a intercalados

En esta sección se describen algunas diferencias entre el acceso y el almacenamiento de datos de píxel RGB en la memoria frente a los datos de YC<sub>b</sub>C<sub>r.</sub>

Los datos de píxel RGB se almacenan normalmente mediante un diseño de memoria intercalada. Esto significa que los datos de un único componente de color se intercalan entre píxeles y cada píxel se almacena de forma contigua en la memoria.

Esta es una ilustración que muestra los datos de píxel RGBA almacenados en un diseño de memoria intercalada.

![una ilustración que muestra los datos de píxel rgba almacenados en un diseño de memoria intercalada.](graphics/ycbcr3.png)

Los datos de YC<sub>b</sub>C<sub>r</sub> se almacenan normalmente mediante un diseño de memoria plana. Esto significa que cada componente de color se almacena por separado en su propio plano contiguo, para un total de tres planos. En otra configuración común, los componentes<sub>C b</sub> y C<sub>r</sub> se intercalan y almacenan juntos, mientras que el componente Y permanece en su propio plano, para un total de dos planos.

Esta es una ilustración en la que se muestran los datos de píxeles planas Y y C<sub>b</sub>C<sub>r</sub> intercalados, un diseño común de memoria de YC<sub>b</sub>C<sub>r.</sub>

![una ilustración que muestra los datos planar y y de píxeles cbcr intercalados, un diseño de memoria ycbcr común.](graphics/ycbcr4.png)

Tanto en WIC como en Direct2D, cada plano de color se trata como su propio objeto distinto (ya sea [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) o [**ID2D1Bitmap)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)y, colectivamente, estos planos forman los datos de respaldo de una imagen YC <sub>b</sub>C <sub>r.</sub>

Aunque WIC admite el acceso a los datos de YC<sub>b</sub>C<sub>r</sub> en las configuraciones de plano 2 y 3, Direct2D solo admite el primero (Y<sub>y</sub>C b C<sub>r</sub>). Por lo tanto, al usar WIC y Direct2D juntos, siempre debe usar la configuración de YC<sub>b</sub>C<sub>r de</sub> 2 plano.

### <a name="chroma-subsampling"></a>Submuestreo de Semán

El modelo de color YC<sub>b</sub>C<sub>r</sub> es adecuado para escenarios de creación de imágenes digitales, ya que puede aprovechar ciertos aspectos del sistema visual humano. En concreto, los seres humanos son más sensibles a los cambios en la luminosidad (brillo) de una imagen y menos sensibles a la chrominance (color). Al dividir los datos de color en componentes independientes de luminosidad y de chrominance, podemos comprimir selectivamente solo los componentes de chrominance para lograr un ahorro de espacio con una pérdida mínima de calidad.

Una técnica para hacerlo se denomina submuestreo de tosco. Los planos<sub>C b</sub> y C<sub>r</sub> se submuestrean (en escala vertical) en una o ambas dimensiones horizontales y verticales. Por motivos históricos, a cada modo de submuestreo se hace referencia normalmente mediante una relación J:a:b de tres partes.



| Modo de submuestreo | Escalado vertical horizontal | Escalado vertical | Bits por píxel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Incluye datos Y.

En la tabla anterior, si usa YC<sub>b</sub>C<sub>r</sub> para almacenar datos de imagen sin comprimir, puede lograr un ahorro de memoria de entre el 25 % y el 62,5 % frente a los datos RGBA de 32 bits por píxel, en función del modo de submuestreo que se use.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Uso jpeg de YC<sub>b</sub>C<sub>r</sub>

En un nivel alto, la canalización de descompresión JPEG consta de las siguientes fases:

1.  Realizar descompresión de entropía (por ejemplo, Huffman)
2.  Realización de la desquantización
3.  Realización de una transformación inversa de coseno discreto
4.  Realización de un upsampling en datos de C<sub>b</sub>C<sub>r</sub>
5.  Conversión de datos de YC<sub>b</sub>C<sub>r</sub> a RGBA (si es necesario)

Al hacer que el códec JPEG produzca datos YC<sub>b</sub>C<sub>r,</sub> podemos evitar los dos últimos pasos del proceso de descodificación o aplazarlos a la GPU. Además del ahorro de memoria que se muestra en la sección anterior, esto reduce significativamente el tiempo total necesario para descodificar la imagen. Se aplica el mismo ahorro al codificar datos de YC<sub>b</sub>C<sub>r.</sub>

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Uso de JPEG YC<sub>b</sub>C<sub>r</sub> Data

En esta sección se explica cómo usar WIC y Direct2D para trabajar con datos de YC<sub>b</sub>C<sub>r.</sub>

Para ver las instrucciones de este documento que se usan en la práctica, consulte el ejemplo jpeg [YCbCr optimizations in Direct2D and WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) (Optimizaciones de JPEG YCbCr en Direct2D y WIC), que muestra todos los pasos necesarios para descodificar y representar el contenido de YC<sub>b</sub>C<sub>r</sub> en una aplicación direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Uso de imágenes YC<sub>b</sub>C<sub>r</sub> JPEG

La gran mayoría de las imágenes JPEG se almacenan como YC<sub>b</sub>C<sub>r</sub>. Algunos JPEG contienen datos de escala de grises o JJ y no usan YC<sub>b</sub>C<sub>r</sub>. Esto significa que normalmente, pero no siempre, puede usar directamente contenido JPEG preexistida sin modificaciones.

WIC y Direct2D no admiten todas las configuraciones posibles de YC<sub>b</sub>C<sub>r,</sub> y la compatibilidad con YC<sub>b</sub>C<sub>r</sub> en Direct2D depende del hardware gráfico y el controlador subyacentes. Por este motivo, una canalización de creación de imágenes de uso general debe ser sólida para las imágenes que no usan YC<sub>b</sub>C<sub>r</sub> (incluidos otros formatos de imagen comunes como PNG o BMP) o para los casos en los que la compatibilidad con YC<sub>b</sub>C<sub>r</sub> no está disponible. Se recomienda mantener la canalización de creación de imágenes basada en BGRA existente y habilitar YC<sub>b</sub>C<sub>r como</sub> optimización del rendimiento cuando esté disponible.

### <a name="windows-imaging-component-apis"></a>Windows API de componentes de creación de imágenes

WIC en Windows 8.1 agrega tres nuevas interfaces para proporcionar acceso a los datos JPEG YC<sub>b</sub>C<sub>r.</sub>

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform es**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) análogo a [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)salvo que genera píxeles en una configuración plana, incluidos los datos de YC <sub>b</sub>C <sub>r.</sub> Para obtener esta interfaz, llame a QueryInterface en una implementación de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que admita el acceso plano. Esto incluye la implementación del códec JPEG de [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) así como [**IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICColorTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) proporciona la capacidad de codificar datos de píxeles planas, incluidos los datos de C <sub>r</sub> de YC <sub>b.</sub> Puede obtener esta interfaz llamando a QueryInterface en la implementación del códec JPEG [**de IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) permite a [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) consumir datos de píxeles planas, incluido YC <sub>b</sub>C <sub>r y</sub>convertirlos a un formato de píxel intercalado. No expone la capacidad de convertir datos de píxeles intercalados a un formato plano. Para obtener esta interfaz, llame a QueryInterface en Windows implementación proporcionada de **IWICFormatConverter**.

### <a name="direct2d-apis"></a>API de Direct2D

Direct2D en Windows 8.1 admite datos de píxeles planas de YC<sub>b</sub>C<sub>r</sub> con el nuevo efecto de imagen YC<sub>b</sub>C<sub>r</sub> . Este efecto proporciona la capacidad de representar datos de YC<sub>b</sub>C<sub>r.</sub> El efecto toma como entrada dos interfaces [**ID2D1Bitmap:**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) una que contiene datos Y planas en el formato DXGI FORMAT R8 UNORM y otra que contiene datos CbCr intercalados en el formato \_ \_ \_ DXGI \_ FORMAT \_ R8G8 \_ UNORM. Normalmente, este efecto se usa en lugar de **ID2D1Bitmap** que habría contenido datos de píxeles de BGRA.

El efecto de imagen YC<sub>b</sub>C<sub>r</sub> está pensado para usarse junto con las API de WIC YC<sub>b</sub>C<sub>r</sub> que proporcionan los datos YC<sub>b</sub>C<sub>r.</sub> Esto actúa eficazmente para descargar parte del trabajo de descodificación de la CPU a la GPU, donde se puede procesar mucho más rápido y en paralelo.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Determinar si se admite la<sub>configuración</sub>de C<sub>r</sub> de YC b

Como se indicó anteriormente, la aplicación debe ser sólida para los casos en los que la compatibilidad con YC<sub>b</sub>C<sub>r</sub> no está disponible. En esta sección se de analizan las condiciones que la aplicación debe comprobar. Si se producirá un error en cualquiera de las siguientes comprobaciones, la aplicación debe volver a una canalización estándar basada en BGRA.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>¿Admite el componente WIC el acceso a datos de YC<sub>b</sub>C<sub>r?</sub>

Solo el Windows códec JPEG proporcionado y ciertas transformaciones wic admiten el acceso a datos YC<sub>b</sub>C<sub>r.</sub> Para obtener una lista completa, consulte la Windows Api de componentes de creación [de imágenes.](#windows-imaging-component-apis)

Para obtener una de las interfaces planas de YC<sub>b</sub>C<sub>r,</sub> llame a QueryInterface en la interfaz original. Se producirá un error si el componente no admite el acceso a datos de YC<sub>b</sub>C<sub>r.</sub>

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>¿Se admite la transformación de WIC solicitada para YC<sub>b</sub>C<sub>r</sub>?

Después de obtener un [**IWICPlanarBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)primero debe llamar a [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Este método toma como parámetros de entrada el conjunto completo de transformaciones que desea aplicar a los datos de C<sub>R</sub> de YC<sub>b</sub>plana y devuelve un valor booleano que indica la compatibilidad, así como las dimensiones más cercanas al tamaño solicitado que se pueden devolver. Debe comprobar los tres valores antes de acceder a los datos de píxeles [**con IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Este patrón es similar a cómo [**se usa IWICBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>¿El controlador de gráficos admite las características necesarias para usar YC<sub>b</sub>C<sub>r</sub> con Direct2D?

Esta comprobación solo es necesaria si usa el efecto Direct2D YC<sub>b</sub>C<sub>r</sub> para representar el contenido de YC<sub>b</sub>C<sub>r.</sub> Direct2D almacena datos de YC<sub>b</sub>C<sub>r</sub> mediante los formatos de píxelES UNORM DXGI \_ FORMAT \_ R8 y \_ DXGI FORMAT \_ \_ R8G8 \_ UNORM, que no están disponibles en todos los controladores de gráficos.

Antes de usar el efecto de imagen de C <sub>r</sub> de YC <sub>b,</sub>debe llamar a [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para asegurarse de que el controlador admite ambos formatos.

### <a name="sample-code"></a>Código de ejemplo

A continuación se muestra un ejemplo de código que muestra las comprobaciones recomendadas. Este ejemplo se tomó de las [optimizaciones JPEG YCbCr en el ejemplo de Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decoding YC<sub>b</sub>C<sub>r</sub> Pixel Data

Si desea obtener datos de píxeles de YC <sub>b</sub>C <sub>r,</sub> debe llamar a [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Este método copia los datos de píxeles en una matriz de estructuras [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) rellenas, una para cada plano de datos que desee (por ejemplo, Y y C <sub>b</sub>C <sub>r</sub>). Un **WICBitmapPlane contiene** información sobre los datos de píxeles y apunta al búfer de memoria que recibirá los datos.

Si desea usar los datos de píxeles de YC <sub>b</sub>C <sub>r</sub> con otras API de WIC, debe crear un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)configurado correctamente, llamar a [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) para obtener el búfer de memoria subyacente y asociar el búfer con [**el WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) usado para recibir los datos de píxel de C <sub>r</sub> de YC <sub>b.</sub> A continuación, puede usar [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) con normalidad.

Por último, si desea representar los datos de YC <sub>b</sub>C <sub>r</sub> en Direct2D, debe crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir de cada [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) y usarlos como origen para el efecto de imagen de C <sub>r</sub> de YC <sub>b.</sub> WIC permite solicitar varias configuraciones planas. Al interoperar con Direct2D, debe solicitar dos planos, uno con EL GUID \_ WICPixelFormat8bppY y otro con EL GUID WICPixelFormat16bppCbCr, ya que esta es la configuración esperada por \_ Direct2D.

### <a name="code-sample"></a>Ejemplo de código

A continuación se muestra un ejemplo de código que muestra los pasos para descodificar y representar datos de YC<sub>b</sub>C<sub>r</sub> en Direct2D. Este ejemplo se tomó de las [optimizaciones JPEG YCbCr en el ejemplo de Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformación de datos de<sub>píxeles</sub>de YC b C<sub>r</sub>

La transformación de datos de YC <sub>b</sub>C <sub>r</sub> es casi idéntica a la decodización, ya que ambas implican [**IWICPlanarBitmapSourceTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) La única diferencia es el objeto WIC del que obtuvo la interfaz. El Windows escalado, el rotador de volteo y la transformación de color proporcionados admiten el acceso YC<sub>b</sub>C<sub>r.</sub>

### <a name="chaining-transforms-together"></a>Encadenar transformaciones juntas

WIC admite la noción de encadenar varias transformaciones. Por ejemplo, puede crear la siguiente canalización de WIC:

![diagrama de una canalización wic a partir de un descodificador jpeg.](graphics/ycbcr5.png)

A continuación, puede llamar a QueryInterface en [**IWICColorTransform para**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) obtener [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La transformación de color puede comunicarse con las transformaciones anteriores y puede exponer las funcionalidades de agregado de cada fase de la canalización. WIC garantiza que los datos de YC<sub>b</sub>C<sub>r</sub> se conservan durante todo el proceso. Este encadenamiento solo funciona cuando se usan componentes que admiten el acceso de YC<sub>b</sub>C<sub>r.</sub>

### <a name="jpeg-codec-optimizations"></a>Optimizaciones de códec JPEG

De forma similar a la implementación de descodificación de fotogramas JPEG de [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)la implementación de descodificación de fotogramas JPEG de [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) admite el escalado y la rotación de dominios DCT JPEG nativos. Puede solicitar una potencia de dos escalados o una rotación directamente desde el descodificador JPEG. Esto suele tener como resultado una mayor calidad y rendimiento que el uso de transformaciones discretas.

Además, al encadenar una o varias transformaciones de WIC después del descodificador JPEG, puede aprovechar el escalado y la rotación nativos de JPEG para satisfacer la operación agregada solicitada.

### <a name="format-conversions"></a>Conversiones de formato

Use [**IWICPlanarFormatConverter para**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) convertir datos de píxeles planas de YC <sub>b</sub>C <sub>r</sub> a un formato de píxel intercalado, como GUID \_ WICPixelFormat32bppPBGRA. WIC en Windows 8.1 no proporciona la capacidad de convertir a un formato de píxeles YC<sub>b</sub>C<sub>r</sub> plano.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codificación de datos<sub>de píxeles</sub>de YC b C<sub>r</sub>

Use [**IWICPlanarBitmapFrameEncode para**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) codificar los datos de píxeles de YC <sub>b</sub>C <sub>r</sub> en el codificador JPEG. La codificación de datos de YC <sub>b</sub>C <sub>r</sub> **IWICPlanarBitmapFrameEncode** es similar, pero no idéntica a la codificación de datos intercalados mediante [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). La interfaz plana solo expone la capacidad de escribir datos de imagen de fotograma plano y debe seguir usando la interfaz de codificación de fotogramas para establecer metadatos o una miniatura y confirmar al final de la operación.

En el caso típico, debe seguir estos pasos:

1.  Obtenga [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) de la forma normal. Si desea configurar el submuestreo de croma, establezca la opción [**codificador JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) al crear el fotograma.
2.  Si necesita establecer metadatos o una miniatura, haga esto [**con IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) de la forma habitual.
3.  QueryInterface para [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Establezca los datos de píxeles de C <sub>r</sub> de YC <sub>b</sub>mediante [**IWICPlanarBitmapFrameEncode::WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) o [**IWICPlanarBitmapFrameEncode::WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). A diferencia de sus homólogos [**de IWICBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) se proporciona a estos métodos una matriz de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) o [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) que contienen los planos de píxeles de C <sub>r</sub> de YC <sub>b.</sub>
5.  Cuando haya terminado, llame a [**IWICBitmapFrameEncode::Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decoding YC<sub>b</sub>C<sub>r</sub> pixel data in Windows 10

A partir de Windows 10 compilación 1507, Direct2D proporciona [**ID2D1ImageSourceFromWic,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)una manera más sencilla de descodificar JPEG en Direct2D mientras se aprovechan las optimizaciones de YC <sub>b</sub>C <sub>r.</sub> **ID2D1ImageSourceFromWic** realiza automáticamente todas las comprobaciones de funcionalidad de YC <sub>b</sub>C <sub>r</sub> necesarias; usa la ruta de acceso de código optimizada siempre que sea posible y, de lo contrario, usa una reserva. También permite nuevas optimizaciones, como solo las subregiones de almacenamiento en caché de la imagen que se necesitan a la vez.

Para obtener más información sobre [**el uso de ID2D1ImageSourceFromWic,**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)consulte el ejemplo del [SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)de ajuste de fotos de Direct2D .

## <a name="related-topics"></a>Temas relacionados

* [Optimizaciones JPEG YCbCr en direct2D y ejemplo de WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)

---
description: A partir de Windows 8.1, el códec JPEG de Windows Imaging Component (WIC) admite la lectura y escritura de datos de imagen en su formulario YCbCr nativo.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Compatibilidad con JPEG YCbCr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002030"
---
# <a name="jpeg-ycbcr-support"></a>Compatibilidad con JPEG YCbCr

A partir de Windows 8.1, el códec JPEG de [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) admite la lectura y escritura de datos de imagen en su forma nativa<sub>de C</sub><sub>r</sub> de YC. La compatibilidad con C<sub>r</sub> de WIC YC<sub>b</sub>se puede usar junto con [Direct2D](../direct2d/direct2d-portal.md) para representar datos de píxeles de c<sub>r</sub> <sub>de YC con</sub>un efecto de imagen. Además, el códec de JPEG de WIC puede consumir datos de píxeles<sub>de C</sub><sub>r</sub> de YC producidos por determinados controladores de cámara a través de Media Foundation.

Los datos de píxeles<sub>de C</sub><sub>r</sub> de la YC consumen mucha menos memoria que los formatos de píxel de BGRA estándar. Además, el acceso a los datos<sub>de C</sub><sub>r</sub> de la YC permite descargar algunas fases de la canalización de descodificación y codificación JPEG a Direct2D, que es una GPU acelerada. Mediante el uso de YC<sub>b</sub>C<sub>r</sub>, la aplicación puede reducir el consumo de memoria JPEG y los tiempos de carga de las mismas imágenes de tamaño y calidad. O bien, la aplicación puede usar más imágenes JPEG de mayor resolución sin sufrir penalizaciones de rendimiento.

En este tema se describe cómo funcionan los datos de<sub>b</sub><sub>r</sub> de la YC y cómo usarlos en WIC y Direct2D.

-   [Acerca de los datos JPEG YC<sub>b</sub>C<sub>r</sub>](#about-jpeg-ycbcr-data)
    -   [Modelo de color de C<sub>r</sub> de YC<sub>b</sub>](#ycbcr-color-model)
    -   [Diseños de memoria plana frente a intercalados](#planar-versus-interleaved-memory-layouts)
    -   [Submuestreo de croma](#chroma-subsampling)
    -   [Uso de JPEG de YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Usar datos JPEG YC<sub>b</sub>C<sub>r</sub>](#using-jpeg-ycbcr-data)
    -   [Uso de imágenes de imagen JPEG<sub>de C</sub><sub>r</sub> en YC](#using-ycbcr-jpeg-images)
    -   [API de componentes de Windows Imaging](#windows-imaging-component-apis)
    -   [API de Direct2D](#direct2d-apis)
    -   [Determinar si se admite la configuración de la YC<sub>b</sub>C<sub>r</sub>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Descodificación de datos de píxeles<sub>de C</sub><sub>r</sub> de la YC](#decoding-ycbcr-pixel-data)
    -   [Transformando datos de píxeles<sub>de C</sub><sub>r</sub> de YC](#transforming-ycbcr-pixel-data)
    -   [Codificación de datos de píxeles de C<sub>r</sub> de código YC<sub>b</sub>](#encoding-ycbcr-pixel-data)
    -   [Descodificación de datos de píxeles<sub>de C</sub><sub>r</sub> de la YC en Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Temas relacionados](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Acerca de los datos JPEG YC<sub>b</sub>C<sub>r</sub>

En esta sección se explican algunos conceptos clave necesarios para entender cómo funciona la compatibilidad con<sub>la unidad C</sub>de<sub>r</sub> en WIC y sus ventajas principales.

### <a name="ycsubbsubcsubrsub-color-model"></a>Modelo de color de C<sub>r</sub> de YC<sub>b</sub>

WIC en Windows 8 y versiones anteriores admite cuatro [modelos de color](-wic-codec-native-pixel-formats.md)diferentes, el más común de los cuales es RGB/BGR. Este modelo de color define los datos de color mediante los componentes rojo, verde y azul; también se puede usar un cuarto componente alfa.

Esta es una imagen descomponeda de sus componentes rojo, verde y azul.

![una imagen descomponeda en sus componentes rojo, verde y azul.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> es un modelo de color alternativo que define los datos de color mediante un componente de luminancia (y) y dos componentes de crominancia (c<sub>b</sub> y c<sub>r</sub>). Se utiliza normalmente en escenarios de imágenes y vídeos digitales. El término "YC<sub>b</sub>C<sub>r</sub> " se utiliza a menudo indistintamente con YUV, aunque los dos son técnicamente distintos.

Hay varias variaciones de YC<sub>b</sub>C<sub>r</sub> que difieren en el espacio de colores y en las definiciones de rangos dinámicos; WIC es compatible específicamente con los datos<sub>de c</sub><sub>r</sub> de la YC de formato JPEG JFIF. Para obtener más información, consulte la [especificación de JPEG ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

A continuación se muestra una imagen descompuesta por los componentes de y, C<sub>b</sub>y c<sub>r</sub> .

![una imagen descomponeda en sus componentes y, CB y CR.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Diseños de memoria plana frente a intercalados

En esta sección se describen algunas diferencias entre el acceso y el almacenamiento de datos de píxeles RGB en memoria frente a datos de C<sub>r</sub> de<sub>la YC.</sub>

Los datos de píxeles RGB se almacenan normalmente mediante un diseño de memoria intercalado. Esto significa que los datos de un componente de color único se intercalan entre píxeles y cada píxel se almacena de forma contigua en la memoria.

Esta es una figura que muestra los datos de píxeles RGBA almacenados en un diseño de memoria intercalada.

![una figura que muestra los datos de píxeles RGBA almacenados en un diseño de memoria intercalado.](graphics/ycbcr3.png)

Normalmente, los datos<sub>de C</sub><sub>r</sub> de la YC se almacenan con un diseño de memoria plana. Esto significa que cada componente de color se almacena por separado en su propio plano contiguo, para un total de tres planos. En otra configuración común, los componentes C<sub>b</sub> y c<sub>r</sub> se intercalan y almacenan juntos, mientras que el componente Y permanece en su propio plano, para un total de dos planos.

Esta es una figura que muestra los datos planos y y, a continuación, los datos de píxeles<sub>de c</sub><sub>r</sub> , un diseño de memoria de c<sub>r</sub> de<sub>la YC común</sub>.

![una figura que muestra los datos planos y de CbCr intercalados, un diseño de memoria de YCbCr común.](graphics/ycbcr4.png)

En WIC y Direct2D, cada plano de color se trata como su propio objeto distinto (un objeto [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)), y colectivamente estos planos forman los datos de respaldo para una imagen de <sub>r r</sub> de YC <sub>b</sub>.

Aunque WIC admite el acceso a los datos de x<sub>r</sub> de<sub>la YC en</sub>las configuraciones de 2 y 3 planos, Direct2D solo admite los anteriores (y y c<sub>b</sub><sub>r</sub>). Por lo tanto, cuando se usan WIC y Direct2D juntos, siempre debe usar la configuración de 2<sub>r</sub> de 1 plano YC<sub>b</sub>.

### <a name="chroma-subsampling"></a>Submuestreo de croma

El modelo de color YC<sub>b</sub>C<sub>r</sub> es muy adecuado para escenarios de creación de imágenes digitales, ya que puede aprovechar algunos aspectos del sistema visual humano. En concreto, los seres humanos son más sensibles a los cambios en la luminancia (luminosidad) de una imagen y menos sensible a la crominancia (color). Al dividir los datos de color en componentes independientes de luminancia y crominancia, podemos comprimir selectivamente los componentes de crominancia para lograr un ahorro de espacio con una pérdida mínima de calidad.

Una técnica para hacerlo se denomina submuestreo de croma. Los planos C<sub>b</sub> y c<sub>r</sub> se submuestrean (downscaled) en una de las dimensiones horizontal y vertical. Por motivos históricos, normalmente se hace referencia a cada modo de submuestreo de croma con una relación de tres partes J:a: b.



| Modo de submuestreo | Downscale horizontal | Downscale vertical | Bits por píxel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Incluye datos Y.

En la tabla anterior, si usa YC<sub>b</sub>C<sub>r</sub> para almacenar los datos de imagen no comprimidos, puede lograr un ahorro de memoria de un 25% a un 62,5% frente a los datos RGBA de 32 bits por píxel, en función del modo de submuestreo cromado que se use.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Uso de JPEG de YC<sub>b</sub>C<sub>r</sub>

En un nivel alto, la canalización de descompresión JPEG consta de las siguientes fases:

1.  Descompresión de la entropía (por ejemplo, Huffman)
2.  Realizar la descuantificación
3.  Realizar la transformación de coseno discreto inverso
4.  Realizar el muestreo de croma en los datos de c<sub>b</sub><sub>r</sub>
5.  Convertir datos de la YC<sub>b</sub>C<sub>r</sub> en rgba (si es necesario)

Al hacer que el códec JPEG genere datos<sub>de C</sub><sub>r</sub> en YC, se pueden evitar los dos pasos finales del proceso de descodificación o aplazarlos a la GPU. Además del ahorro de memoria que se muestra en la sección anterior, esto reduce considerablemente el tiempo total necesario para descodificar la imagen. Se aplican los mismos ahorros al codificar los datos de C<sub>r</sub> de<sub>la YC.</sub>

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Usar datos JPEG YC<sub>b</sub>C<sub>r</sub>

En esta sección se explica cómo usar WIC y Direct2D para operar con los datos de C<sub>r</sub> <sub>en YC.</sub>

Para ver las instrucciones de este documento que se usan en la práctica, consulte el ejemplo de las [optimizaciones de JPEG YCbCr en Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , donde se muestran todos los pasos necesarios para descodificar y representar el contenido<sub>de C</sub><sub>r</sub> de YC en una aplicación de Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Uso de imágenes de imagen JPEG<sub>de C</sub><sub>r</sub> en YC

La gran mayoría de las imágenes JPEG se almacenan como YC<sub>b</sub>C<sub>r</sub>. Algunos JPEG contienen datos CMYK o de escala de grises y no utilizan YC<sub>b</sub>C<sub>r</sub>. Esto significa que normalmente, pero no siempre, puede usar directamente contenido JPEG existente sin ninguna modificación.

WIC y Direct2D no admiten todas las configuraciones posibles de la YC<sub>b</sub>c<sub>r</sub> y la compatibilidad con la tecnología<sub>de c</sub><sub>r</sub> en Direct2D depende del hardware y del controlador de gráficos subyacentes. Por este motivo, una canalización de imágenes de uso general debe ser robusta para las imágenes que no usan la unidad<sub>b</sub>c<sub>r</sub> de la YC (incluidos otros formatos de imagen comunes, como PNG o BMP) o para los casos en los que no está disponible la compatibilidad con la<sub>b</sub>c<sub>r</sub> de la YC. Le recomendamos que mantenga su canalización de creación de imágenes basada en BGRA existente y que habilite la unidad<sub>b</sub><sub>r r</sub> como una optimización del rendimiento cuando esté disponible.

### <a name="windows-imaging-component-apis"></a>API de componentes de Windows Imaging

WIC en Windows 8.1 agrega tres nuevas interfaces para proporcionar acceso a los datos JPEG YC<sub>b</sub>C<sub>r</sub> .

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) es análogo a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), con la salvedad de que genera píxeles en una configuración plana, incluidos los datos de <sub>b</sub><sub>r</sub> de la YC. Puede obtener esta interfaz llamando a QueryInterface en una implementación de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que admita el acceso al plano. Esto incluye la implementación del códec JPEG de [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) , así como [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)y [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) ofrece la posibilidad de codificar datos de píxeles planos, incluidos los datos de C <sub>r</sub> de <sub>la YC.</sub> Puede obtener esta interfaz llamando a QueryInterface en la implementación del códec JPEG de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) permite a [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) consumir datos de píxeles planos, incluida la <sub>x C</sub><sub>r</sub>, y convertirlos a un formato de píxel intercalado. No expone la capacidad de convertir datos de píxeles intercalados en un formato plano. Puede obtener esta interfaz llamando a QueryInterface en la implementación proporcionada por Windows de **IWICFormatConverter**.

### <a name="direct2d-apis"></a>API de Direct2D

Direct2D en Windows 8.1 admite datos de píxeles planos<sub>de c</sub><sub>r</sub> de YC con el nuevo efecto de imagen YC<sub>b</sub>c<sub>r</sub> . Este efecto proporciona la capacidad de representar datos<sub>de</sub>C<sub>r</sub> de YC. El efecto toma como entrada dos interfaces [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) : una que contiene datos de Y planos en el formato de dxgi \_ \_ \_ UNORM, y otra que contiene datos de CbCr intercalados en formato de dxgi \_ \_ R8G8 \_ UNORM. Normalmente, este efecto se usa en lugar de **ID2D1Bitmap** que habría contenido BGRA píxeles.

El efecto de imagen YC<sub>b</sub><sub>c r está</sub> pensado para usarse junto con las API de<sub>r r</sub> de<sub>WIC b de</sub>WIC que proporcionan los datos<sub>de c</sub><sub>r</sub> de la YC. Esto actúa de manera eficaz para descargar parte del trabajo de descodificación de la CPU a la GPU, donde se puede procesar mucho más rápido y en paralelo.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Determinar si se admite la configuración de la YC<sub>b</sub>C<sub>r</sub>

Como se indicó antes, la aplicación debe ser robusta en los casos en los que no está disponible la compatibilidad con la<sub>b</sub><sub>r</sub> de YC. En esta sección se describen las condiciones que debe comprobar la aplicación. Si se produce un error en cualquiera de las siguientes comprobaciones, la aplicación debe revertir a una canalización estándar basada en BGRA.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>¿El componente WIC admite el acceso a datos YC<sub>b</sub>C<sub>r</sub> ?

Solo el códec JPEG proporcionado por Windows y ciertas transformaciones de WIC admiten el acceso a datos de C<sub>r</sub> de<sub>la YC.</sub> Para obtener una lista completa, consulte la sección [API de componentes de creación de imágenes de Windows](#windows-imaging-component-apis) .

Para obtener una de<sub>las interfaces de e/s de</sub> YC planas<sub>b</sub>, llame a QueryInterface en la interfaz original. Se producirá un error si el componente no admite el acceso a datos de C<sub>r</sub> de la YC<sub>b</sub>.

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>¿La transformación de WIC solicitada es compatible con YC<sub>b</sub>C<sub>r</sub>?

Después de obtener un [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform), primero debe llamar a [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Este método toma como parámetros de entrada el conjunto completo de transformaciones que se desea aplicar a<sub>los datos de e/s de</sub> la YC plana<sub>b</sub>, y devuelve un valor booleano que indica la compatibilidad, así como las dimensiones más cercanas al tamaño solicitado que se puede devolver. Debe comprobar los tres valores antes de tener acceso a los datos de píxel con [**IWICPlanarBitmapSourceTransform:: copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Este patrón es similar al uso de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>¿El controlador de gráficos es compatible con las características necesarias para usar la<sub>b</sub>C<sub>r</sub> con Direct2D?

Esta comprobación solo es necesaria si se usa el efecto de c<sub>r</sub> de Direct2D YC<sub>b</sub>para representar el contenido de c<sub>r</sub> <sub>de YC.</sub> Direct2D almacena los datos de x<sub>r</sub> <sub>de YC con</sub>los formatos de dxgi \_ \_ \_ UNORM y dxgi \_ format \_ R8G8 \_ UNORM pixel, que no están disponibles en todos los controladores de gráficos.

Antes de usar el efecto de imagen YC <sub>b</sub>C <sub>r</sub> , debe llamar a [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para asegurarse de que el controlador admite ambos formatos.

### <a name="sample-code"></a>Código de ejemplo

A continuación se muestra un ejemplo de código que muestra las comprobaciones recomendadas. Este ejemplo se ha tomado de las [optimizaciones de JPEG YCbCr en el ejemplo de Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Descodificación de datos de píxeles<sub>de C</sub><sub>r</sub> de la YC

Si desea obtener datos de píxeles <sub>de</sub>C <sub>r</sub> de YC, debe llamar a [**IWICPlanarBitmapSourceTransform:: copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Este método copia los datos de píxeles en una matriz de estructuras [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) rellenadas, una por cada plano de datos que desea (por ejemplo, y y c <sub>b</sub><sub>r</sub>). Un **WICBitmapPlane** contiene información sobre los datos de píxeles y apunta al búfer de memoria que recibirá los datos.

Si desea usar los datos de píxeles <sub>de x C</sub><sub>r</sub> de la YC con otras API de WIC, debe crear un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)configurado correctamente, llamar a [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) para obtener el búfer de memoria subyacente y asociar el búfer con el [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) que se usa para recibir los datos de píxeles <sub>de C</sub><sub>r</sub> de la YC. Después, puede usar el [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normalmente.

Por último, si desea representar los datos de <sub>b</sub><sub>r</sub> de <sub>la YC en</sub>Direct2D, debe crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a partir de cada [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) y usarlo como origen para el efecto de imagen de C <sub>r</sub> de la YC. WIC permite solicitar varias configuraciones planas. Al interoperar con Direct2D, debe solicitar dos planos, uno con GUID \_ WICPixelFormat8bppY y el otro con GUID \_ WICPixelFormat16bppCbCr, ya que se trata de la configuración esperada por Direct2D.

### <a name="code-sample"></a>Ejemplo de código

A continuación se muestra un ejemplo de código en el que se muestran los pasos para descodificar y representar datos<sub>de C</sub><sub>r</sub> de la YC en Direct2D. Este ejemplo se ha tomado de las [optimizaciones de JPEG YCbCr en el ejemplo de Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


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



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformando datos de píxeles<sub>de C</sub><sub>r</sub> de YC

Transformar los datos de <sub>C</sub><sub>r</sub> de YC es casi idéntico a la descodificación, ya que ambas implican [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La única diferencia es el objeto de WIC del que obtuvo la interfaz. Las ventanas proporcionadas Scaler, flip Rotator y transformación de color admiten el acceso YC<sub>b</sub>C<sub>r</sub> .

### <a name="chaining-transforms-together"></a>Encadenar transformaciones juntas

WIC admite la noción de encadenamiento de varias transformaciones. Por ejemplo, puede crear la siguiente canalización de WIC:

![diagrama de una canalización de WIC que empieza con un descodificador JPEG.](graphics/ycbcr5.png)

Después, puede llamar a QueryInterface en [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) para obtener [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La transformación de color puede comunicarse con las transformaciones anteriores y puede exponer las capacidades de agregado de cada fase de la canalización. WIC garantiza que los datos<sub>de</sub>C<sub>r</sub> de la YC se conservan en todo el proceso. Este encadenamiento solo funciona cuando se usan componentes que<sub></sub>admiten el acceso a<sub>r C r</sub> .

### <a name="jpeg-codec-optimizations"></a>Optimizaciones de códec JPEG

De forma similar a la implementación de descodificación de fotogramas JPEG de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), la implementación de descodificación de fotogramas JPEG de [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) admite el escalado y la rotación de dominios nativa JPEG DCT. Puede solicitar una potencia de dos downscale o un giro directamente desde el descodificador JPEG. Normalmente, esto da como resultado una mayor calidad y rendimiento que el uso de las transformaciones discretas.

Además, al encadenar una o varias transformaciones de WIC después del descodificador JPEG, se puede aprovechar el escalado y la rotación JPEG nativos para satisfacer la operación solicitada de agregado.

### <a name="format-conversions"></a>Conversiones de formato

Use [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) para convertir datos de píxeles <sub>de C</sub><sub>r</sub> de la YC plana a un formato de píxel intercalado como GUID \_ WICPixelFormat32bppPBGRA. WIC en Windows 8.1 no proporciona la capacidad de realizar la conversión a un formato de píxel<sub>de C</sub><sub>r</sub> plano de x.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codificación de datos de píxeles de C<sub>r</sub> de código YC<sub>b</sub>

Use [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) para codificar los datos de píxeles <sub>de C</sub><sub>r</sub> de la YC en el codificador JPEG. La codificación YC <sub>b</sub>C <sub>r</sub> Data **IWICPlanarBitmapFrameEncode** es similar, pero no idéntica a la codificación de datos intercalados mediante [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). La interfaz plana solo expone la capacidad de escribir datos de imagen de marco plano y debe seguir usando la interfaz de codificación de fotogramas para establecer los metadatos o una miniatura y para confirmar al final de la operación.

En el caso típico, debe seguir estos pasos:

1.  Obtenga el [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) como normal. Si desea configurar el submuestreo de croma, establezca la opción codificador de [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) al crear el marco.
2.  Si tiene que establecer los metadatos o una miniatura, hágalo usando [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) como normal.
3.  QueryInterface para [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Establezca los datos de píxeles de C <sub>r</sub> de <sub>la YC mediante</sub> [**IWICPlanarBitmapFrameEncode:: WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) o [**IWICPlanarBitmapFrameEncode:: WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). A diferencia de lo que sucede con sus homólogos de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , estos métodos se proporcionan con una matriz de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) o [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) que contiene los planos de píxeles <sub>de C</sub><sub>r</sub> de YC.
5.  Cuando haya terminado, llame a [**IWICBitmapFrameEncode:: commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Descodificación de datos de píxeles<sub>de C</sub><sub>r</sub> de la YC en Windows 10

A partir de la compilación 1507 de Windows 10, Direct2D proporciona [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), una forma más sencilla de descodificar los archivos JPEG en Direct2D, al tiempo que se aprovechan las OPTIMIZAciones <sub>YC de</sub>C <sub>r</sub> . **ID2D1ImageSourceFromWic** realiza automáticamente todas las comprobaciones necesarias de la funcionalidad de la YC <sub>b</sub>C <sub>r</sub> ; usa el codepath optimizado siempre que sea posible y utiliza una reserva en caso contrario. También permite nuevas optimizaciones, como solo almacenar en caché subregiones de la imagen que se necesitan a la vez.

Para obtener más información sobre el uso de [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), consulte el [ejemplo](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)de SDK de ajuste fotográfico de Direct2D.

## <a name="related-topics"></a>Temas relacionados

* [Optimización de JPEG YCbCr en el ejemplo de Direct2D y WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)

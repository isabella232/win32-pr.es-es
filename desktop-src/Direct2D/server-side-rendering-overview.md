---
title: Usar Direct2D para la representación de Server-Side
description: Describe el uso de Direct2D para la representación del lado servidor.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, representación del lado servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420835"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Usar Direct2D para la representación de Server-Side

Direct2D es adecuado para aplicaciones gráficas que requieren la representación del lado servidor en Windows Server. En esta información general se describen los aspectos básicos del uso de Direct2D para la representación del lado servidor. Contiene las secciones siguientes:

-   [Requisitos para la representación de Server-Side](#requirements-for-server-side-rendering)
-   [Opciones para las API disponibles](#options-for-available-apis)
    -   [GDI](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Cómo usar Direct2D para la representación de Server-Side](#how-to-use-direct2d-for-server-side-rendering)
    -   [Representación de software](#software-rendering)
    -   [Multithreading](#multithreading)
    -   [Generar un archivo de mapa de bits](#generating-a-bitmap-file)
-   [Conclusión](#conclusion)
-   [Temas relacionados](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Requisitos para la representación de Server-Side

A continuación se muestra un escenario típico para un servidor de gráficos: los gráficos y los gráficos se representan en un servidor y se entregan como mapas de bits en respuesta a las solicitudes Web. El servidor puede estar equipado con una tarjeta gráfica de low-end o sin tarjeta gráfica.

Este escenario revela tres requisitos de aplicación. En primer lugar, la aplicación debe controlar varias solicitudes simultáneas de forma eficaz, especialmente en los servidores de varios núcleos. En segundo lugar, la aplicación debe usar la representación de software cuando se ejecuta en servidores con una tarjeta gráfica de low-end o sin tarjeta gráfica. Por último, la aplicación debe ejecutarse como un servicio en la sesión 0 para que no sea necesario que un usuario inicie sesión. Para obtener más información acerca de la sesión 0, vea [impacto del aislamiento de sesión 0 en servicios y controladores en Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).

## <a name="options-for-available-apis"></a>Opciones para las API disponibles

Hay tres opciones para la representación del lado servidor: GDI, GDI+ y Direct2D. Como GDI y GDI+, Direct2D es una API de representación de 2D nativa que proporciona a las aplicaciones un mayor control sobre el uso de los dispositivos de gráficos. Además, Direct2D es compatible de forma exclusiva con un generador multiproceso y un único subproceso. En las secciones siguientes se comparan todas las API en términos de dibujo de calidad y representación en el lado servidor multiproceso.

### <a name="gdi"></a>GDI

A diferencia de Direct2D y GDI+, GDI no admite características de dibujo de alta calidad. Por ejemplo, GDI no admite el suavizado de contorno para crear líneas suaves y solo tiene compatibilidad limitada con la transparencia. En función de los resultados de las pruebas de rendimiento de gráficos en Windows 7 y Windows Server 2008 R2, Direct2D se escala de forma más eficaz que GDI, a pesar del rediseño de los bloqueos en GDI. Para obtener más información acerca de estos resultados de pruebas, vea [Engineering Windows 7 Graphics performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Además, las aplicaciones que usan GDI se limitan a los identificadores de GDI 10240 por proceso y 65536 a los identificadores de GDI por sesión. La razón es que internamente Windows usa una palabra de 16 bits para almacenar el índice de identificadores de cada sesión.

### <a name="gdi"></a>GDI+

Aunque GDI+ admite el suavizado de contorno y la combinación alfa para el dibujo de alta calidad, el problema principal con GDI+ para los escenarios de servidor es que no admite la ejecución en la sesión 0. Dado que la sesión 0 solo admite la funcionalidad no interactiva, las funciones que interactúan directa o indirectamente con los dispositivos de pantalla recibirán errores. Algunos ejemplos específicos de funciones son no solo aquellos que se ocupan de mostrar los dispositivos, sino que también se ocupan indirectamente de los controladores de dispositivos.

De forma similar a GDI, GDI+ está limitado por su mecanismo de bloqueo. Los mecanismos de bloqueo en GDI+ son los mismos en Windows 7 y Windows Server 2008 R2, como en las versiones anteriores.

### <a name="direct2d"></a>Direct2D

Direct2D es una API de gráficos 2D de modo inmediato y con aceleración de hardware que proporciona alto rendimiento y representación de alta calidad. Ofrece una fábrica de un solo subproceso y un generador multiproceso y el escalado lineal de la representación de software específica del curso.

Para ello, Direct2D define una interfaz de fábrica raíz. Como norma general, un objeto creado en un generador solo se puede usar con otros objetos creados desde el mismo generador. El autor de la llamada puede solicitar un generador de un solo subproceso o multiproceso cuando se crea. Si se solicita un generador de un solo subproceso, no se realiza ningún bloqueo de subprocesos. Si el autor de la llamada solicita un generador multiproceso, se adquiere un bloqueo de subprocesos en toda la fábrica siempre que se realiza una llamada a Direct2D.

Además, el bloqueo de subprocesos en Direct2D es más granular que en GDI y GDI+, de modo que el aumento del número de subprocesos tiene un impacto mínimo en el rendimiento.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Cómo usar Direct2D para la representación de Server-Side

En las secciones siguientes se describe cómo usar la representación de software, cómo usar óptimamente un generador de un solo subproceso y multiproceso, y cómo dibujar y guardar un dibujo complejo en un archivo.

### <a name="software-rendering"></a>Representación de software

Las aplicaciones de servidor usan la representación de software mediante la creación del destino de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , con el tipo de destino de representación establecido en D2D1 \_ representar el software de \_ \_ tipo destino \_ o D2D1 \_ representar \_ \_ \_ el tipo de destino predeterminado. Para obtener más información sobre los destinos de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , vea el método [**ID2D1Factory:: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) . para obtener más información sobre los tipos de destino de representación, vea [**D2D1 \_ Render \_ target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Subprocesamiento múltiple

Saber cómo crear y compartir factorías y representar destinos entre subprocesos puede afectar significativamente al rendimiento de una aplicación. Las tres figuras siguientes muestran tres enfoques variados. El enfoque óptimo se muestra en la figura 3.

![diagrama multithreading de direct2d con un solo destino de representación.](images/server-side-rendering-1.png)

En la figura 1, los distintos subprocesos comparten el mismo generador y el mismo destino de representación. Este enfoque puede provocar resultados imprevisibles en casos en los que varios subprocesos cambian simultáneamente el estado del destino de representación compartido, como establecer simultáneamente la matriz de transformación. Dado que el bloqueo interno en Direct2D no sincroniza un recurso compartido, como los destinos de representación, este enfoque puede provocar un error en la llamada [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) en el subproceso 1, porque en el subproceso 2, la llamada **beginDraw** ya está usando el destino de representación compartido.

![diagrama multithreading de direct2d con varios destinos de representación.](images/server-side-rendering-2.png)

Para evitar los resultados imprevisibles encontrados en la figura 1, la figura 2 muestra un generador multiproceso con cada subproceso que tiene su propio destino de representación. Este enfoque funciona, pero funciona eficazmente como una aplicación de un solo subproceso. La razón es que el bloqueo de toda la fábrica solo se aplica al nivel de operación de dibujo y todas las llamadas de dibujo del mismo generador se serializan en consecuencia. Como resultado, el subproceso 1 se bloquea al intentar entrar en una llamada de dibujo, mientras que el subproceso 2 se encuentra en medio de ejecutar otra llamada de dibujo.

![diagrama multithreading de direct2d con varios generadores y varios destinos de representación.](images/server-side-rendering-3.png)

En la figura 3 se muestra el enfoque óptimo, donde se usan un generador de un solo subproceso y un destino de representación de un solo subproceso. Dado que no se realiza ningún bloqueo cuando se usa un generador de un solo subproceso, las operaciones de dibujo de cada subproceso se pueden ejecutar simultáneamente para lograr un rendimiento óptimo.

### <a name="generating-a-bitmap-file"></a>Generar un archivo de mapa de bits

Para generar un archivo de mapa de bits mediante la representación de software, use un destino de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Use un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) para escribir el mapa de bits en un archivo. Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar el mapa de bits en un formato de imagen especificado. En el ejemplo de código siguiente se muestra cómo dibujar y guardar la siguiente imagen en un archivo.

![imagen de salida de ejemplo.](images/saveasimagefile-sample.png)

En primer lugar, este ejemplo de código crea un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) y un destino de representación [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) . Después representa un dibujo con texto, una geometría de trazado que representa un reloj de hora y un cristal de hora transformada en un mapa de bits de WIC. A continuación, usa [IWICStream:: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) para guardar el mapa de bits en un archivo. Si su aplicación necesita guardar el mapa de bits en la memoria, use [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) en su lugar. Por último, usa [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar el mapa de bits.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Conclusión

Tal y como se muestra en el apartado anterior, el uso de Direct2D para la representación del lado servidor es sencillo y sencillo. Además, proporciona una representación de alta calidad y alta pueden paralelizar que se puede ejecutar en entornos con privilegios bajos del servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 
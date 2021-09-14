---
title: Información general sobre los destinos de representación
description: Describe los distintos tipos de destinos de representación de Direct2D y cómo usarlos.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinos de representación
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162610"
---
# <a name="render-targets-overview"></a>Información general sobre los destinos de representación

Un destino de representación es un recurso que hereda de la [**interfaz ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales. En este tema se describen los distintos tipos de destinos de representación de Direct2D y cómo usarlos.

-   [Destinos de representación](#render-targets-overview)
    -   [Representar características de destino](#render-target-features)
    -   [Representación de recursos de destino](#render-target-resources)
    -   [Comandos de dibujo](#drawing-commands)
    -   [Tratamiento de errores](#error-handling)
-   [Ejemplo: Representación de contenido en una ventana](#example-render-content-to-a-window)

## <a name="render-targets"></a>Destinos de representación

Un destino de representación es un recurso que hereda de la [**interfaz ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales. Hay varios tipos de destinos de representación que se pueden usar para representar gráficos de las maneras siguientes:

-   [**Los objetos ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representan el contenido en una ventana.
-   [**Los objetos ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) se representan en un contexto de dispositivo GDI.
-   Los objetos de destino de representación de mapa de bits representan el contenido en un mapa de bits fuera de la pantalla.
-   Los objetos de destino de representación DXGI se representan en una superficie DXGI para su uso con Direct3D.

Dado que un destino de representación está asociado a un dispositivo de representación determinado, es un recurso dependiente del dispositivo y deja de funcionar si se quita el dispositivo.

### <a name="render-target-features"></a>Representar características de destino

Puede especificar si un destino de representación usa la aceleración de hardware y si un equipo local o remoto representa la pantalla remota. Los destinos de representación se pueden configurar para la representación con alias o suavizado de contorno. Para representar escenas con un gran número de primitivas, un desarrollador también puede representar gráficos 2D en modo con alias y usar el suavizado de contorno de múltiples muestras D3D para lograr una mayor escalabilidad.

Los destinos de representación también pueden agrupar las operaciones de dibujo en capas representadas por la [**interfaz ID2D1Layer.**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) Las capas son útiles para recopilar operaciones de dibujo que se van a componer juntas al representar un marco. En algunos escenarios, esta puede ser una alternativa útil a la representación en un destino de representación de mapa de bits y, a continuación, volver a usar el contenido del mapa de bits, ya que los costos de asignación de capas son inferiores a los de [**id2D1BitmapRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)

Los destinos de representación pueden crear nuevos destinos de representación que sean compatibles con ellos mismos, lo que resulta útil para la representación intermedia fuera de la pantalla, al tiempo que se conservan las distintas propiedades de destino de representación que se han establecido en el original.

También es posible representar mediante GDI en un destino de representación de Direct2D llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un destino de representación para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tiene métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) y [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que se pueden usar para recuperar un contexto de dispositivo GDI. La representación a través de GDI solo es posible si el destino de representación se creó con la marca compatible con [**\_ \_ \_ \_ GDI \_ RENDER TARGET USAGE de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) establecida. Esto es útil para las aplicaciones que se representan principalmente con Direct2D pero que tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de representar con GDI. Para obtener más información, vea [Introducción a la interoperación de Direct2D y GDI.](direct2d-and-gdi-interoperation-overview.md)

### <a name="render-target-resources"></a>Representación de recursos de destino

Al igual que un generador, un destino de representación puede crear recursos de dibujo. Los recursos creados por un destino de representación son recursos dependientes del dispositivo (al igual que el destino de representación). Un destino de representación puede crear los siguientes tipos de recursos:

-   Mapas de bits
-   Pinceles
-   Capas
-   Mallas

### <a name="drawing-commands"></a>Comandos de dibujo

Para representar el contenido, use los métodos de dibujo de destino de representación. Antes de empezar a dibujar, llame al [**método ID2D1RenderTarget::BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Cuando haya terminado de dibujar, llame al [**método ID2D1RenderTarget::EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Entre estas llamadas, se usan los métodos Draw y Fill para representar los recursos de dibujo. La mayoría de los métodos Draw y Fill toman una forma (ya sea una primitiva o una geometría) y un pincel para rellenar o delinear la forma.

Los destinos de representación proporcionan métodos para recortar, aplicar máscaras de opacidad y transformar el espacio de coordenadas.

Direct2D usa un sistema de coordenadas con la mano izquierda: los valores positivos del eje X se dirigen a la derecha y los valores positivos del eje Y avanzan hacia abajo.

### <a name="error-handling"></a>Tratamiento de errores

Los comandos de dibujo de destino de representación no indican si la operación solicitada se ha realizado correctamente. Para averiguar si hay errores de dibujo, llame al método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino de representación o al [**método EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obtener **un HRESULT**.

## <a name="example-render-content-to-a-window"></a>Ejemplo: Representación de contenido en una ventana

En el ejemplo siguiente se [**usa el método CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) para crear un [**id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



En el ejemplo siguiente se [**usa ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para dibujar texto en la ventana.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



En este ejemplo se ha omitido el código.

 

 
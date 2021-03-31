---
title: Información general de destinos de representación
description: Describe los diferentes tipos de destinos de representación de Direct2D y cómo usarlos.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, destinos de representación
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995382"
---
# <a name="render-targets-overview"></a>Información general de destinos de representación

Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales. En este tema se describen los diferentes tipos de destinos de representación de Direct2D y cómo usarlos.

-   [Destinos de representación](#render-targets-overview)
    -   [Características de destino de representación](#render-target-features)
    -   [Representar recursos de destino](#render-target-resources)
    -   [Dibujar comandos](#drawing-commands)
    -   [Tratamiento de errores](#error-handling)
-   [Ejemplo: representación de contenido en una ventana](#example-render-content-to-a-window)

## <a name="render-targets"></a>Destinos de representación

Un destino de representación es un recurso que hereda de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Un destino de representación crea recursos para dibujar y realiza operaciones de dibujo reales. Hay varios tipos de destinos de representación que se pueden usar para representar gráficos de las siguientes maneras:

-   Los objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representan el contenido en una ventana.
-   Los objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) se representan en un contexto de dispositivo GDI.
-   Los objetos de destino de representación de mapas de bits representan el contenido en un mapa de bits fuera de la pantalla.
-   Los objetos de destino de representación de DXGI se representan en una superficie de DXGI para su uso con Direct3D.

Dado que un destino de representación está asociado a un dispositivo de representación determinado, es un recurso dependiente del dispositivo y deja de funcionar si se quita el dispositivo.

### <a name="render-target-features"></a>Características de destino de representación

Puede especificar si un destino de representación utiliza la aceleración de hardware y si la pantalla remota se representa en un equipo local o remoto. Los destinos de representación pueden configurarse para la representación con alias o con suavizado de contorno. En el caso de las escenas de representación con un gran número de primitivas, un desarrollador también puede representar gráficos 2D en modo de alias y usar el suavizado de contorno de muestreo múltiple para lograr una mayor escalabilidad.

Los destinos de representación también pueden agrupar las operaciones de dibujo en capas representadas por la interfaz [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . Las capas son útiles para recopilar operaciones de dibujo que se van a componer juntas al representar un fotograma. En algunos escenarios, puede ser una alternativa útil a la representación en un destino de representación de mapas de bits y, a continuación, volver a usar el contenido del mapa de bits, ya que los costos de asignación para la disposición en capas son menores que para un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Los destinos de representación pueden crear nuevos destinos de representación que son compatibles con ellos mismos, lo que resulta útil para la representación fuera de pantalla intermedia, a la vez que conserva las distintas propiedades de representación y destino que se establecieron en el original.

También es posible representar usando GDI en un destino de representación de Direct2D llamando a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un destino de representación para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tiene los métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) y [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) en él que se pueden usar para recuperar un contexto de dispositivo GDI. La representación a través de GDI solo es posible si el destino de representación se creó con el conjunto de marcadores [**compatible con GDI de uso de destino de representación de D2D1 \_ \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) . Esto resulta útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de presentar con GDI. Para obtener más información, vea [información general sobre la interoperación de Direct2D y GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Representar recursos de destino

Al igual que un generador, un destino de representación puede crear recursos de dibujo. Los recursos creados por un destino de representación son recursos dependientes del dispositivo (al igual que el destino de representación). Un destino de representación puede crear los siguientes tipos de recursos:

-   Mapas de bits
-   Pinceles
-   Capas
-   Mallas

### <a name="drawing-commands"></a>Dibujar comandos

Para representar el contenido, se usan los métodos de dibujo del destino de representación. Antes de empezar a dibujar, se llama al método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Una vez finalizado el dibujo, se llama al método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre estas llamadas, se usan métodos Draw y Fill para representar recursos de dibujo. La mayoría de los métodos Draw y Fill toman una forma (una primitiva o una geometría) y un pincel para rellenar o esquematizar la forma.

Los destinos de representación proporcionan métodos para recortar, aplicar máscaras de opacidad y transformar el espacio de coordenadas.

Direct2D usa un sistema de coordenadas de la mano izquierda: los valores positivos del eje x pasan a los valores correctos y positivos del eje y continúan hacia abajo.

### <a name="error-handling"></a>Tratamiento de errores

Los comandos de dibujo de destino de representación no indican si la operación solicitada se realizó correctamente. Para averiguar si hay errores de dibujo, llame al método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) del destino de representación o al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obtener un **HRESULT**.

## <a name="example-render-content-to-a-window"></a>Ejemplo: representación de contenido en una ventana

En el ejemplo siguiente se usa el método [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) para crear un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


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



En el ejemplo siguiente se usa [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para dibujar texto en la ventana.


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



El código se ha omitido en este ejemplo.

 

 
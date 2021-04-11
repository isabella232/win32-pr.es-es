---
description: La frecuencia de actualización de variables indica que es necesario que se habilite el desactivado, lo que también se conoce como &\# 0034; VSYNC-off&\# 0034; soporte técnico.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Se muestra la frecuencia de actualización de variables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274684"
---
# <a name="variable-refresh-rate-displays"></a>Se muestra la frecuencia de actualización de variables

La frecuencia de *actualización de variables muestra requerir el* desactivado para habilitarla, lo que también se conoce como compatibilidad con "VSYNC".

-   [Frecuencia de actualización de variables muestra/VSYNC OFF](#variable-refresh-rate-displaysvsync-off)
-   [Temas relacionados](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Frecuencia de actualización de variables muestra/VSYNC OFF

La compatibilidad con las visualizaciones de frecuencia de actualización variable se logra estableciendo ciertas marcas al crear y presentar la cadena de intercambio.

Para usar esta característica, los usuarios de la aplicación deben estar en sistemas Windows 10 con [KB3156421](https://support.microsoft.com/kb/3156421) o la actualización de aniversario instalada. La característica funciona en todas las versiones de Direct3D 11 y 12 usando * efectos de *intercambio de DXGI \_ \_ \_ \_ \* Flip _ efecto* de intercambio.

Para agregar compatibilidad con la sincronización de VSYNC a las aplicaciones, puede consultar un ejemplo de ejecución completo de Direct3D 12, _ *D3D12Fullscreen** (consulte los [ejemplos de trabajo](../direct3d12/working-samples.md)). También hay algunos puntos que no se indican explícitamente en el código de ejemplo, pero tiene que prestar atención.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) debe tener la misma marca de creación de cadena de intercambio (el \_ marcador de cadena de intercambio de DXGI \_ permite el \_ \_ \_ recorte) que se le pasa como [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).
-   DXGI \_ present \_ permitir el \_ recorte solo se puede usar con el intervalo de sincronización 0. Se recomienda pasar siempre esta marca de interrupción al usar el intervalo de sincronización 0 si [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) informa de que se admite el desgarro *y* la aplicación está en un modo de ventana, incluido el modo de pantalla completa sin borde. Para más información, consulte las constantes de [**DXGI \_ presentes**](dxgi-present.md) .
-   Deshabilitar VSYNC no uncap necesariamente la velocidad de fotogramas: los desarrolladores también deben asegurarse de que las llamadas [**presentes**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) no estén limitadas por otros eventos de control de tiempo (como el `CompositionTarget::Rendering` evento en una aplicación basada en XAML).

El código siguiente recapitula algunas piezas clave que debe agregar a las aplicaciones.

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras en DXGI 1,5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 

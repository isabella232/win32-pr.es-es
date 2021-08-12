---
description: Las pantallas de frecuencia de actualización variable requieren que se habilite el desgarro, lo que también se conoce como compatibilidad con \# &0034;vsync-off&\# 0034;.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Se muestra la frecuencia de actualización variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288928"
---
# <a name="variable-refresh-rate-displays"></a>Se muestra la frecuencia de actualización variable

Las pantallas de *frecuencia* de actualización variable requieren que se habilite el desgarro, lo que también se conoce como compatibilidad con "vsync-off".

-   [Se muestra la frecuencia de actualización variable/Vsync desactivada](#variable-refresh-rate-displaysvsync-off)
-   [Temas relacionados](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Se muestra la frecuencia de actualización variable/Vsync desactivada

La compatibilidad con las pantallas de frecuencia de actualización variable se logra estableciendo ciertas marcas al crear y presentar la cadena de intercambio.

Para usar esta característica, los usuarios de la aplicación deben estar en Windows 10 con [KB3156421](https://support.microsoft.com/kb/3156421) o la actualización de aniversario instalada. La característica funciona en todas las versiones de Direct3D 11 y 12 mediante efectos de intercambio **\_ DXGI SWAP \_ EFFECT \_ FLIP. \_ \***

Para agregar compatibilidad con vsync-off a las aplicaciones, puede consultar un ejemplo completo de ejecución para Direct3D 12, **D3D12Fullscreen** (consulte Ejemplos de [trabajo).](../direct3d12/working-samples.md) También hay algunos puntos que no se han llamado explícitamente en el código de ejemplo, pero debe prestar atención.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1)**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)debe tener la misma marca de creación de cadena de intercambio (DXGI SWAP CHAIN FLAG ALLOW TEARING) pasada como \_ \_ \_ \_ \_ [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1).**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   DXGI \_ PRESENT \_ ALLOW \_ TEARING solo se puede usar con el intervalo de sincronización 0. Se recomienda pasar siempre esta marca de desmontaje cuando se usa el intervalo  de sincronización 0 si [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) informa de que se admite el desmontaje y la aplicación está en modo de ventana, incluido el modo de pantalla completa sin borde. Consulte las [**constantes PRESENT \_ de DXGI**](dxgi-present.md) para obtener más detalles.
-   Deshabilitar vsync no desencapsular necesariamente la velocidad de fotogramas: los desarrolladores también deben asegurarse de que present [**calls**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) are not throttled by other timing events (como el evento en una aplicación basada en `CompositionTarget::Rendering` XAML).

El código siguiente recapitulará algunas partes clave que debe agregar a las aplicaciones.

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

[Mejoras de DXGI 1.5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 

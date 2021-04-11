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
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="97375-103">Se muestra la frecuencia de actualización de variables</span><span class="sxs-lookup"><span data-stu-id="97375-103">Variable refresh rate displays</span></span>

<span data-ttu-id="97375-104">La frecuencia de *actualización de variables muestra requerir el* desactivado para habilitarla, lo que también se conoce como compatibilidad con "VSYNC".</span><span class="sxs-lookup"><span data-stu-id="97375-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="97375-105">Frecuencia de actualización de variables muestra/VSYNC OFF</span><span class="sxs-lookup"><span data-stu-id="97375-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="97375-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97375-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="97375-107">Frecuencia de actualización de variables muestra/VSYNC OFF</span><span class="sxs-lookup"><span data-stu-id="97375-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="97375-108">La compatibilidad con las visualizaciones de frecuencia de actualización variable se logra estableciendo ciertas marcas al crear y presentar la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="97375-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="97375-109">Para usar esta característica, los usuarios de la aplicación deben estar en sistemas Windows 10 con [KB3156421](https://support.microsoft.com/kb/3156421) o la actualización de aniversario instalada.</span><span class="sxs-lookup"><span data-stu-id="97375-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="97375-110">La característica funciona en todas las versiones de Direct3D 11 y 12 usando \* efectos de *intercambio de DXGI \_ \_ \_ \_ \* Flip _ efecto* de intercambio.</span><span class="sxs-lookup"><span data-stu-id="97375-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="97375-111">Para agregar compatibilidad con la sincronización de VSYNC a las aplicaciones, puede consultar un ejemplo de ejecución completo de Direct3D 12, _ *D3D12Fullscreen*\* (consulte los [ejemplos de trabajo](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="97375-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="97375-112">También hay algunos puntos que no se indican explícitamente en el código de ejemplo, pero tiene que prestar atención.</span><span class="sxs-lookup"><span data-stu-id="97375-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="97375-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (o [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) debe tener la misma marca de creación de cadena de intercambio (el \_ marcador de cadena de intercambio de DXGI \_ permite el \_ \_ \_ recorte) que se le pasa como [**presente**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (o [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span><span class="sxs-lookup"><span data-stu-id="97375-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="97375-114">DXGI \_ present \_ permitir el \_ recorte solo se puede usar con el intervalo de sincronización 0.</span><span class="sxs-lookup"><span data-stu-id="97375-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="97375-115">Se recomienda pasar siempre esta marca de interrupción al usar el intervalo de sincronización 0 si [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) informa de que se admite el desgarro *y* la aplicación está en un modo de ventana, incluido el modo de pantalla completa sin borde.</span><span class="sxs-lookup"><span data-stu-id="97375-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="97375-116">Para más información, consulte las constantes de [**DXGI \_ presentes**](dxgi-present.md) .</span><span class="sxs-lookup"><span data-stu-id="97375-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="97375-117">Deshabilitar VSYNC no uncap necesariamente la velocidad de fotogramas: los desarrolladores también deben asegurarse de que las llamadas [**presentes**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) no estén limitadas por otros eventos de control de tiempo (como el `CompositionTarget::Rendering` evento en una aplicación basada en XAML).</span><span class="sxs-lookup"><span data-stu-id="97375-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="97375-118">El código siguiente recapitula algunas piezas clave que debe agregar a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="97375-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="97375-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97375-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97375-120">Mejoras en DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="97375-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="97375-121">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="97375-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 

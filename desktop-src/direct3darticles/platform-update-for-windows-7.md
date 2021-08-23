---
title: Actualización de plataforma para Windows 7
description: En este tema se describen las mejoras en los componentes de la pila de gráficos Windows 7 que están disponibles a través de la actualización de plataforma para Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a577d74613a22a176c038b6c85e53b94f413edbc49d07a886a613ddff5a83b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627585"
---
# <a name="platform-update-for-windows-7"></a>Actualización de plataforma para Windows 7

En este tema se describen las mejoras en los componentes de la pila de gráficos Windows 7 que están disponibles a través de la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838).

Cuando se instala en Windows 7, la actualización de plataforma para Windows 7 se actualiza Windows 7 con funcionalidad disponible en Windows 8. Por ejemplo, estos componentes Windows 8 están disponibles con funcionalidad completa:

-   Direct2D 1.1 (incluidos los efectos de Direct2D)
-   DirectWrite
-   Windows Imaging Component (WIC)

Proporcionan funcionalidad parcial:

-   Direct3D 11.1
-   DXGI 1.2

Y, por ejemplo, este componente no está disponible:

-   DirectComposition (DComp)

Consulte estos temas para obtener información sobre Direct2D, DirectWrite y WIC con la actualización de la plataforma:

-   [Novedades de Direct2D para Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Novedades de DirectWrite para Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Novedades de WIC en Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Consulte estos temas para obtener información sobre Direct3D y DXGI con la actualización de la plataforma:

-   [Características de D3D11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Mejoras de DXGI 1.2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Una vez instalada la actualización de la plataforma, las interfaces introducidas en Direct3D11.1 y DXGI 1.2 estarán disponibles con funcionalidad parcial. Las características de estos componentes gráficos están vinculadas directamente a los componentes del kernel de gráficos, los controladores de gráficos y el hardware gráfico. Antes de usar Direct3D11.1 en Windows 7, familiarícese con estos detalles:

-   Windows 8 el modelo de controlador WDDM 1.2, que proporciona mejoras en toda la superficie de API asociada para todos los niveles [de características.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Al leer la documentación de Direct3D11.1, comprenda que los nuevos *controladores* significan controladores WDDM 1.2. Estas versiones actualizadas del controlador, así como la mayoría de las características opcionales expuestas a través de [**CheckFeatureSupport,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)no están disponibles en Windows 7. Puesto que no hay ninguna garantía de que estas características opcionales estén disponibles, asegúrese de que las aplicaciones tienen los comportamientos de reserva adecuados en caso de que la funcionalidad deseada no esté disponible.

    Hay una excepción importante. Varias características, como [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) con desplazamientos de búfer constantes, requieren nuevos controladores para el nivel [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) característica 10 y superior, pero en realidad se emulan para el nivel de característica 9. Esta emulación está disponible en Windows 7 con la actualización de la plataforma. Consulte [**D3D11 FEATURE DATA D3D11 OPTIONS (OPCIONES DE \_ \_ D3D11 FEATURE DATA \_ D3D11) \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) para obtener más información sobre qué características se emulan.

-   El Windows 8 modelo de controlador WDDM 1.2 admite una nueva generación de hardware, expuesta a través del nivel [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) característica D3D 11.1. Windows 7 con la actualización de la plataforma solo admite el modelo de controlador WDDM 1.1 y, por lo tanto, la compatibilidad con hardware de nivel de característica 11.1 no está disponible (a través de la actualización de la plataforma). En Windows 7 con la actualización de la plataforma, [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) siempre devuelve un nivel de característica de 11.0 o inferior, excepto con un dispositivo de referencia que se puede usar para probar una ruta de acceso de código 11.1 en Windows 7. Use solo las características disponibles en los niveles de características de destino, como se describe en la referencia de nivel de característica.
-   Algunos métodos nuevos introducidos en DGXI 1.2 no son totalmente compatibles con la actualización de plataforma para Windows 7. Puede probar la disponibilidad de estas funciones llamándolos directamente y comprobando un código de error. Asegúrese de que las aplicaciones que tienen como destino Windows 7 con la actualización de la plataforma tienen una reserva cuando la funcionalidad deseada no está disponible. Estas clases de características no están disponibles en La actualización de plataforma para Windows 7:

    -   Estéreo
    -   Cadenas de intercambio que no tienen como destino Hwnds
    -   Notificaciones de estado de oclusión
    -   Duplicación de escritorio
    -   Recursos de nt handle

    En concreto, las siguientes API devolverán DXGI \_ ERROR \_ UNSUPPORTED, DXGI \_ ERROR INVALID \_ \_ CALL, E \_ NOTIMPL o E \_ INVALIDARG:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Estas API tienen diferencias de comportamiento, como se indicó:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) toma una estructura [**DXGI \_ SWAP CHAIN \_ \_ DESC1,**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) que tiene un campo para **Escalar**. [**DXGI \_ SCALING \_ NONE no**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) se admite en Windows 7 con la actualización de la plataforma y hace que **CreateSwapChainForHwnd** devuelva DXGI ERROR INVALID CALL cuando se llama \_ a \_ \_ .
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) solo es útil cuando se establece en una cadena de intercambio mediante DXGI \_ SCALING \_ NONE. Su valor todavía se almacena y se puede recuperar, pero no tiene ningún efecto.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)e [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) **devuelven FALSE.**
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) se agregaron para facilitar los modos de presentación estéreo. Estéreo no se admite en la actualización de plataforma para Windows 7, por lo que este método es equivalente a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) como [**DXGI \_ MODE \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Estéreo siempre será FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) no se admiten en la actualización de plataforma para Windows 7. Sin embargo, el tiempo de ejecución todavía permite llamarlos y realiza la validación de que se usan correctamente en recursos no compartidos.
    -   [Los dispositivos WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) solo [admiten el nivel](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de característica 11.0. Es decir, los dispositivos WARP creados al pasar [D3D \_ DRIVER \_ TYPE \_ WARP](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) no admiten 11.1 ni admiten superficies compartidas.
-   Para los desarrolladores que trabajan actualmente en aplicaciones de Microsoft Visual Studio 2010 o versiones anteriores mediante la marca [**\_ CREATE DEVICE \_ \_ DEBUG de D3D11,**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) tenga en cuenta que se producirá un error en las llamadas a [**D3D11CreateDevice.**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) Esto se debe a que el entorno de ejecución D3D11.1 ahora requiere D3D11 \_1SDKLayers.dll en lugar de D3D11SDKLayers.dll. Para obtener este nuevo archivo DLL (D3D111SDKLayers.dll), instale el \_ [SDK](https://dev.windows.com/downloads/windows-8-sdk)de Windows 8 o [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)o las herramientas de depuración remota de Visual Studio 2012. Consulte la documentación [de la capa](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) de depuración para obtener más información.

 

 
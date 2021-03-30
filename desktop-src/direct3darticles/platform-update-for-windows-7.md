---
title: Actualización de la plataforma para Windows 7
description: En este tema se describen las mejoras de los componentes de la pila de gráficos de Windows 7 que están disponibles a través de la actualización de la plataforma para Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904773"
---
# <a name="platform-update-for-windows-7"></a>Actualización de la plataforma para Windows 7

En este tema se describen las mejoras de los componentes de la pila de gráficos de Windows 7 que están disponibles a través de la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838).

Cuando se instala en Windows 7, la actualización de la plataforma para Windows 7 actualiza Windows 7 con funcionalidad disponible en Windows 8. Por ejemplo, estos componentes de Windows 8 están disponibles con funcionalidad completa:

-   Direct2D 1,1 (incluidos los efectos de Direct2D)
-   DirectWrite
-   Windows Imaging Component (WIC)

Proporcionan funcionalidad parcial:

-   Direct3D 11,1
-   DXGI 1,2

Y, por ejemplo, este componente no está disponible:

-   DirectComposition (DComp)

Vea estos temas para obtener información sobre Direct2D, DirectWrite y WIC con la actualización de la plataforma:

-   [Novedades de Direct2D para Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Novedades de DirectWrite para Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Novedades de WIC en Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Vea estos temas para obtener información sobre Direct3D y DXGI con la actualización de la plataforma:

-   [Características D3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Mejoras en DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Una vez instalada la actualización de la plataforma, las interfaces introducidas en Direct3D 11.1 y DXGI 1,2 estarán disponibles con funcionalidad parcial. Las características de estos componentes gráficos están asociadas directamente a los componentes del kernel de gráficos, los controladores de gráficos y el hardware de gráficos. Antes de usar Direct3D 11.1 en Windows 7, familiarícese con estas características específicas:

-   Windows 8 presentó el modelo de controlador WDDM 1,2, que ofrecía mejoras en la superficie de API asociada para todos los [niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). Al leer la documentación de Direct3D 11.1, comprenda que los *nuevos controladores* significan controladores WDDM 1,2. Estas versiones actualizadas del controlador, así como la mayoría de las características opcionales que se exponen a través de [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), no están disponibles en Windows 7. Dado que no hay ninguna garantía de que estas características opcionales estén disponibles, asegúrese de que las aplicaciones tienen los comportamientos de reserva adecuados en caso de que la funcionalidad deseada no esté disponible.

    Hay una excepción importante. Varias características, como [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) con desplazamientos de búfer constantes, requieren nuevos controladores para el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 y versiones posteriores, pero se emulan realmente para el nivel de característica 9. Esta emulación está disponible en Windows 7 con la actualización de la plataforma. Consulte [**\_ Opciones de \_ \_ D3D11 \_ de datos de características de D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) para obtener más información sobre qué características se emulan.

-   El modelo de controladores de Windows 8 WDDM 1,2 admite una nueva generación de hardware, expuesta a través del [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de D3D 11,1. Windows 7 con la actualización de la plataforma solo admite el modelo de controlador WDDM 1,1 y, por lo tanto, no está disponible la compatibilidad de hardware de nivel de característica 11,1 (a través de la actualización de la plataforma). En Windows 7 con la actualización de la plataforma, [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) siempre devuelve un nivel de característica de 11,0 o inferior, a excepción de con un dispositivo de referencia que se puede usar para probar una ruta de acceso de código 11,1 en Windows 7. Use solo las características disponibles en los niveles de características de destino, como se describe en la referencia de nivel de característica.
-   Algunos de los nuevos métodos introducidos en DGXI 1,2 no son totalmente compatibles con la actualización de la plataforma para Windows 7. para probar la disponibilidad de estas funciones, puede llamarlas directamente y comprobar si hay un código de error. Asegúrese de que las aplicaciones que tienen como destino Windows 7 con la actualización de la plataforma tienen una reserva en contexto cuando la funcionalidad deseada no está disponible. Estas clases de características no están disponibles en la actualización de la plataforma para Windows 7:

    -   Estéreo
    -   Intercambio no tiene como destino HWND
    -   Notificaciones de estado de oclusión
    -   Duplicación de escritorio
    -   Administrar recursos de NT

    En concreto, las siguientes API devolverán un error de DXGI \_ \_ no compatible, error de dxgi \_ \_ llamada no válida \_ , e \_ NOTIMPL o e \_ INVALIDARG:

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

-   Estas API tienen diferencias de comportamiento, como se indica a continuación:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) toma una estructura DESC1 de la cadena de intercambio de DXGI, que tiene un campo para el **escalado**. [**\_ \_ \_**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) [**DXGI \_ No \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) se admite el escalado de ninguno en Windows 7 con la actualización de la plataforma y hace que **CreateSwapChainForHwnd** devuelva una \_ \_ llamada no válida de DXGI cuando se \_ llama.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) solo es útil cuando se establece en un intercambio con el \_ escalado de DXGI \_ ninguno. Su valor todavía se almacena y se puede recuperar, pero no tiene ningún efecto.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)y [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) devuelven **false**.
    -   Se han agregado [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) y **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) para facilitar los modos de visualización estéreo. No se admite el estéreo en la actualización de la plataforma para Windows 7, por lo que este método es equivalente a [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) como [**\_ \_ DESC1 de modo DXGI**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). El estéreo siempre será FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) y **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) no se admiten en la actualización de la plataforma para Windows 7. Sin embargo, el tiempo de ejecución sigue permitiendo que se llamen y realiza la validación de que se usan correctamente en recursos no compartidos.
    -   Los dispositivos [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) solo admiten el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Es decir, los dispositivos de ALABEo creados al pasar el [ \_ tipo de controlador D3D \_ \_ Warp](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) no admiten 11,1 ni admiten superficies compartidas.
-   Para los desarrolladores que trabajan actualmente en aplicaciones en Microsoft Visual Studio 2010 o una versión anterior con la marca de [**\_ \_ \_ depuración crear dispositivo de D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) , tenga en cuenta que se producirá un error en las llamadas a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) . Esto se debe a que el tiempo de ejecución de D3D 11.1 requiere ahora D3D11 \_1SDKLayers.dll en lugar de D3D11SDKLayers.dll. Para obtener este nuevo archivo DLL (D3D11 \_1SDKLayers.dll), instale el [SDK de Windows 8](https://dev.windows.com/downloads/windows-8-sdk)o [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads), o las herramientas de depuración remota de Visual Studio 2012. Consulte la documentación de la [capa de depuración](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) para obtener más información.

 

 
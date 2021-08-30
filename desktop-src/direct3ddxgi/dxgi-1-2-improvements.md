---
description: Se ha agregado la siguiente funcionalidad en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.2.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: Mejoras de DXGI 1.2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f1903ca75615a887295a856bb5804c6d8f17d150ae41258ec9438fdb95196b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025625"
---
# <a name="dxgi-12-improvements"></a>Mejoras de DXGI 1.2

Se ha agregado la siguiente funcionalidad en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.2.

## <a name="presentation-enhancements-and-optimizations"></a>Mejoras y optimizaciones de presentación

DXGI 1.2 mejora la presentación con una nueva cadena de intercambio de modelos de volteo, protección de contenido, presentación sin ventanas y presentación optimizada en la que se especifican rectángulos y áreas desplazadas desaprobados. La presentación también se ha mejorado con el comportamiento de presentación 3D estereo estéreo.

Puede usar la siguiente API de DXGI 1.2 para mejorar la presentación.

-   [**IDXGIDisplayControl::IsStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**IDXGIDisplayControl::SetStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1::CreateSubresourceSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2::GetResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1::GetFullscreenDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1::GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1::GetCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1::IsTemporaryMonoSupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1::GetRestrictToOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1::SetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1::GetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Para obtener más información sobre cómo usar la API de DXGI 1.2 para una presentación mejorada, vea Mejorar la presentación con el modelo de volteo, rectángulos desgajes y áreas [desplazadas.](dxgi-1-2-presentation-improvements.md)

Para obtener información sobre cómo determinar si se puede representar en estéreo, vea Representación en estéreo y notificación [sobre el estado estéreo.](stereo-rendering-stereo-status-notifying.md)

Para obtener información sobre cómo determinar los cambios en el estado de oclusión de la aplicación, consulte [Waiting on an event when rendering is unnecessary](waiting-when-occluded.md)(Esperando un evento cuando la representación no es necesaria).

Para obtener información sobre cómo cambian los valores de datos al presentar contenido en la pantalla, consulte Conversión de [datos para el espacio de colores.](converting-data-color-space.md)

## <a name="desktop-duplication"></a>Duplicación de escritorio

Windows 8 deshabilita los controladores reflejados Windows modelo de controlador de pantalla (XDDM) de 2000. DXGI 1.2 proporciona la API de duplicación de escritorio como alternativa. La API de duplicación de escritorio proporciona acceso remoto a la imagen de escritorio para escenarios de colaboración.

La API de duplicación de escritorio consta de los métodos siguientes.

-   [**IDXGIOutput1::D uplicateOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**IDXGIOutputDuplication::GetDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**IDXGIOutputDuplication::MapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**IDXGIOutputDuplication::UnMapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**IDXGIOutputDuplication::ReleaseFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Para obtener más información sobre cómo usar la API de duplicación de escritorio, consulte [API de duplicación de escritorio.](desktop-dup-api.md)

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Uso mejorado de recursos compartidos y eventos sincronizados

En versiones anteriores de Windows, las aplicaciones usan el sondeo continuo para determinar si la unidad de procesamiento gráfico (GPU) ha terminado de procesar comandos arbitrarios. DXGI 1.2 permite a una aplicación poner en cola un evento en un dispositivo DXGI. Después, la aplicación puede esperar a que el dispositivo DXGI señale el evento para determinar que la GPU ha terminado de ejecutar todos los comandos de representación. DXGI 1.2 permite que varios dispositivos compartan un recurso a través de un identificador nt.

Puede usar la siguiente API dxgi 1.2 y la API de Direct3D 11.1 para compartir recursos y sincronizar eventos.

-   [**IDXGIDevice2::EnqueueSetEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1::CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2::GetSharedResourceAdapterLuid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1::OpenSharedResourceByName**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ RESOURCE \_ MISC \_ SHARED \_ NTHANDLE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Ofrecer la memoria de vídeo de los recursos

DXGI 1.2 permite que una aplicación ofrezca la memoria de vídeo de sus recursos con poca sobrecarga. Al ofrecer la memoria de vídeo, el sistema operativo puede liberar la memoria de vídeo.

Esta característica dxgi 1.2 consta de los métodos siguientes.

-   [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

Puede usar el método [**ID3D11Debug::SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) para establecer marcas de máscara de características que depuran el comportamiento de los métodos [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) en la aplicación.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>Adelantamiento de GPU en niveles de granularidad más finos para el modelo de controlador WDDM 1.2

A partir del modelo de controlador Windows Display Driver Model (WDDM) 1.2, el programador wddm puede adelantar la ejecución de la GPU de las tareas de aplicación en niveles de granularidad más finos. DXGI 1.2 permite determinar los niveles de granularidad de adelantamiento de GPU.

Esta característica DXGI 1.2 consta del método siguiente.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>Depuración de API

El SDK Windows 8 proporciona funcionalidad de depuración adicional. Puede usar las siguientes API de DXGI desde Dxgidebug.dll para depurar la aplicación:

-   [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Para acceder [**a DXGIGetDebugInterface,**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)llame a la función [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obtener Dxgidebug.dll y la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener la dirección de **DXGIGetDebugInterface**. A continuación, puede **llamar a DXGIGetDebugInterface** para obtener la [**interfaz IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) [**o IDXGIInfoQueue.**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Para obtener información sobre cómo depurar aplicaciones directX de forma remota, consulte Depuración remota de [aplicaciones DirectX.](../direct3dtools/debugging-directx-apps-remotely.md)

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

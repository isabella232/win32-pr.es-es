---
description: La funcionalidad siguiente se ha agregado o cambiado en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.4, en gran medida para admitir Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Mejoras de DXGI 1.4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef5777f50a149da6ccb2893bcac8a8f509c86cdff40d94889155c2e5e1eb12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289559"
---
# <a name="dxgi-14-improvements"></a>Mejoras de DXGI 1.4

La funcionalidad siguiente se ha agregado o cambiado en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.4, en gran medida para admitir Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Enumeración de adaptador más económica

Para Direct3D 12, ya no es posible retroceder desde un dispositivo al [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que se usó para crearlo. Tampoco es posible proporcionar el tipo de controlador D3D \_ \_ WARP en \_ [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Para facilitar el desarrollo, puede usar [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) para tratar ambos. [**IDXGIFactory4::EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (diseñado para emparejarse con [**ID3D12Device::GetAdapterLuid)**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)permite a una aplicación recuperar información sobre el adaptador donde se creó un dispositivo Direct3D 12. [**IDXGIFactory4::EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) proporciona un adaptador que se puede proporcionar a **D3D12CreateDevice** para usar el representador WARP.

## <a name="video-memory-budget-tracking"></a>Seguimiento del presupuesto de memoria de vídeo

Se recomienda a los desarrolladores de aplicaciones que usen un sistema de reserva de memoria de vídeo para informar al sistema operativo de la cantidad de memoria de vídeo física que la aplicación no puede perder.

La cantidad de memoria física disponible para un proceso se conoce como "presupuesto de memoria de vídeo". El presupuesto puede fluctuar notablemente a medida que el fondo procesa la reactivación y la suspensión. y fluctúan drásticamente cuando el usuario cambia a otra aplicación. Se puede notificar a la aplicación cuando cambia el presupuesto y sondear tanto el presupuesto actual como la cantidad de memoria consumida actualmente. Si una aplicación no permanece dentro de su presupuesto, el proceso se inmovilizará intermitentemente para permitir que otras aplicaciones se ejecuten o las API de creación devolverán errores. La [**interfaz IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) proporciona los métodos que pertenecen a esta funcionalidad, en particular [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) y [**RegisterVideoMemoryBudgetChangeNotificationEvent.**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)

Para obtener más información, consulte el tema de Direct3D 12 en [Residencia.](../direct3d12/residency.md)

## <a name="direct3d-12-swapchain-changes"></a>Cambios en la cadena de intercambio de Direct3D 12

Algunas de las funcionalidades existentes de la cadena de intercambio de Direct3D 11 han quedado en desuso para lograr las reducciones de sobrecarga en Direct3D 12. Mientras que se realizaron otros cambios para alinearse con los conceptos de Direct3D 12 o proporcionar una mejor compatibilidad con las características de Direct3D 12.

**Identidad invariable del búfer de seguridad**

En Direct3D 11, las aplicaciones podrían llamar [**a GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)( 0, ... ) solo una vez. Cada llamada a [**Present cambió**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) implícitamente la identidad de recurso de la interfaz devuelta. Direct3D 12 ya no admite ese cambio implícito de identidad de recursos, debido a la sobrecarga de CPU necesaria y al diseño flexible del descriptor de recursos. Como resultado, la aplicación debe llamar manualmente a **GetBuffer** para cada búfer creado con la cadena de intercambio. La aplicación debe representarse manualmente en el siguiente búfer de la secuencia después de llamar a **Present**. Se recomienda a las aplicaciones crear una caché de descriptores para cada búfer, en lugar de volver a crear muchos objetos cada **presente.**

**Compatibilidad con varios adaptadores**

Cuando se crea una cadena de intercambio en un adaptador de varias GPU, todos los búferes de reserva se crean en el nodo 1 y solo se admite una cola de comandos única. [**ResizeBuffers1 permite**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) a las aplicaciones crear búferes de reserva en nodos diferentes, lo que permite usar una cola de comandos diferente con cada uno. Estas funcionalidades permiten usar técnicas de representación de fotogramas alternativos (AFR) con la cadena de intercambio. Consulte [Sistemas de varios adaptadores.](../direct3d12/multi-engine.md)

**Varios**

-   Se debe pasar un objeto de cola de comandos a [**los métodos CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) en lugar del objeto de dispositivo Direct3D 12.
-   Solo se admiten los dos efectos de intercambio de modelos de volteo siguientes: <dl> Se debe preferar DXGI SWAP EFFECT FLIP DISCARD cuando las aplicaciones se representen completamente sobre el búfer de reserva antes de presentarlo o estén interesadas en admitir escenarios de varios adaptadores \_ \_ \_ \_ fácilmente.  
    DXGI SWAP EFFECT FLIP SEQUENTIAL debe usarse en aplicaciones que se basan en optimizaciones de presentación parciales o que se leen regularmente de los búferes de \_ \_ reserva \_ \_ presentados anteriormente.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Temas relacionados

[Niveles de características de hardware de Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

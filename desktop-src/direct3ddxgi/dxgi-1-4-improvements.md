---
description: La siguiente funcionalidad se ha agregado o cambiado en Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, en gran medida para admitir Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Mejoras en DXGI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e9a8a48dd026248afac7c1a7df23a99176adef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079927"
---
# <a name="dxgi-14-improvements"></a>Mejoras en DXGI 1,4

La siguiente funcionalidad se ha agregado o cambiado en Microsoft DirectX Graphics Infrastructure (DXGI) 1,4, en gran medida para admitir Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Enumeración de adaptadores más barata

Para Direct3D 12, ya no es posible retroceder desde un dispositivo a la [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que se usó para crearlo. Además, ya no es posible proporcionar el \_ tipo de controlador D3D \_ \_ Warp en [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Para facilitar el desarrollo, puede usar [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) para tratar ambos. [**IDXGIFactory4:: EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (diseñado para emparejarse con [**ID3D12Device:: GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)) permite que una aplicación recupere información sobre el adaptador en el que se creó un dispositivo de Direct3D 12. [**IDXGIFactory4:: EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) proporciona un adaptador que se puede proporcionar a **D3D12CreateDevice** para usar el REpresentador de alabeo.

## <a name="video-memory-budget-tracking"></a>Seguimiento de presupuesto de memoria de vídeo

Se recomienda a los desarrolladores de aplicaciones que usen un sistema de reserva de memoria de vídeo para informar al sistema operativo de la cantidad de memoria de vídeo física que no puede tener la aplicación.

La cantidad de memoria física disponible para un proceso se conoce como el "presupuesto de memoria de vídeo". El presupuesto puede fluctuar notablemente a medida que los procesos en segundo plano se reactivan y suspenden. y fluctúan drásticamente cuando el usuario cambia a otra aplicación. Se puede notificar a la aplicación cuando el presupuesto cambie y sondee el presupuesto actual y la cantidad de memoria consumida actualmente. Si una aplicación no se mantiene dentro de su presupuesto, el proceso se inmovilizará intermitentemente para permitir que se ejecuten otras aplicaciones y/o las API de creación devolverán un error. La interfaz [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) proporciona los métodos que pertenecen a esta funcionalidad, en particular [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) y [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Para obtener más información, consulte el tema Direct3D 12 en [residencia](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Cambios de intercambio de Direct3D 12

Parte de la funcionalidad de intercambio de Direct3D 11 existente quedó en desuso para lograr las reducciones de sobrecarga en Direct3D 12. Mientras que otros cambios se realizaron en alinearse con los conceptos de Direct3D 12 o proporcionar una mejor compatibilidad para las características de Direct3D 12.

**Identidad de búfer de reserva invariable**

En Direct3D 11, las aplicaciones pueden llamar a [**getBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)(0,... ) una sola vez. Cada llamada a [**presente**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) ha cambiado implícitamente la identidad del recurso de la interfaz devuelta. Direct3D 12 ya no admite ese cambio de identidad de recursos implícito, debido a la sobrecarga de CPU necesaria y al diseño flexible del descriptor de recursos. Como resultado, la aplicación debe llamar manualmente a **getBuffer** para cada búfer creado con el intercambio. La aplicación debe representarse manualmente en el siguiente búfer de la secuencia después de llamar a **present**. Se recomienda que las aplicaciones creen una memoria caché de descriptores para cada búfer, en lugar de volver a crear muchos **objetos.**

**Compatibilidad con varios adaptadores**

Cuando se crea un intercambio en un adaptador de varias GPU, los búferes de reserva se crean en el nodo 1 y solo se admite una única cola de comandos. [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) permite a las aplicaciones crear búferes de reserva en nodos diferentes, lo que permite usar una cola de comandos diferente con cada uno. Estas funcionalidades permiten usar técnicas de representación de tramas alternativas (AFR) con intercambio. Consulte [sistemas de varios adaptadores](../direct3d12/multi-engine.md).

**Varios**

-   Un objeto de cola de comandos debe pasarse a métodos [**CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) en lugar del objeto de dispositivo Direct3D 12.
-   Solo se admiten los dos efectos de intercambio de modelo Flip siguientes: <dl> El \_ efecto de intercambio de DXGI \_ \_ \_ debe ser preferible cuando las aplicaciones se representan por completo en el búfer antes de presentarlos o están interesados en admitir los escenarios de varios adaptadores con facilidad.  
    La \_ \_ volteo del efecto de intercambio \_ de DXGI \_ debe usarse en las aplicaciones que dependen de las optimizaciones de presentación parciales o que se leen periódicamente de búferes de reserva previamente presentados.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Temas relacionados

[Niveles de características de hardware de Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

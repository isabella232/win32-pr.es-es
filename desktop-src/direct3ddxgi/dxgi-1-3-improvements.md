---
description: Se ha agregado la siguiente funcionalidad en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.3, que se incluye a partir de Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Mejoras de DXGI 1.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709dc9e98ffe6ecd67f6bd91aa654b1e0bfe0375dabcd2a344f5b012c57dca2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984125"
---
# <a name="dxgi-13-improvements"></a>Mejoras de DXGI 1.3

Se ha agregado la siguiente funcionalidad en Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.3, que se incluye a partir de Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Recorte del uso de memoria del adaptador DXGI

A partir Windows 8.1, DXGI 1.3 agrega la capacidad de vaciar y liberar los recursos de memoria no usados asignados por el adaptador de DXGI. Esto permite que las aplicaciones liberen memoria temporal mientras se suspenden, lo que reduce la posibilidad de que la aplicación finalice para liberar recursos para otras aplicaciones. Cuando se reanuda la aplicación, los controladores de dispositivo que admiten recortes volverán a crear los recursos cuando sean necesarios. A partir de Windows 8.1, todos los dispositivos Direct3D creados por una aplicación deben llamar a [**IDXGIDevice3::Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) al suspender para reducir la superficie de memoria y reducir la posibilidad de que la aplicación finalice para reclamar recursos del sistema.

## <a name="multi-plane-overlays"></a>Superposiciones de varios plano

A partir Windows 8.1, DXGI 1.3 admite superposiciones de varios plano. Puede averiguar si el dispositivo admite superposiciones de varios plano en hardware mediante [**IDXGIOutput2::SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Superposición de cadenas de intercambio y escalado de cadenas de intercambio

A partir Windows 8.1, DXGI 1.3 admite cadenas de intercambio superpuestas. Las cadenas de intercambio superpuestas se usan para dibujar gráficos 3D en resoluciones no nativas (con escalado de hardware) mientras se presenta la interfaz de usuario a resolución nativa. Esto permite que los juegos aprovechen las mayores tasas de relleno para el juego dinámico sin degradar la calidad visual de los elementos de la interfaz de usuario, como la puntuación del jugador y el texto del diálogo. En los dispositivos que admiten superposiciones de varios planos, Direct3D usará superposiciones de varios plano para las cadenas de intercambio superpuestas. Cree una cadena de intercambio de primer plano especificando la marca [**DXGI \_ SWAP CHAIN FLAG FOREGROUND \_ \_ \_ \_ LAYER**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) al crear la cadena de intercambio y use [**IDXGISwapChain2::SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) e [**IDXGISwapChain2::GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) para escalar la cadena de intercambio usada para el juego.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Selección de la subregión backbuffer para la cadena de intercambio

A partir de Windows 8.1, DXGI 1.3 se puede usar para seleccionar una subregión del búfer de reserva para su uso con la cadena de intercambio, lo que permite representar en un búfer de reserva más pequeño sin volver a crear la cadena de intercambio. Vea [**IDXGISwapChain2::SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) e [**IDXGISwapChain2::GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Presentación de la cadena de intercambio de latencia inferior

A partir de Windows 8.1, DXGI 1.3 permite reducir la latencia al permitir que la cadena de intercambio termine de presentar el fotograma anterior antes de empezar a usar el dispositivo para dibujar el fotograma siguiente. Vea [**IDXGISwapChain2::GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2::GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)e [**IDXGISwapChain2::SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

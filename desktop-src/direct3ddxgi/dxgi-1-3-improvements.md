---
description: La siguiente funcionalidad se ha agregado en Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, que se incluye a partir de Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Mejoras en DXGI 1,3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c863bc30ffdf27705492b56a5348040c8e12f4fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906480"
---
# <a name="dxgi-13-improvements"></a>Mejoras en DXGI 1,3

La siguiente funcionalidad se ha agregado en Microsoft DirectX Graphics Infrastructure (DXGI) 1,3, que se incluye a partir de Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Trim el uso de memoria del adaptador de DXGI

A partir de Windows 8.1, DXGI 1,3 agrega la capacidad de vaciar y liberar los recursos de memoria no usados asignados por el adaptador de DXGI. Esto permite que las aplicaciones liberen memoria temporal mientras se suspenden, lo que reduce la posibilidad de que se termine la aplicación para liberar recursos para otras aplicaciones. Cuando se reanuda la aplicación, los controladores de dispositivos que admiten Trim volverán a crear los recursos a medida que se necesiten. A partir de Windows 8.1, todos los dispositivos de Direct3D creados por una aplicación deben llamar a [**IDXGIDevice3:: Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) al suspender para reducir la superficie de memoria y reducir la posibilidad de que la aplicación se termine para recuperar los recursos del sistema.

## <a name="multi-plane-overlays"></a>Superposiciones de varios planos

A partir de Windows 8.1, DXGI 1,3 admite superposiciones de varios planos. Puede averiguar si el dispositivo admite superposiciones de varios planos en hardware mediante [**IDXGIOutput2:: SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Cadenas de intercambio superpuestas y escalado de cadenas de intercambio

A partir de Windows 8.1, DXGI 1,3 admite la superposición de cadenas de intercambio. Las cadenas de intercambio superpuestas se usan para dibujar gráficos 3D en resoluciones no nativas (con escalado de hardware) mientras se presenta la interfaz de usuario en la resolución nativa. Esto permite que los juegos aprovechen las mejores tasas de relleno para el juego con capacidad de respuesta sin degradar la calidad visual de los elementos de la interfaz de usuario, como la puntuación del jugador y el texto del cuadro de diálogo. En los dispositivos que admiten superposiciones de varios planos, Direct3D usará superposiciones de varios planos para la superposición de cadenas de intercambio. Cree una cadena de intercambio en primer plano especificando el indicador de [**\_ \_ \_ \_ \_ nivel de primer plano**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) de la cadena de intercambio de DXGI al crear la cadena de intercambio y use [**IDXGISwapChain2:: SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) y [**IDXGISwapChain2:: GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) para escalar la cadena de intercambio utilizada para el juego.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Seleccionar subregión de búfer de reserva para la cadena de intercambio

A partir de Windows 8.1, se puede usar DXGI 1,3 para seleccionar una subregión del búfer de reserva para su uso con la cadena de intercambio, lo que hace posible que se represente en un búfer de reserva menor sin volver a crear la cadena de intercambio. Vea [**IDXGISwapChain2:: SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) y [**IDXGISwapChain2:: GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Presentación de la cadena de intercambio de menor latencia

A partir de Windows 8.1, DXGI 1,3 permite reducir la latencia al dejar que la cadena de intercambio termine de presentar el fotograma anterior antes de empezar a usar el dispositivo para dibujar el siguiente fotograma. Vea [**IDXGISwapChain2:: GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2:: GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)y [**IDXGISwapChain2:: SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)

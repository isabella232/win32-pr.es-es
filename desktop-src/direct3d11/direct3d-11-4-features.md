---
title: Características de Direct3D 11,4
description: En Direct3D 11,4 se ha agregado la siguiente funcionalidad.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995413"
---
# <a name="direct3d-114-features"></a>Características de Direct3D 11,4

En Direct3D 11,4 se ha agregado la siguiente funcionalidad.

Vea también [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Eliminación de dispositivos Direct3D

Los métodos [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)y [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) se admiten en una nueva interfaz, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), para admitir la recepción de una notificación de eventos asincrónicos cuando se ha quitado un dispositivo Direct3D.

## <a name="multithreaded-protection"></a>Protección multiproceso

Para asegurarse de que los comandos de gráficos en particular se ejecutan en un orden específico, la interfaz [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) tiene métodos para activar y desactivar la protección de multiproceso, y métodos para escribir y dejar código crítico que requiera esta protección.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Barreras para la interoperabilidad y la sincronización de varios dispositivos con Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) y [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) proporcionan la misma funcionalidad de barrera que Direct3D 12 para Direct3D 11. Las barreras se usan para sincronizar varios dispositivos Direct3D 11 y para la interoperabilidad entre Direct3D 11 y Direct3D 12. Se admiten las barreras en Windows 10 Creators Update.

## <a name="extended-nv12-texture-support"></a>Compatibilidad con textura NV12 extendida

Las texturas de NV12 con capacidades de captura y de vídeo admiten ahora el uso compartido. Las marcas de textura D3D11 anteriores para la captura y la codificación de vídeo están desusadas para NV12, ya que se establecerán todo el tiempo para los nuevos controladores. Estas texturas se pueden compartir no solo con D3D11, sino también con D3D12. En D3D12, ninguna marca nueva representa estas funciones de textura.

Consulte el valor booleano en [**D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Almacenamiento en caché del sombreador

Los controladores pueden admitir el almacenamiento en caché del sombreador administrado por el sistema operativo de las aplicaciones de Direct3D 11 en Windows 10 Creators Update.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 
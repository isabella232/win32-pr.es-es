---
title: Uso de secuencias de audio y vídeo sin comprimir
description: Uso de secuencias de audio y vídeo sin comprimir
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flujos, configurar secuencias de audio y vídeo sin comprimir
- códecs, configurar secuencias de audio y vídeo sin comprimir
- secuencias de vídeo, sin comprimir
- secuencias de audio sin comprimir
- secuencias de audio y vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714333"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Uso de secuencias de audio y vídeo sin comprimir

En la mayoría de los casos, el medio sin comprimir tiene requisitos de almacenamiento y entrega muy elevados, pero en algunos escenarios de reproducción local, el nivel de calidad es lo suficientemente importante como para garantizar que no se use la compresión.

La configuración de una secuencia de medios sin comprimir debe reflejar la configuración de los medios de origen. Al configurar una secuencia sin comprimir, debe calcular la velocidad de bits del medio y establecer la secuencia de forma adecuada llamando a [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate). Dado que las secuencias sin comprimir no son viables para la transmisión por secuencias, siempre debe establecer en cero la ventana de búfer de los flujos de medios sin comprimir llamando a [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).

Se admiten los siguientes formatos de píxel para las secuencias de vídeo sin comprimir:

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ i420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de secuencias de audio**](configuring-audio-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Configuración de secuencias de vídeo**](configuring-video-streams.md)
</dt> </dl>

 

 





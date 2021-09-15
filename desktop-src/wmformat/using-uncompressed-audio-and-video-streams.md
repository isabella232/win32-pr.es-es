---
title: Uso de audio y vídeo sin comprimir Secuencias
description: Uso de audio y vídeo sin comprimir Secuencias
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- secuencias, configuración de secuencias de audio y vídeo sin comprimir
- códecs, configuración de secuencias de audio y vídeo sin comprimir
- secuencias de vídeo, sin comprimir
- secuencias de audio, sin comprimir
- secuencias de audio y vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574304"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Uso de audio y vídeo sin comprimir Secuencias

En la mayoría de los casos, los medios sin comprimir tienen requisitos de almacenamiento y entrega prohibitivamente grandes, pero en algunos escenarios de reproducción local, el nivel de calidad es lo suficientemente importante como para garantizar que no se use la compresión.

La configuración de un flujo multimedia sin comprimir debe reflejar la configuración del medio de origen. Al configurar una secuencia sin comprimir, debe calcular la velocidad de bits del medio y establecer la secuencia correctamente llamando a [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate). Dado que las secuencias no comprimidas no son viables para el streaming, siempre debe establecer la ventana de búfer para los flujos multimedia sin comprimir en cero llamando a [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).

Se admiten los siguientes formatos de píxel para secuencias de vídeo sin comprimir:

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de audio Secuencias**](configuring-audio-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Configuración de video Secuencias**](configuring-video-streams.md)
</dt> </dl>

 

 





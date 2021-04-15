---
title: Formatos de entrada de vídeo
description: Formatos de entrada de vídeo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- SDK de Windows Media Format, formatos de entrada de vídeo
- Formato de sistemas avanzados (ASF), formatos de entrada de vídeo
- ASF (formato de sistemas avanzados), formatos de entrada de vídeo
- formatos de entrada de vídeo
- SDK de Windows Media Format, formatos de vídeo
- Formato de sistemas avanzados (ASF), formatos de vídeo
- ASF (formato de sistemas avanzados), formatos de vídeo
- formatos de vídeo
- Códec de Windows Media Video 9, formatos de entrada de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105695574"
---
# <a name="video-input-formats"></a>Formatos de entrada de vídeo

El escritor acepta los siguientes formatos de vídeo como entrada para comprimirlos con el códec Windows Media Video 9:

-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ i420
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU
-   WMMEDIASUBTYPE \_ YVU9
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB565
-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB8

Siempre debe usar [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) y [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) para enumerar los formatos de entrada disponibles y obtener el objeto de propiedades de medios de entrada para el formato deseado. Los objetos de las propiedades de los medios de entrada de vídeo deben cambiarse para reflejar el tamaño y la velocidad de fotogramas de los medios de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> </dl>

 

 





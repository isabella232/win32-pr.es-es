---
title: Formatos de entrada de vídeo
description: Formatos de entrada de vídeo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows SDK de formato multimedia, formatos de entrada de vídeo
- Formato de sistemas avanzados (ASF), formatos de entrada de vídeo
- ASF (formato de sistemas avanzados), formatos de entrada de vídeo
- formatos de entrada de vídeo
- Windows SDK de formato multimedia, formatos de vídeo
- Formato de sistemas avanzados (ASF), formatos de vídeo
- ASF (formato de sistemas avanzados), formatos de vídeo
- formatos de vídeo
- Windows Códec Media Video 9, formatos de entrada de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256190"
---
# <a name="video-input-formats"></a>Formatos de entrada de vídeo

El escritor acepta los siguientes formatos de vídeo como entrada para comprimirse mediante el códec Windows Media Video 9:

-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ I420
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

Siempre debe usar [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) e [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) para enumerar los formatos de entrada disponibles y obtener el objeto de propiedades del medio de entrada para el formato deseado. Los objetos de propiedades de los medios de entrada de vídeo deben cambiarse para reflejar el tamaño del fotograma y la velocidad de fotogramas de los medios de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> </dl>

 

 





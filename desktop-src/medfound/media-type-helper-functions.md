---
description: Las siguientes funciones pertenecen a objetos de tipo multimedia.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funciones auxiliares de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b488eb706338926aaffd3c3c4e13a5da4d1d004bd21dbbd1f5871c6d4818dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827365"
---
# <a name="media-type-helper-functions"></a>Funciones auxiliares de tipos de medios

Las siguientes funciones pertenecen a objetos de tipo multimedia.



| Función                                                                     | Descripción                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcula la velocidad de fotogramas a partir de la duración media de un fotograma de vídeo. |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Recupera el tamaño de la imagen para un formato de vídeo sin comprimir.            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | Compara un tipo de medio completo con un tipo de medio parcial.                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | Crea un tipo de medio vacío.                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Convierte una velocidad de fotogramas de vídeo en una duración de fotogramas.                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Recupera el paso de superficie mínimo para un formato de vídeo.              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Consulta si un código FOURCC o **un valor D3DFORMAT** es un formato YUV. |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | Valida el tamaño de un búfer para un bloque de formato de vídeo.              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | Crea un tipo de medio que encapsula otro tipo de medio.                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Conversiones de tipos de medios](media-type-conversions.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




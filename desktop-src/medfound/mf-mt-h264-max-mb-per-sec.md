---
description: Especifica la velocidad máxima de procesamiento del macrobloqueo para una secuencia de vídeo H.264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93bce2de0aa4f6c67cc7f6e61c09fde89923467a9211ba9e10642edf5a7f6416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104542"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>Atributo \_ MF MT \_ H264 \_ MAX MB PER \_ \_ \_ SEC

Especifica la velocidad máxima de procesamiento del macrobloqueo para una secuencia de vídeo H.264.

## <a name="data-type"></a>Tipo de datos

**UINT32 \[ \]** almacenado como **UINT8 \[ \]**

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios para flujos H.264 transmitidos a través de USB. El valor del atributo es una matriz de valores UINT32, que corresponden a los siguientes campos del descriptor de formato de vídeo UVC 1.5 H.264.

| Elemento Array | Campo descriptor                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionTemporalScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsMaxScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsMaxScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsMaxScalability**        |
| 8             | **dwMaxMBperSecOneResolutionMaxQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsMaxQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsMaxQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsMaxQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

Este atributo también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 





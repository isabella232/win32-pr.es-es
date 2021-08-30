---
description: Especifica los modos de uso admitidos para una secuencia de vídeo H.264.
ms.assetid: EEAE0B57-9731-4032-80A3-6A1AD11214EC
title: MF_MT_H264_SUPPORTED_USAGES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d507578c25d8b90fbe3ef6bfab66055651bc7b0b93e25eb42723121f4b16a3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940625"
---
# <a name="mf_mt_h264_supported_usages-attribute"></a>Atributo USAGES ADMITIDOS de MF \_ MT \_ H264 \_ \_

Especifica los modos de uso admitidos para una secuencia de vídeo H.264.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios para flujos H.264 transmitidos a través de USB. El valor corresponde al campo **bmSupportedUsages** del descriptor de fotograma de vídeo UVC 1.5 H.264.

Este atributo también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 





---
description: Especifica los tipos de marco de sincronización que se admiten para una secuencia de vídeo H.264.
ms.assetid: A2E548F1-A5FA-4110-AD07-46BE9D7DC4A5
title: MF_MT_H264_SUPPORTED_SYNC_FRAME_TYPES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f6b6d00b3914ebcf55952baf372c139d43a02689605f800628df58b2d71395b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113745"
---
# <a name="mf_mt_h264_supported_sync_frame_types-attribute"></a>Atributo MF \_ MT \_ H264 \_ SUPPORTED SYNC FRAME \_ \_ \_ TYPES

Especifica los tipos de marco de sincronización que se admiten para una secuencia de vídeo H.264.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios para flujos H.264 transmitidos a través de USB. El valor corresponde al campo **bmSupportedSyncFrameTypes** del descriptor de formato de vídeo UVC 1.5 H.264.

Este atributo también se usa con codificadores de cámara [H.264 UVC 1.5](camera-encoder-h264-uvc-1-5.md).

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

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 





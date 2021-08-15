---
description: Especifica las marcas de funcionalidad para una secuencia de vídeo H.264.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: MF_MT_H264_CAPABILITIES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138cfa32fc50ebb02ca4d399a178b338e58016c64ae3486d7f7b4a76f3e47afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741835"
---
# <a name="mf_mt_h264_capabilities-attribute"></a>Atributo MF \_ MT \_ H264 \_ CAPABILITIES

Especifica las marcas de funcionalidad para una secuencia de vídeo H.264.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios para flujos H.264 transmitidos a través de USB. El valor corresponde al campo **bmCapabilities** del descriptor de fotograma de vídeo UVC 1.5 H.264.

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

 

 





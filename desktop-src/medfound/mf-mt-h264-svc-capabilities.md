---
description: Especifica las capacidades de SVC de una secuencia de vídeo H. 264.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: MF_MT_H264_SVC_CAPABILITIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35a39b5f1727af8399d9d0c56c93d2d9d1486c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810100"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a>\_Atributo de \_ \_ capacidades SVC MT H264 SVC \_

Especifica las capacidades de SVC de una secuencia de vídeo H. 264.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los tipos de medios para flujos H. 264 transmitidos a través de USB. El valor corresponde al campo **bmSVCCapabilities** en el descriptor de fotogramas de vídeo UVC 1,5 H. 264.

Este atributo también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 





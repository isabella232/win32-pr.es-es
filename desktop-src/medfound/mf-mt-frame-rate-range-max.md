---
description: Velocidad máxima de fotogramas que admite un dispositivo de captura de vídeo, en fotogramas por segundo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364007"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>Atributo MF \_ MT FRAME RATE RANGE \_ \_ \_ \_ MAX

Velocidad máxima de fotogramas que admite un dispositivo de captura de vídeo, en fotogramas por segundo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame [**a MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Observaciones

La velocidad de fotogramas se expresa como una relación. Los 32 bits superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (fps), la proporción es de 30/1.

Si el dispositivo de captura notifica una velocidad de fotogramas máxima, el origen del medio establece este atributo en el tipo de medio. La velocidad mínima de fotogramas se especifica en el atributo [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MIN.](mf-mt-frame-rate-range-min.md) No se garantiza que el dispositivo admita cada incremento dentro de este intervalo.

Para establecer la velocidad de fotogramas del dispositivo, modifique primero el valor del atributo [**MF \_ MT FRAME \_ \_ RATE**](mf-mt-frame-rate-attribute.md) en el tipo de medio. A continuación, establezca el tipo de medio en el origen de medios.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Cómo establecer la velocidad de fotogramas de captura de vídeo](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 





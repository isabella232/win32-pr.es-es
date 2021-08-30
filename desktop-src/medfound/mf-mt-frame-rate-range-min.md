---
description: Velocidad mínima de fotogramas que admite un dispositivo de captura de vídeo, en fotogramas por segundo.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: MF_MT_FRAME_RATE_RANGE_MIN atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11253444255e3bac36cb4563e632ebe04d1782b0ae8edadabc08e34cf1d38a99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113795"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>Atributo MF \_ MT FRAME RATE RANGE \_ \_ \_ \_ MIN

Velocidad mínima de fotogramas que admite un dispositivo de captura de vídeo, en fotogramas por segundo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame [**a MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Comentarios

La velocidad de fotogramas se expresa como una relación. Los 32 bits superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (fps), la proporción es de 30/1.

Si el dispositivo de captura informa de una velocidad de fotogramas mínima, el origen del medio establece este atributo en el tipo de medio. La velocidad máxima de fotogramas se especifica en el atributo [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MAX.](mf-mt-frame-rate-range-max.md) No se garantiza que el dispositivo admita cada incremento dentro de este intervalo.

Para establecer la velocidad de fotogramas del dispositivo, modifique primero el valor del atributo [**MF \_ MT FRAME \_ \_ RATE**](mf-mt-frame-rate-attribute.md) en el tipo de medio. A continuación, establezca el tipo de medio en el origen de medios.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Cómo establecer la velocidad de fotogramas de captura de vídeo](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 





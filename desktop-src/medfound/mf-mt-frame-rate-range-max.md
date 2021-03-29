---
description: La velocidad de fotogramas máxima que admite un dispositivo de captura de vídeo, en fotogramas por segundo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001501"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>\_Atributo de \_ intervalo de velocidad de fotogramas MF MT \_ \_ \_

La velocidad de fotogramas máxima que admite un dispositivo de captura de vídeo, en fotogramas por segundo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Observaciones

La velocidad de fotogramas se expresa como una proporción. Los 32 superiores del valor del atributo contienen el numerador, y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1.

Si el dispositivo de captura informa de una velocidad de fotogramas máxima, el origen de medios establece este atributo en el tipo de medio. La velocidad de fotogramas mínima se indica en el atributo de [ \_ intervalo de velocidad de \_ fotogramas MF MT \_ \_ \_ min](mf-mt-frame-rate-range-min.md) . No se garantiza que el dispositivo admita todos los incrementos dentro de este intervalo.

Para establecer la velocidad de fotogramas del dispositivo, modifique primero el valor del atributo de [**\_ \_ \_ velocidad de fotogramas MF MT**](mf-mt-frame-rate-attribute.md) en el tipo de medio. A continuación, establezca el tipo de medio en el origen del medio.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Cómo establecer la velocidad de fotogramas de captura de vídeo](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ mín.](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 





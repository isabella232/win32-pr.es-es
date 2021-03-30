---
description: La velocidad de fotogramas mínima admitida por un dispositivo de captura de vídeo, en fotogramas por segundo.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: MF_MT_FRAME_RATE_RANGE_MIN atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912165"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>\_ \_ \_ \_ Atributo min de intervalo de velocidad de fotogramas MF MT \_

La velocidad de fotogramas mínima admitida por un dispositivo de captura de vídeo, en fotogramas por segundo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Observaciones

La velocidad de fotogramas se expresa como una proporción. Los 32 superiores del valor del atributo contienen el numerador, y los 32 bits inferiores contienen el denominador. Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1.

Si el dispositivo de captura informa de una velocidad de fotogramas mínima, el origen de medios establece este atributo en el tipo de medio. La velocidad de fotogramas máxima se indica en el atributo [MF \_ MT \_ Frame \_ rate \_ Range \_ Max](mf-mt-frame-rate-range-max.md) . No se garantiza que el dispositivo admita todos los incrementos dentro de este intervalo.

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

[\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 





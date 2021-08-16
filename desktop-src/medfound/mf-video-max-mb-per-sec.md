---
description: Especifica, en IMFTransform, la velocidad máxima de procesamiento del macrobloqueo, en macrobloques por segundo, que es compatible con el codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c76e6a44a6e0993f9cf6410a0092708da767f92815fc98020dd2f4d88359370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739243"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>Atributo MF \_ VIDEO MAX MB PER \_ \_ \_ \_ SEC

Especifica, en [**IMFTransform,**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)la velocidad máxima de procesamiento de macrobloqueo, en macrobloques por segundo, que es compatible con el codificador de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo es de solo lectura.

**Codificadores H.264/AVC:**

Este atributo se ve afectado por las siguientes propiedades:

-   [MF \_ MT \_ VIDEO \_ LEVEL](mf-mt-video-level.md) (que es un alias de MF MT [ \_ \_ MPEG2 \_ LEVEL](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Si el [atributo MF MT VIDEO \_ \_ \_ LEVEL](mf-mt-video-level.md) está presente, el codificador debe devolver la velocidad de procesamiento de la velocidad de bits más alta y la resolución admitida en el nivel especificado. Si el atributo MF \_ MT VIDEO LEVEL no está \_ \_ presente, debe usar un nivel predeterminado de 4.

Si se ha establecido la propiedad ICodecAPI [CODECAPI \_ AVEncCommonQualityVsSpeed,](../directshow/avenccommonqualityvsspeed-property.md) el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad. Si el atributo CODECAPI AVEncCommonQualityVsSpeed no está presente, debe usar un valor predeterminado de 0, que debe ser el modo \_ de procesamiento más rápido.

Si la propiedad ICodecAPI [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) se ha establecido en un valor válido y admitido, el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad. Si el atributo CODECAPI AVEncMPVDefaultBPictureCount no es presen, debe usar un valor predeterminado de \_ 0 fotogramas B.

Una aplicación solo debe usar los 28 bits inferiores. Los 4 bits superiores están reservados para su uso futuro. Las aplicaciones deben omitir los 4 bits superiores y las MTA deben establecer los 4 bits superiores en 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

---
description: Especifica, en IMFTransform, la velocidad de procesamiento máxima de adaptativo macrobloque, en macrobloques por segundo, que es compatible con el codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720412"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>\_Atributo MF \_ máx \_ \_ . MB por \_ segundo de vídeo

Especifica, en [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la velocidad de procesamiento máxima de adaptativo macrobloque, en macrobloques por segundo, que es compatible con el codificador de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo es de solo lectura.

**Codificadores H. 264/AVC:**

Este atributo se ve afectado por las siguientes propiedades:

-   [MF \_ \_ \_ Nivel de vídeo MT](mf-mt-video-level.md) (que es un alias de [ \_ nivel MF MT \_ MPEG2 \_ ](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Si el atributo de [ \_ nivel de \_ vídeo \_ MF MT](mf-mt-video-level.md) está presente, el codificador debe devolver la velocidad de procesamiento de la velocidad de bits y la resolución más altas admitidas en el nivel especificado. Si el \_ atributo de \_ nivel de vídeo MF MT \_ no está presente, debe usar un nivel predeterminado de 4.

Si se ha establecido la propiedad [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI, el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad. Si el \_ atributo AVEncCommonQualityVsSpeed de CODECAPI no está presente, debe usar un valor predeterminado de 0, que debe ser el modo de procesamiento más rápido.

Si la propiedad ICodecAPI de [ \_ AVEncMPVDefaultBPictureCount de CODECAPI](../directshow/avencmpvdefaultbpicturecount-property.md) se ha establecido en un valor válido y admitido, el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad. Si el \_ atributo CODECAPI AVEncMPVDefaultBPictureCount no es Pres, entonces debe usar un valor predeterminado de 0 B fotogramas.

Una aplicación solo debe usar los 28 bits inferiores. Los 4bits superiores se reservan para uso futuro. Las aplicaciones deben omitir los 4 bits superiores y MFTs deben establecer los 4 bits superiores en 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

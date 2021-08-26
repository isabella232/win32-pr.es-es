---
description: Especifica el nivel MPEG-2 o H.264 en un tipo de medio de vídeo. Se trata de un alias de MF \_ MT \_ MPEG2 \_ LEVEL.
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012775"
---
# <a name="mf_mt_video_level-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ LEVEL

Especifica el nivel MPEG-2 o H.264 en un tipo de medio de vídeo. Se trata de un alias [de MF \_ MT \_ MPEG2 \_ LEVEL.](mf-mt-mpeg2-level-attribute.md)

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

**Codificadores H.264:**

Los niveles admitidos se amplían para incluir [**eAVEncH264VLevel5 \_ 2.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)

Valor predeterminado: el valor predeterminado recomendado es seleccionar el nivel mínimo para que coincida con la configuración de codificación de vídeo, incluida la resolución, la velocidad de fotogramas, etc.

Valor predeterminado recomendado: seleccione el nivel mínimo para que coincida con la configuración de codificación de vídeo, incluida la resolución, la velocidad de fotogramas, etc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





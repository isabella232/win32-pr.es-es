---
description: Especifica el nivel MPEG-2 o H. 264 en un tipo de medio de vídeo. Se trata de un alias de \_ nivel MF MT \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717007"
---
# <a name="mf_mt_video_level-attribute"></a>\_Atributo de \_ nivel de vídeo MF MT \_

Especifica el nivel MPEG-2 o H. 264 en un tipo de medio de vídeo. Se trata de un alias [de \_ \_ \_ nivel MF MT MPEG2](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264:**

Los niveles admitidos se amplían para incluir [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

Predeterminado: el valor predeterminado recomendado es seleccionar el nivel mínimo para que coincida con la configuración de la codificación de vídeo, incluida la resolución, la velocidad de fotogramas, etc.

Opción predeterminada recomendada: seleccione el nivel mínimo para que coincida con la configuración de la codificación de vídeo, incluida la resolución, la velocidad de fotogramas, etc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





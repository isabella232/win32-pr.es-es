---
description: Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4100a605ecc7e8fe1c171b02341822972061363e7cd1b322162291dbd75b2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692074"
---
# <a name="mf_mt_video_3d_format-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ 3D \_ FORMAT

Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en memoria.

## <a name="data-type"></a>Tipo de datos

**MFVideo3DFormat** almacenado como **UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es miembro de la [**enumeración MFVideo3DFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) El atributo solo se aplica si el atributo [MF \_ MT VIDEO \_ \_ 3D](mf-mt-video-3d.md) es **TRUE.**

Este atributo es necesario para los formatos de vídeo 3D sin comprimir. Es opcional para vídeo 3D comprimido. Un origen multimedia que entrega fotogramas codificados podría ser capaz de establecer el atributo, en función de la información del contenedor de archivos. De lo contrario, el descodificador debe establecer el atributo en el tipo de medio de salida del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





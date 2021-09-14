---
description: Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363931"
---
# <a name="mf_mt_video_3d_format-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ 3D \_ FORMAT

Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en memoria.

## <a name="data-type"></a>Tipo de datos

**MFVideo3DFormat** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es miembro de la [**enumeración MFVideo3DFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) El atributo solo se aplica si el atributo [MF \_ MT VIDEO \_ \_ 3D](mf-mt-video-3d.md) es **TRUE.**

Este atributo es necesario para los formatos de vídeo 3D sin comprimir. Es opcional para vídeo 3D comprimido. Un origen multimedia que entrega fotogramas codificados podría ser capaz de establecer el atributo, en función de la información del contenedor de archivos. De lo contrario, el descodificador debe establecer el atributo en el tipo de medio de salida del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





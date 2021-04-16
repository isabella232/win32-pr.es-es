---
description: Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en la memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678286"
---
# <a name="mf_mt_video_3d_format-attribute"></a>\_Atributo de \_ formato de vídeo \_ 3D MF MT \_

Para un tipo de medio de vídeo, especifica cómo se almacenan los fotogramas de vídeo 3D en la memoria.

## <a name="data-type"></a>Tipo de datos

**MFVideo3DFormat** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) . El atributo solo se aplica si el atributo [MF \_ MT \_ video \_ 3D](mf-mt-video-3d.md) es **true**.

Este atributo es necesario para los formatos de vídeo 3D sin comprimir. Es opcional para vídeo 3D comprimido. Un origen multimedia que proporciona fotogramas codificados podría establecer el atributo, en función de la información del contenedor de archivos. En caso contrario, el descodificador debe establecer el atributo en el tipo de medio de salida del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





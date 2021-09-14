---
description: Para un formato de vídeo 3D, especifica qué vista es la vista izquierda.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363934"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ MT \_ VIDEO \_ 3D \_ FIRST IS LEFT \_ \_ attribute

Para un formato de vídeo 3D, especifica qué vista es la vista izquierda.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Observaciones

En el caso del vídeo 3D, cada ejemplo de vídeo contiene dos vistas, que se designan como primera *vista* y *segunda vista.* El diseño exacto de las vistas en memoria se indica mediante el atributo [MF \_ MT VIDEO \_ \_ 3D \_ FORMAT.](mf-mt-video-3d-format.md)



| Formato               | Primera vista              | Segunda vista               |
|----------------------|-------------------------|---------------------------|
| Empaquetado en paralelo  | Mitad izquierda del búfer | Mitad derecha del búfer  |
| Empaquetado de arriba a abajo | Mitad superior del búfer  | Mitad inferior del búfer |
| Multivista            | Índice de búfer 0          | Índice de búfer 1            |
| Vista base            | Fotograma completo            | No está presente               |



 

De forma predeterminada, la primera vista es la vista izquierda y la segunda es la vista derecha. Si se intercambian las vistas izquierda y derecha, establezca el atributo MF \_ MT \_ VIDEO \_ 3D FIRST IS LEFT en FALSE en \_ el tipo de \_ \_ medio. 

> [!Note]  
> En *formato de vista base* **(MFVideo3DSampleFormat \_ BaseView),** solo se conserva la vista base, por lo que este atributo no se aplica.

 

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

 

 





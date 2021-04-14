---
description: En el caso de un formato de vídeo 3D, especifica qué vista es la vista izquierda.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424056"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ MT \_ vídeo \_ 3D \_ primero \_ es el \_ atributo izquierdo

En el caso de un formato de vídeo 3D, especifica qué vista es la vista izquierda.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

En el caso de vídeo en 3D, cada ejemplo de vídeo contiene dos vistas, que se designan como *primera vista* y *segunda vista*. El diseño exacto de las vistas en memoria se indica mediante el atributo de [ \_ \_ \_ \_ formato 3D de vídeo MF MT](mf-mt-video-3d-format.md) .



| Formato               | Primera vista              | Segunda vista               |
|----------------------|-------------------------|---------------------------|
| Empaquetados en paralelo  | Mitad izquierda del búfer | Mitad derecha del búfer  |
| Empaquetados de arriba abajo | Mitad superior del búfer  | Mitad inferior del búfer |
| MultiView            | Índice de búfer 0          | Índice de búfer 1            |
| Vista base            | Fotograma completo            | No está presente               |



 

De forma predeterminada, la primera vista es la vista izquierda y la segunda vista es la derecha. Si se intercambian las vistas izquierda y derecha, establezca el \_ atributo MF MT \_ video \_ 3D \_ First \_ is \_ left en **false** en el tipo de medio.

> [!Note]  
> En el formato de *vista base* (**MFVideo3DSampleFormat \_ BaseView**), solo se conserva la vista base, por lo que este atributo no se aplica.

 

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

 

 





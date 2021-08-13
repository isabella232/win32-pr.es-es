---
description: Para un formato de vídeo 3D, especifica qué vista es la vista base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03bc12d32b96abc52999ef6a3b21580c4ac1c59125a076b9eb1d620e0bd362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741597"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>Mf \_ MT \_ VIDEO \_ 3D \_ LEFT IS BASE \_ \_ attribute

Para un formato de vídeo 3D, especifica qué vista es la vista base.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Observaciones

De forma predeterminada, la vista izquierda de una secuencia de vídeo 3D es la vista base. Si la vista derecha es la vista base, establezca este atributo en **FALSE.**

Para convertir vídeo estéreo en 2D, mantenga la vista base y descarte la otra vista.

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

 

 





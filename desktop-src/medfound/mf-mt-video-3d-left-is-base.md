---
description: Para un formato de vídeo 3D, especifica qué vista es la vista base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363930"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>Mf \_ MT \_ VIDEO \_ 3D \_ LEFT IS BASE \_ \_ attribute

Para un formato de vídeo 3D, especifica qué vista es la vista base.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Observaciones

De forma predeterminada, la vista izquierda de una secuencia de vídeo 3D es la vista base. Si la vista derecha es la vista base, establezca este atributo en **FALSE.**

Para convertir vídeo estéreo a 2D, mantenga la vista base y descarte la otra vista.

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

 

 





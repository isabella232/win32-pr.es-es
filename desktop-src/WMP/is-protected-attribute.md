---
title: Is_Protected atributo
description: El atributo Is \_ Protected indica si el contenido está protegido mediante administración de derechos digitales (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected atributo Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 520631b90e4ff379d3a613008dee2db5d76784a831ef54ef0d3551fbf99a85f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763865"
---
# <a name="is_protected-attribute"></a>Atributo \_ Protegido

El **atributo Is \_ Protected** indica si el contenido está protegido mediante administración de derechos digitales (DRM).

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos multimedia de Windows usados con frecuencia](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**DigitallySecure** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMProtected.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






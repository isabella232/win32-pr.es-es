---
title: Atributo WM/ContentDistributor
description: El atributo WM/ContentDistributor es el nombre del distribuidor del elemento.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Atributo WM/ContentDistributor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba79ab07b8579961db70038ef80f79da974ba5dff6d3ac88781be5d4f046f088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122715"
---
# <a name="wmcontentdistributor-attribute"></a>Atributo WM/ContentDistributor

El **atributo WM/ContentDistributor** es el nombre del distribuidor del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**ContentDistributor** es un alias para este atributo.

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszWMContentDistributor.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






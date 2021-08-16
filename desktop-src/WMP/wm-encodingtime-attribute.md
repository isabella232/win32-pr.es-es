---
title: Atributo WM/EncodingTime
description: El atributo WM/EncodingTime es la fecha y hora en que se ha codificado el contenido.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Atributo WM/EncodingTime Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b143218b854177852049c1ae1ed530360c196eecd217db3ed53d9f46bd2915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122665"
---
# <a name="wmencodingtime-attribute"></a>Atributo WM/EncodingTime

El **atributo WM/EncodingTime** es la fecha y hora en que se ha codificado el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**CreationDate** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMEncodingTime.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






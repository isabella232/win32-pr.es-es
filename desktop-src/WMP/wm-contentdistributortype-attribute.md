---
title: Atributo WM/ContentDistributorType
description: El atributo WM/ContentDistributorType es el tipo del distribuidor del elemento.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Atributo WM/ContentDistributorType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c9d44ad64cf860f1ad70827b51dd2cda28717fd6531d1e570a52a1ac070304
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862125"
---
# <a name="wmcontentdistributortype-attribute"></a>Atributo WM/ContentDistributorType

El **atributo WM/ContentDistributorType** es el tipo del distribuidor del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

El valor de este atributo se establecerá en "List" o "Radio". Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**ContentDistributorType es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMContentDistributorType.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






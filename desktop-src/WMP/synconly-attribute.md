---
title: Atributo SyncOnly
description: El atributo SyncOnly es una representación de cadena de un valor booleano que Reproductor de Windows Media para determinar si una lista de reproducción solo está disponible para la sincronización.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Atributo SyncOnly Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134738"
---
# <a name="synconly-attribute"></a>Atributo SyncOnly

El **atributo SyncOnly** es una representación de cadena de un valor **booleano** que Reproductor de Windows Media para determinar si una lista de reproducción solo está disponible para la sincronización.

## <a name="applies-to"></a>Se aplica a

-   [Listas](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentarios

El valor 1 indica que la lista de reproducción solo está disponible para la sincronización y no puede aparecer en el **nodo Lista de reproducción** automática. Un valor de cero indica que la lista de reproducción puede aparecer en el **nodo Lista de reproducción** automática.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






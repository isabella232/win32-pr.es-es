---
title: Atributo UserServiceRating
description: El atributo UserServiceRating está reservado para su uso futuro.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Atributo UserServiceRating Reproductor de Windows Media
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1dc9b0f1131a02a4ce3fe05ebe2423116e7701e3bbb9ce7f5ea8faa1c1dce7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001595"
---
# <a name="userservicerating-attribute"></a>Atributo UserServiceRating

El **atributo UserServiceRating** está reservado para su uso futuro.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Las clasificaciones de usuario se representan mediante valores enteros, como se describe en la tabla siguiente. Al especificar un valor, use uno de los valores de la columna Valor de escritura. Al recuperar valores, puede usar los intervalos de la columna Valores de lectura para determinar el número de estrellas.



| Rating  | Escribir valor | Lectura de valores |
|---------|---------------|----------------|
| Sin censura | 0             | 0              |
| 1 estrella  | 1             | De 1 a 12        |
| 2 estrellas | 25            | De 13 a 37       |
| 3 estrellas | 50            | De 38 a 62       |
| 4 estrellas | 75            | De 63 a 86       |
| 5 estrellas | 99            | De 87 a 99       |



 

Este atributo solo se almacena en la biblioteca.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






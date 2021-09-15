---
title: Atributo UserEffectiveRating
description: El atributo UserEffectiveRating es la clasificación calculada por Reproductor de Windows Media en función de la frecuencia con la que se ha reproducido el elemento.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Atributo UserEffectiveRating Reproductor de Windows Media
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569053"
---
# <a name="usereffectiverating-attribute"></a>Atributo UserEffectiveRating

El **atributo UserEffectiveRating** es la clasificación calculada por Reproductor de Windows Media en función de la frecuencia con la que se ha reproducido el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

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

 

 






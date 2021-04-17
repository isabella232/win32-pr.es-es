---
title: Atributo UserEffectiveRating
description: El atributo UserEffectiveRating es la clasificación calculada por Windows Media Player en función de la frecuencia de reproducción del elemento.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- UserEffectiveRating Media Player de Windows
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718701"
---
# <a name="usereffectiverating-attribute"></a>Atributo UserEffectiveRating

El atributo **UserEffectiveRating** es la clasificación calculada por Windows Media Player en función de la frecuencia de reproducción del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Las clasificaciones de usuario se representan mediante valores enteros, como se describe en la tabla siguiente. Al especificar un valor, use uno de los valores de la columna valor de escritura. Al recuperar valores, puede usar los intervalos de la columna leer valores para determinar el número de estrellas.



| Rating  | Escribir valor | Leer valores |
|---------|---------------|----------------|
| Sin clasificación | 0             | 0              |
| 1 estrella  | 1             | De 1 a 12        |
| 2 estrellas | 25            | de 13 a 37       |
| 3 estrellas | 50            | de 38 a 62       |
| 4 estrellas | 75            | de 63 a 86       |
| 5 estrellas | 99            | de 87 a 99       |



 

Este atributo solo se almacena en la biblioteca.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 






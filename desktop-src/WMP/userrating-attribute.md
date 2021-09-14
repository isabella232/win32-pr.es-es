---
title: Atributo UserRating
description: El atributo UserRating es la clasificación especificada por el usuario en la biblioteca.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- UserRating Attribute Reproductor de Windows Media
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070855"
---
# <a name="userrating-attribute"></a>Atributo UserRating

El **atributo UserRating** es la clasificación especificada por el usuario en la biblioteca.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotos](photo-item-attributes.md)
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
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior (el elemento de foto solo se admite en Reproductor de Windows Media 10 o posterior)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 






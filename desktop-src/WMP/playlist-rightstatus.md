---
title: PLAYLIST.rightStatus
description: El atributo rightStatus especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Playlist.rightStatus Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b79b0f4e3ad18ed4e044f894d63ec5059477f80999a8b96dc461d9499b29cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336568"
---
# <a name="playlistrightstatus"></a>PLAYLIST.rightStatus

El **atributo rightStatus** especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento **PLAYLIST.**

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Este atributo puede combinar cualquier texto con palabras clave específicas que mostrarán la información deseada, como la duración total de la lista de reproducción. Las palabras clave están entre símbolos de porcentaje (%) para mantenerlas distintas del texto normal.

Se pueden usar las siguientes palabras clave.



| Palabra clave               | Descripción                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Número de elementos de la lista de reproducción.                                                                                                                                                                             |
| tamaño                  | Tamaño total de la lista de reproducción.                                                                                                                                                                                  |
| duration              | Duración total de la lista de reproducción.                                                                                                                                                                              |
| *Xxx*                 | Hace un **getItemInfo en** la lista de reproducción y *XXX* es el elemento que se va a recibir.                                                                                                                                 |
| SelectedSize          | Tamaño total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                          |
| SelectedCount         | Número total de entradas seleccionadas en la lista de reproducción.                                                                                                                                                            |
| SelectedDuration      | Duración total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                      |
| CheckedCount          | Número total de pistas activadas en la lista de reproducción.                                                                                                                                                              |
| CheckedDuration       | Duración total de las pistas activadas en la lista de reproducción.                                                                                                                                                        |
| CheckedSize           | Tamaño total de las pistas activadas en la lista de reproducción.                                                                                                                                                            |
| DurationString        | Muestra texto que describe la duración como "Tiempo total" o "Tiempo estimado", en función de si se conocen los valores totales. Este texto va seguido de "%duration%".                                       |
| CheckedDurationString | Muestra texto que describe la duración de todos los elementos activados en la lista de reproducción como "Tiempo total" o "Tiempo estimado", dependiendo de si se conocen los valores totales. Este texto va seguido de "%duration%". |



 

El valor "Tiempo total: %duration%" para una lista de reproducción que contiene una duración total de siete minutos mostrará "Tiempo total: 07:00".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 






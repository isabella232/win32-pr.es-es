---
title: PLAYLIST.leftStatus
description: El atributo leftStatus especifica o recupera el texto de estado que se muestra en el lado izquierdo y en la parte inferior del elemento PLAYLIST.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- LISTA DE REPRODUCCIÓN.leftStatus Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466157"
---
# <a name="playlistleftstatus"></a>PLAYLIST.leftStatus

El **atributo leftStatus** especifica o recupera el texto de estado que se muestra en el lado izquierdo y en la parte inferior del elemento **PLAYLIST.**

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**

## <a name="remarks"></a>Observaciones

Este atributo puede combinar cualquier texto con palabras clave específicas que mostrarán la información deseada, como la duración total de la lista de reproducción. Las palabras clave están rodeados de símbolos de porcentaje (%) para mantenerlos distintos del texto normal.

Se pueden usar las siguientes palabras clave.



| Palabra clave               | Descripción                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Número de elementos de la lista de reproducción.                                                                                                                                                                             |
| tamaño                  | Tamaño total de la lista de reproducción.                                                                                                                                                                                  |
| duration              | Duración total de la lista de reproducción.                                                                                                                                                                              |
| *XXX*                 | Hace un **elemento getItemInfo en** la lista de reproducción, *donde XXX* es el elemento que se va a recibir.                                                                                                                                 |
| SelectedSize          | Tamaño total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                          |
| SelectedCount         | Número total de entradas seleccionadas en la lista de reproducción.                                                                                                                                                            |
| SelectedDuration      | Duración total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                      |
| CheckedCount          | Número total de pistas activadas en la lista de reproducción.                                                                                                                                                              |
| CheckedDuration       | Duración total de las pistas activadas en la lista de reproducción.                                                                                                                                                        |
| CheckedSize           | Tamaño total de las pistas activadas en la lista de reproducción.                                                                                                                                                            |
| DurationString        | Muestra texto que describe la duración como "Tiempo total" o "Tiempo estimado", dependiendo de si se conocen los valores totales. Este texto va seguido de "%duration%".                                       |
| CheckedDurationString | Muestra texto que describe la duración de todos los elementos activados en la lista de reproducción como "Tiempo total" o "Tiempo estimado", dependiendo de si se conocen los valores totales. Este texto va seguido de "%duration%". |



 

El valor "Tiempo total: %duration%" para una lista de reproducción que contiene una duración total de siete minutos mostrará "Tiempo total: 07:00".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 






---
title: Lista de reproducción. rightStatus
description: El atributo rightStatus especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento de lista de reproducción.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Windows Media Player de lista de reproducción. rightStatus
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708675"
---
# <a name="playlistrightstatus"></a>Lista de reproducción. rightStatus

El atributo **rightStatus** especifica o recupera el texto de estado que se muestra en el lado derecho y en la parte inferior del elemento de **lista de reproducción** .

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Este atributo puede combinar cualquier texto con palabras clave específicas que muestren la información deseada, como la duración total de la lista de reproducción. Las palabras clave se incluyen entre símbolos de porcentaje (%) para mantenerlos distintos del texto normal.

Se pueden usar las siguientes palabras clave.



| Palabra clave               | Descripción                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Número de elementos de la lista de reproducción.                                                                                                                                                                             |
| tamaño                  | Tamaño total de la lista de reproducción.                                                                                                                                                                                  |
| duration              | Duración total de la lista de reproducción.                                                                                                                                                                              |
| *XXXXXX*                 | Realiza una **getItemInfo** en la lista de reproducción, donde *XXX* es el elemento que se va a recibir.                                                                                                                                 |
| SelectedSize          | Tamaño total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                          |
| SelectedCount         | Número total de entradas seleccionadas en la lista de reproducción.                                                                                                                                                            |
| SelectedDuration      | Duración total de las entradas seleccionadas en la lista de reproducción.                                                                                                                                                      |
| CheckedCount          | Número total de pistas comprobadas en la lista de reproducción.                                                                                                                                                              |
| CheckedDuration       | Duración total de las pistas comprobadas en la lista de reproducción.                                                                                                                                                        |
| CheckedSize           | Tamaño total de las pistas comprobadas en la lista de reproducción.                                                                                                                                                            |
| DurationString        | Muestra el texto que describe la duración como "tiempo total" o "tiempo estimado", en función de si se conocen los valores totales. Este texto va seguido de "% Duration%".                                       |
| CheckedDurationString | Muestra el texto que describe la duración de todos los elementos activados en la lista de reproducción como "tiempo total" o "tiempo estimado", dependiendo de si se conocen los valores totales. Este texto va seguido de "% Duration%". |



 

El valor "tiempo total:% Duration%" para una lista de reproducción que contenga una duración total de siete minutos mostrará "tiempo total: 07:00".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 






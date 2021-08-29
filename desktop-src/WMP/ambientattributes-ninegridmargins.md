---
title: AmbientAttributes.nineGridMargins
description: El atributo nineGridMargins especifica anchos de margen para el escalado no uniforme del elemento de máscara.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- AmbientAttributes.nineGridMargins Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d68e9e5ea8d90312d648e4b0af674a93eec84ddcd09ac7d2cb4bc6bc99ae158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574005"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

El **atributo nineGridMargins** especifica anchos de margen para el escalado no uniforme del elemento de máscara.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura** que contiene los anchos de los márgenes con el formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*". Cada valor de ancho es un número que representa el ancho, en píxeles, de un margen para la cuadrícula de nueve.

## <a name="remarks"></a>Comentarios

Una *cuadrícula de* nueve es una técnica que se usa para dividir los elementos de la interfaz de usuario en nueve regiones rectangulares organizadas en una matriz de 3 por 3. Cuando se cambia el tamaño de un elemento, las nueve regiones de cuadrícula pueden escalarse por un factor diferente.

Cada uno de los cuatro valores de ancho que especifique representa el ancho de una fila o columna de tres regiones adyacentes. Cada fila o columna forma el lado izquierdo, superior, derecho o inferior de la cuadrícula de nueve.

[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) debe establecerse en true para que este atributo funcione.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 






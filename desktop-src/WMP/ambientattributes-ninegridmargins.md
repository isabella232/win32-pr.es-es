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
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889937"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

El **atributo nineGridMargins** especifica anchos de margen para el escalado no uniforme del elemento de máscara.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura** que contiene los anchos de los márgenes con el formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*". Cada valor de ancho es un número que representa el ancho, en píxeles, de un margen para la cuadrícula de nueve.

## <a name="remarks"></a>Observaciones

Una *cuadrícula de* nueve es una técnica que se usa para dividir los elementos de la interfaz de usuario en nueve regiones rectangulares organizadas en una matriz de 3 por 3. Cuando se cambia el tamaño de un elemento, las nueve regiones de cuadrícula pueden escalarse por un factor diferente.

Cada uno de los cuatro valores de ancho que especifique representa el ancho de una fila o columna de tres regiones adyacentes. Cada fila o columna forma el lado izquierdo, superior, derecho o inferior de la cuadrícula de nueve.

[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) debe establecerse en true para que este atributo funcione.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 






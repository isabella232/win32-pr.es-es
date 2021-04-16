---
title: BOTÓN. cursor
description: El atributo cursor especifica o recupera el cursor que aparece cuando se mantiene el puntero del mouse sobre el botón.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BOTÓN. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699568"
---
# <a name="buttoncursor"></a>BOTÓN. cursor

El atributo **cursor** especifica o recupera el cursor que aparece cuando se mantiene el puntero del mouse sobre el **botón**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



| Value            | Descripción                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                     |
| casilla             | Casilla.                                                                                      |
| help             | Flecha con signo de interrogación que indica que la ayuda está disponible.                                     |
| sizeall          | Flecha de cuatro puntas que señala al norte, sur, este y oeste.                                  |
| sizenesw         | Flecha de doble punta que apunta al noreste y al suroeste.                                     |
| tamaños de           | Flecha de dos puntas que apunta al norte y al sur.                                             |
| sizenwse         | Flecha de dos puntas que apunta al noroeste y al sudeste.                                     |
| sizewe           | Flecha de dos puntas que apunta al oeste y al este.                                               |
| flecha arriba          | Flecha vertical que señala hacia arriba.                                                            |
| \*. ani o \* . cur | Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ) |



 

## <a name="remarks"></a>Observaciones

Si el sistema no reconoce el valor de cursor especificado, el valor del cursor permanece en el valor establecido anteriormente.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 






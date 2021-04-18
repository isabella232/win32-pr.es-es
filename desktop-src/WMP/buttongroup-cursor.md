---
title: BUTTONGROUP. cursor
description: El atributo cursor especifica o recupera el tipo de cursor que aparece cuando el mouse está encima de un botón en BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BUTTONGROUP. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699798"
---
# <a name="buttongroupcursor"></a>BUTTONGROUP. cursor

El atributo **cursor** especifica o recupera el tipo de cursor que aparece cuando el mouse está encima de un botón en **BUTTONGROUP**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                      |
| casilla             | Casilla.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que señala al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta al noreste y al suroeste.                                      |
| tamaños de           | Flecha de dos puntas que apunta al norte y al sur.                                              |
| sizenwse         | Flecha de dos puntas que apunta al noroeste y al sudeste.                                      |
| sizewe           | Flecha de dos puntas que apunta al oeste y al este.                                                |
| flecha arriba          | Flecha vertical que señala hacia arriba.                                                             |
| \*. ani o \* . cur | Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ). |



 

## <a name="remarks"></a>Observaciones

El cursor especificado se aplica a todos los botones de **BUTTONGROUP**.

Si especifica un valor de cursor no válido, permanece en el valor establecido anteriormente.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 






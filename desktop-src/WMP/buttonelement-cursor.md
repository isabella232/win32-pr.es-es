---
title: BUTTONELEMENT. cursor
description: El atributo cursor especifica o recupera el valor del cursor BUTTONELEMENT que aparece cuando el mouse está sobre BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700383"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT. cursor

El atributo **cursor** especifica o recupera el valor del cursor **BUTTONELEMENT** que aparece cuando el mouse está sobre **BUTTONELEMENT**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.



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

Si se especifica un valor no válido, se mantiene el valor anterior.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BUTTONELEMENT (elemento)**](buttonelement-element.md)
</dt> </dl>

 

 






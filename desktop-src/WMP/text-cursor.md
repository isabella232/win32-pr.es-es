---
title: TEXT. cursor
description: El atributo cursor especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control de texto.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718649"
---
# <a name="textcursor"></a>TEXT. cursor

El atributo **cursor** especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control de texto.

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



 

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 






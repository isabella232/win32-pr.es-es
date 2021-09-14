---
title: BUTTONGROUP.cursor
description: El atributo cursor especifica o recupera el tipo de cursor que aparece cuando el mouse está sobre un botón en BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- ButtonGROUP.cursor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889268"
---
# <a name="buttongroupcursor"></a>BUTTONGROUP.cursor

El **atributo** cursor especifica o recupera el tipo de cursor que aparece cuando el mouse está sobre un botón en **BUTTONGROUP**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno de los valores siguientes.



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                      |
| Mano             | Mano.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta hacia el nordeste y el suroeste.                                      |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                              |
| sizenwse         | Flecha de doble punta que apunta al sudeste y al sudeste.                                      |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                                |
| uparrow          | Flecha vertical que apunta hacia arriba.                                                             |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz). |



 

## <a name="remarks"></a>Observaciones

El cursor especificado se aplica a todos los botones de **BUTTONGROUP.**

Si especifica un valor de cursor no válido, permanece en el valor establecido anteriormente.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 






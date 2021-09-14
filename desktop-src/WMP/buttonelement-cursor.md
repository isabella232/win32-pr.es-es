---
title: BUTTONELEMENT.cursor
description: El atributo cursor especifica o recupera el valor del cursor BUTTONELEMENT que aparece cuando el mouse está sobre BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- ButtonELEMENT.cursor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889353"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT.cursor

El **atributo** cursor especifica o recupera el valor del cursor **BUTTONELEMENT** que aparece cuando el mouse está sobre **BUTTONELEMENT.**

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Value            | Descripción                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                      |
| Mano             | Mano.                                                                                       |
| help             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                      |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                   |
| sizenesw         | Flecha de doble punta que apunta hacia el noreste y el suroeste.                                      |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                              |
| sizenwse         | Flecha de doble punta que apunta al noroeste y al sudeste.                                      |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                                |
| arriba          | Flecha vertical que apunta hacia arriba.                                                             |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz). |



 

## <a name="remarks"></a>Observaciones

Si se especifica un valor no válido, se mantiene el valor anterior.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> </dl>

 

 






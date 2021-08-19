---
title: BUTTON.cursor
description: El atributo cursor especifica o recupera el cursor que aparece cuando el puntero del mouse mantiene el puntero sobre button.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Button.cursor Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa98c91080bc6d108e8ab62f0de99758c4eb6ba4229a83f8ded8b22bb2ec9695
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123795"
---
# <a name="buttoncursor"></a>BUTTON.cursor

El **atributo de cursor** especifica o recupera el cursor que aparece cuando el puntero del mouse mantiene el puntero sobre **button**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura y **escritura.**



| Value            | Descripción                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                     |
| Mano             | Mano.                                                                                      |
| ayuda             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                     |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                  |
| sizenesw         | Flecha de doble punta que apunta hacia el nordeste y el suroeste.                                     |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                             |
| sizenwse         | Flecha de doble punta que apunta al sudeste y al sudeste.                                     |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                               |
| uparrow          | Flecha vertical que apunta hacia arriba.                                                            |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz) |



 

## <a name="remarks"></a>Comentarios

Si el sistema no reconoce el valor de cursor especificado, el valor del cursor permanece en el valor establecido anteriormente.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 






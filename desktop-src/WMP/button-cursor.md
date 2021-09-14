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
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889513"
---
# <a name="buttoncursor"></a>BUTTON.cursor

El **atributo** cursor especifica o recupera el cursor que aparece cuando el puntero del mouse mantiene el puntero sobre **button**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**



| Value            | Descripción                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| sistema           | Predeterminada. Cursor dependiente de la plataforma (normalmente una flecha).                                     |
| Mano             | Mano.                                                                                      |
| help             | Flecha con signo de interrogación que indica que la Ayuda está disponible.                                     |
| sizeall          | Flecha de cuatro puntas que apunta al norte, sur, este y oeste.                                  |
| sizenesw         | Flecha de doble punta que apunta hacia el noreste y el suroeste.                                     |
| sizens           | Flecha de doble punta que apunta hacia el norte y el sur.                                             |
| sizenwse         | Flecha de doble punta que apunta al noroeste y al sudeste.                                     |
| sizewe           | Flecha de doble punta que apunta hacia el oeste y el este.                                               |
| arriba          | Flecha vertical que apunta hacia arriba.                                                            |
| \*.ani o \* .cur | Cualquier archivo .ani o .cur (debe estar en el mismo directorio que el archivo .wms o en el archivo .wmz) |



 

## <a name="remarks"></a>Observaciones

Si el sistema no reconoce el valor de cursor especificado, el valor del cursor permanece en el valor establecido anteriormente.

Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 






---
title: Controls.currentPosition
description: La propiedad currentPosition especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls.currentPosition Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be64d23b65a396cfb15e9f7b19b4571bdb26cbb7f308241e9a381375b9d26a40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341882"
---
# <a name="controlscurrentposition"></a>Controls.currentPosition

La **propiedad currentPosition** especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** (**double**).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa currentPosition** para buscar una posición proporcionada por el usuario. Se crea un elemento HTML BUTTON para ejecutar el JScript código. Se creó un elemento de entrada HTML TEXT, denominado setPosition, para aceptar un valor, en segundos, del usuario. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 






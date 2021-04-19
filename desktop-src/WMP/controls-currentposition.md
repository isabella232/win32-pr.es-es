---
title: Controls. currentPosition
description: La propiedad currentPosition especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Media Player de Windows Controls. currentPosition
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
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700131"
---
# <a name="controlscurrentposition"></a>Controls. currentPosition

La propiedad **currentPosition** especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura/escritura (**Double**).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **currentPosition** para buscar una posición proporcionada por el usuario. Se crea un elemento de botón HTML para ejecutar el código JScript. Se creó un elemento de entrada de texto HTML, denominado setPosition, para aceptar un valor, en segundos, del usuario. El objeto **Player** se creó con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> </dl>

 

 






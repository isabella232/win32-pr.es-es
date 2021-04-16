---
title: Error. clearErrorQueue (método)
description: El método clearErrorQueue borra los errores de la cola de errores. | Error. clearErrorQueue (método)
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- método clearErrorQueue de Windows Media Player
- método clearErrorQueue Windows Media Player, clase error
- Clase de error Windows Media Player, método clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699589"
---
# <a name="errorclearerrorqueue-method"></a>Error. clearErrorQueue (método)

El método **clearErrorQueue** borra los errores de la cola de errores.

## <a name="syntax"></a>Sintaxis


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método es útil para borrar la cola de errores después de haber procesado una serie de errores.

Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *error*. **clearErrorQueue** en un controlador de eventos para vaciar la cola de errores después de que se muestren todas las descripciones de errores. El objeto **Player** se creó con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> </dl>

 

 






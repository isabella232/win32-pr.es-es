---
title: Método Error.clearErrorQueue
description: El método clearErrorQueue borra los errores de la cola de errores. | Método Error.clearErrorQueue
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- Método clearErrorQueue Reproductor de Windows Media
- Método clearErrorQueue Reproductor de Windows Media , clase Error
- Clase de error Reproductor de Windows Media método , clearErrorQueue
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
ms.openlocfilehash: 5a7a9fb271cab684c1263db4f0c89655855fdcb341dae20d1a828150ab84b81b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838019"
---
# <a name="errorclearerrorqueue-method"></a>Método Error.clearErrorQueue

El **método clearErrorQueue** borra los errores de la cola de errores.

## <a name="syntax"></a>Sintaxis


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método es útil para borrar la cola de errores después de procesar una serie de errores.

Debe establecer *Configuración*. **enableErrorDialogs en** false si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *error*. **clearErrorQueue en** un controlador de eventos para vaciar la cola de errores después de mostrar todas las descripciones de errores. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> </dl>

 

 






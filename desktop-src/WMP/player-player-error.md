---
title: Player. error (evento)
description: El evento de error se produce cuando hay una condición de error.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Evento de error de Windows Media Player
- Evento de error Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento de error
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708964"
---
# <a name="playererror-event"></a>Player. error (evento)

El evento de **error** se produce cuando hay una condición de error.

## <a name="syntax"></a>Sintaxis


```JScript
Player.Error()
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se crea un controlador de eventos para mostrar el texto de Descripción del primer error en la cola de errores. El objeto **Player** se creó con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Error. Item**](error-item.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 






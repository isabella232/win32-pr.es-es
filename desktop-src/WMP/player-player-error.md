---
title: Evento Player.Error
description: El evento Error se produce cuando hay una condición de error.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Evento de error Reproductor de Windows Media
- Evento de error Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , Error event
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
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134818"
---
# <a name="playererror-event"></a>Evento Player.Error

El **evento Error** se produce cuando hay una condición de error.

## <a name="syntax"></a>Sintaxis


```JScript
Player.Error()
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se crea un controlador de eventos para mostrar el texto de descripción del primer error en la cola de errores. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ErrorItem.errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Error.item**](error-item.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 






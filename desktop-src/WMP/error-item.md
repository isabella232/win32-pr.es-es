---
title: Método Error.item
description: El método item recupera un objeto ErrorItem de la cola de errores.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método item Reproductor de Windows Media
- método item Reproductor de Windows Media , Clase Error
- Clase de error Reproductor de Windows Media , método de elemento
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339700"
---
# <a name="erroritem-method"></a>Método Error.item

El **método item** recupera un objeto **ErrorItem** de la cola de errores.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice del **objeto ErrorItem** que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto ErrorItem.**

## <a name="remarks"></a>Comentarios

Reproductor de Windows Media puede generar una serie de errores en respuesta a una condición de error. Este método permite la recuperación de un error específico en la cola mediante un número de índice. Los números de índice de la cola de errores comienzan por cero.

Debe establecer *Configuración*. **enableErrorDialogs en** false si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se usa *el error*. **Objeto** item en un controlador de eventos para alertar al usuario del error más reciente. El **objeto Player** se creó con id. = "Player".


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 






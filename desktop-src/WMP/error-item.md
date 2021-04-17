---
title: Error. Item (método)
description: El método Item recupera un objeto ErrorItem de la cola de errores.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase error
- Clase de error Windows Media Player, Item (método)
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
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698606"
---
# <a name="erroritem-method"></a>Error. Item (método)

El método **Item** recupera un objeto **ErrorItem** de la cola de errores.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice del objeto **ErrorItem** que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **ErrorItem** .

## <a name="remarks"></a>Observaciones

Windows Media Player puede generar una serie de errores en respuesta a una condición de error. Este método permite la recuperación de un error específico en la cola mediante el uso de un número de índice. Los números de índice de la cola de errores comienzan por cero.

Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *error*. objeto de **elemento** en un controlador de eventos para avisar al usuario del error más reciente. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 






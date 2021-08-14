---
title: Error.errorCount
description: La propiedad errorCount recupera el número de errores de la cola de errores.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Error.errorCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99275930155724f47b77de4f85905b92de9d7a7eb612ab713d725a16c1239d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339807"
---
# <a name="errorerrorcount"></a>Error.errorCount

La **propiedad errorCount** recupera el número de errores de la cola de errores.

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Debe establecer *Configuración*. **enableErrorDialogs en** false si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *error*. **errorCount** en un controlador de eventos para alertar al usuario sobre el error más reciente en la cola de errores. El **objeto Player** se creó con id. = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

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
</dt> </dl>

 

 






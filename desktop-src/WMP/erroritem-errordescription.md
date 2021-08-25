---
title: ErrorItem.errorDescription
description: La propiedad errorDescription recupera una descripción del error.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem.errorDescription Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862795"
---
# <a name="erroritemerrordescription"></a>ErrorItem.errorDescription

La **propiedad errorDescription** recupera una descripción del error.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Comentarios

Debe establecer *Configuración*. **enableErrorDialogs en** false si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa ErrorItem*. **errorDescription** en un controlador de eventos para mostrar el mensaje de error al usuario. El **objeto Player** se creó con id. = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/>                               |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 






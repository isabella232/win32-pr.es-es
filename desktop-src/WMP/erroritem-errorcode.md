---
title: ErrorItem.errorCode
description: La propiedad errorCode recupera el código de error actual.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem.errorCode Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f426bbaf1092b64cdb3578cb681282c9b27d9d2e2e23a69d50f9c065353ad104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577709"
---
# <a name="erroritemerrorcode"></a>ErrorItem.errorCode

La **propiedad errorCode** recupera el código de error actual.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Debe establecer *Configuración*. **enableErrorDialogs en** false si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa ErrorItem*. **errorCode** en un controlador de eventos para mostrar el código de error al usuario. El **objeto Player** se creó con id. = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**ErrorItem.errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 






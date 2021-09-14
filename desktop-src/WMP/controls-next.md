---
title: Método Controls.next
description: El método siguiente establece el elemento actual en el siguiente elemento de la lista de reproducción.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- next method Reproductor de Windows Media
- next method Reproductor de Windows Media , Controls (Clase)
- Clase Controls Reproductor de Windows Media , método next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967696"
---
# <a name="controlsnext-method"></a>Método Controls.next

El **método siguiente** establece el elemento actual en el siguiente elemento de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.next()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la lista de reproducción  está en la última entrada cuando se invoca next, la primera entrada de la lista de reproducción se convertirá en la actual.

En el caso de las listas de reproducción del lado servidor, este método omite el siguiente elemento de la lista de reproducción del lado servidor, no la lista de reproducción del cliente.

Al reproducir un DVD, este método omite el siguiente capítulo lógico de la secuencia de reproducción, que puede no ser el siguiente capítulo de la lista de reproducción. Al reproducir los archivos de DVD, este método pasa al siguiente modo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **next** para pasar al siguiente elemento de la lista de reproducción actual. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.previous**](controls-previous.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 






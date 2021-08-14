---
title: Método Controls.stop
description: El método stop detiene la reproducción del elemento multimedia. | Método Controls.stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- método stop Reproductor de Windows Media
- método stop Reproductor de Windows Media , clase Controls
- Clase Controls Reproductor de Windows Media método , stop
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580164"
---
# <a name="controlsstop-method"></a>Método Controls.stop

El **método stop** detiene la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método hace que Reproductor de Windows Media liberar todos los recursos del sistema que usa, como el dispositivo de audio. Sin embargo, el elemento multimedia actual no se libera.

Cuando se detiene el reproductor, la pista rebobina al principio. Al llamar **a play,** se iniciará la reproducción del clip desde el principio. Para detener una operación de reproducción sin cambiar la posición actual, use el **método pause.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **stop** para detener la reproducción. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.pause**](controls-pause.md)
</dt> <dt>

[**Controls.previous**](controls-previous.md)
</dt> </dl>

 

 






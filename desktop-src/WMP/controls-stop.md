---
title: Controls. STOP (método)
description: El método Stop detiene la reproducción del elemento multimedia. | Controls. STOP (método)
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- detener el método Windows Media Player
- método STOP Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método STOP
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
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699605"
---
# <a name="controlsstop-method"></a>Controls. STOP (método)

El método **Stop** detiene la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método hace que Windows Media Player libere cualquier recurso del sistema que esté usando, como el dispositivo de audio. Sin embargo, el elemento multimedia actual no se libera.

Cuando se detiene el reproductor, la pista se rebobina hasta el principio. La llamada a **Play** iniciará la reproducción del clip desde el principio. Para detener una operación de reproducción sin cambiar la posición actual, use el método **PAUSE** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa **Stop** para detener la reproducción. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. Next**](controls-next.md)
</dt> <dt>

[**Controls. PAUSE**](controls-pause.md)
</dt> <dt>

[**Controls. Previous**](controls-previous.md)
</dt> </dl>

 

 






---
title: Controls. PAUSE (método)
description: El método PAUSE pausa la reproducción del elemento multimedia. | Controls. PAUSE (método)
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pausar el método Windows Media Player
- pausar método Windows Media Player, clase Controls
- Clase Controls Windows Media Player, PAUSE (método)
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700037"
---
# <a name="controlspause-method"></a>Controls. PAUSE (método)

El método **PAUSE pausa** la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.pause()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un archivo está en pausa, Windows Media Player no proporciona ningún recurso del sistema, como el dispositivo de audio.

Algunos tipos de medios no se pueden pausar, como las secuencias en directo. Para determinar si se puede pausar un tipo de medio determinado, use *los controles*. **isavailable (' Pause ')**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa **PAUSE** para pausar la reproducción. El objeto **Player** se creó con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
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

[**Controls. isAvailable**](controls-isavailable.md)
</dt> </dl>

 

 






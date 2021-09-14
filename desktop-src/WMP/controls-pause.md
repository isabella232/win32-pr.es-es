---
title: Método Controls.pause
description: El método pause pausa la reproducción del elemento multimedia. | Método Controls.pause
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pausar método Reproductor de Windows Media
- pause method Reproductor de Windows Media , Clase Controls
- Clase Controls Reproductor de Windows Media , método pause
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967683"
---
# <a name="controlspause-method"></a>Método Controls.pause

El **método pause** pausa la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.pause()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un archivo está en pausa, Reproductor de Windows Media no entrega ningún recurso del sistema, como el dispositivo de audio.

Algunos tipos de medios no se pueden pausar, como las secuencias en vivo. Para determinar si se puede pausar un tipo de medio determinado, use *Controles*. **isAvailable('Pause')**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **la pausa para** pausar la reproducción. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> </dl>

 

 






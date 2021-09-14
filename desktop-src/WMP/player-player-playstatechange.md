---
title: Evento Player.PlayStateChange
description: El evento PlayStateChange tiene lugar cuando se produce un cambio en la propiedad playState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Evento PlayStateChange Reproductor de Windows Media
- Evento PlayStateChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068363"
---
# <a name="playerplaystatechange-event"></a>Evento Player.PlayStateChange

El **evento PlayStateChange** tiene lugar cuando se produce un cambio en la **propiedad playState.**

## <a name="syntax"></a>Sintaxis


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewState* 
</dt> <dd>

Number (**long**) que especifica el nuevo **elemento playState.** Consulte [playState para](player-playstate.md) obtener una tabla de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

Reproductor de Windows Media se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un controlador de eventos para el *reproductor*. **evento playStateChange.** Un elemento de texto HTML, denominado "myText", muestra el nuevo estado de reproducción. El objeto player se creó con id. = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> </dl>

 

 






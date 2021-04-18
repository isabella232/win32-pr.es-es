---
title: Evento Player. PlayStateChange
description: El evento PlayStateChange se produce cuando hay un cambio en la propiedad playState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player PlayStateChange de eventos de Windows
- Evento PlayStateChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlayStateChange
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708293"
---
# <a name="playerplaystatechange-event"></a>Evento Player. PlayStateChange

El evento **PlayStateChange** se produce cuando hay un cambio en la propiedad **playState** .

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

Número (**Long**) que especifica el nuevo **playState**. Consulte [playState](player-playstate.md) para obtener una tabla de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado. Además, no todos los Estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de los Estados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un controlador de eventos para el *reproductor*. evento **playStateChange** . Un elemento de texto HTML, denominado "mi texto", muestra el nuevo estado de reproducción. El objeto Player se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player. playState**](player-playstate.md)
</dt> </dl>

 

 






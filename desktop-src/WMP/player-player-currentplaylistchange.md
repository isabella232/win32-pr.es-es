---
title: Evento Player. CurrentPlaylistChange
description: El evento CurrentPlaylistChange se produce cuando hay algún cambio en la lista de reproducción actual. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Media Player CurrentPlaylistChange de eventos de Windows
- Evento CurrentPlaylistChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708646"
---
# <a name="playercurrentplaylistchange-event"></a>Evento Player. CurrentPlaylistChange

El evento **CurrentPlaylistChange** se produce cuando hay algún cambio en la lista de reproducción actual.

## <a name="syntax"></a>Sintaxis


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*change* 
</dt> <dd>

**Número** (**largo**) que indica el tipo de cambio que se ha producido en la lista de reproducción. Vea el *reproductor*. Evento **PlaylistChange** para una tabla de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento no se produce cuando una lista de reproducción distinta se convierte en la lista de reproducción actual. Solo se produce cuando se produce un cambio en la lista de reproducción actual, como un elemento multimedia que se anexa a la lista de reproducción.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se actualiza el texto de un elemento HTML DIV, denominado PlItems, para mostrar los nombres de los elementos multimedia de la lista de reproducción actual. El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
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

[**Player. currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player. PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 






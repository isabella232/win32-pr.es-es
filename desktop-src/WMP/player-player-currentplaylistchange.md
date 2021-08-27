---
title: Evento Player.CurrentPlaylistChange
description: El evento CurrentPlaylistChange tiene lugar cuando algo cambia en la lista de reproducción actual. | Evento Player.CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Evento CurrentPlaylistChange Reproductor de Windows Media
- Evento CurrentPlaylistChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , CurrentPlaylistChange
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
ms.openlocfilehash: 672ff739e60efe73e1d30670dec5bc956f9fdd56506464b036add6f52cc6fc34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338151"
---
# <a name="playercurrentplaylistchange-event"></a>Evento Player.CurrentPlaylistChange

El **evento CurrentPlaylistChange** tiene lugar cuando algo cambia dentro de la lista de reproducción actual.

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

**Number** ( long )**que** indica qué tipo de cambio se produjo en la lista de reproducción. Consulte el *reproductor*. **Evento PlaylistChange** para una tabla de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este evento no se produce cuando otra lista de reproducción se convierte en la lista de reproducción actual. Solo se produce cuando se produce un cambio dentro de la lista de reproducción actual, como un elemento multimedia que se anexa a la lista de reproducción.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se actualiza el texto de un elemento DIV HTML, denominado PlItems, para mostrar los nombres de los elementos multimedia en la lista de reproducción actual. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.currentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**Player.PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 






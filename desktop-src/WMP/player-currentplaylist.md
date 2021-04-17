---
title: Player. currentPlaylist
description: La propiedad currentPlaylist especifica o recupera el objeto de lista de reproducción actual.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Media Player de Windows Player. currentPlaylist
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700018"
---
# <a name="playercurrentplaylist"></a>Player. currentPlaylist

La propiedad currentPlaylist especifica o recupera el objeto de **lista de reproducción** actual.

## <a name="syntax"></a>Sintaxis

*reproductor* . **currentPlaylist**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto de **lista de reproducción** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Es si se trata de la *configuración*. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentPlaylist**.

Esta propiedad toma un objeto de lista de reproducción, que se puede adquirir de varias maneras, por ejemplo, mediante una llamada a *PlaylistArray*. **elemento** o *PlaylistCollection*. **reproducción**. Para cargar un elemento de **lista de reproducción** con un nombre de archivo, establezca la propiedad URL o use *Player*. **reproducción**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se recupera la primera lista de reproducción de la biblioteca. A continuación, usa **currentPlaylist** para que la lista de reproducción recuperada sea la lista de reproducción actual y, a continuación, muestre el nombre de la lista de reproducción actual. El objeto **Player** se creó con ID = "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
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

[**Player. reproducción**](player-newplaylist.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistArray. Item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection. reproducción**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Configuración. Inicio automático**](settings-autostart.md)
</dt> </dl>

 

 






---
title: Player.currentPlaylist
description: La propiedad currentPlaylist especifica o recupera el objeto Playlist actual.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player.currentPlaylist Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242421"
---
# <a name="playercurrentplaylist"></a>Player.currentPlaylist

La propiedad currentPlaylist especifica o recupera el objeto **Playlist** actual.

## <a name="syntax"></a>Sintaxis

*player* . **currentPlaylist**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un  objeto Playlist de lectura/escritura.

## <a name="remarks"></a>Observaciones

Si el *Configuración*. **La propiedad autoStart** es true, la reproducción comienza automáticamente cada vez que se **establece currentPlaylist.**

Esta propiedad toma un objeto Playlist, que se puede adquirir de varias maneras, como llamando a *PlaylistArray*. **item** o *PlaylistCollection*. **newPlaylist**. Para cargar un elemento **de lista de** reproducción con un nombre de archivo, establezca la propiedad URL o use *player*. **newPlaylist**.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se recupera la primera lista de reproducción de la biblioteca. A continuación, **usa currentPlaylist** para que la lista de reproducción recuperada sea la lista de reproducción actual y, a continuación, para mostrar el nombre de la lista de reproducción actual. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**PlaylistArray.item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Configuración.autoStart**](settings-autostart.md)
</dt> </dl>

 

 






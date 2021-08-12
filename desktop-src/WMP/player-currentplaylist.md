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
ms.openlocfilehash: 7139c567eab5fbb3c324916dec260d34f57429cb50bb99d199f35be8aee7a1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573220"
---
# <a name="playercurrentplaylist"></a>Player.currentPlaylist

La propiedad currentPlaylist especifica o recupera el objeto **Playlist** actual.

## <a name="syntax"></a>Syntax

*player* . **currentPlaylist**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto Playlist de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Si el *Configuración*. **La propiedad autoStart** es true, la reproducción comienza automáticamente cada vez que se **establece currentPlaylist**.

Esta propiedad toma un objeto Playlist, que se puede adquirir de varias maneras, como llamando a *PlaylistArray*. **item** o *PlaylistCollection*. **newPlaylist**. Para cargar un elemento **de lista de** reproducción con un nombre de archivo, establezca la propiedad URL o use el Reproductor *de*. **newPlaylist**.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se recupera la primera lista de reproducción de la biblioteca. A continuación, **usa currentPlaylist** para convertir la lista de reproducción recuperada en la lista de reproducción actual y, a continuación, para mostrar el nombre de la lista de reproducción actual. El **objeto Player** se creó con id. = "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 






---
title: Método Player.newPlaylist
description: El método newPlaylist crea un nuevo objeto Playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Método newPlaylist Reproductor de Windows Media
- Método newPlaylist Reproductor de Windows Media , Clase Player
- Clase player Reproductor de Windows Media método , newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380d1f2751487f5c648b154852be625a5c93103851541dea7e2488ba75080ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572835"
---
# <a name="playernewplaylist-method"></a>Método Player.newPlaylist

El **método newPlaylist** crea un nuevo objeto **Playlist.**

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre de la nueva lista de reproducción.

</dd> <dt>

*DIRECCIÓN URL* \[ En\]
</dt> <dd>

**Cadena** que contiene la dirección URL de la lista de Windows de metarchivo multimedia con la que crear el objeto **Playlist.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Si el *parámetro url* se establece en null o "" (cadena vacía), se creará un objeto **De lista** de reproducción vacío. Si el *parámetro name* se establece en "", se usa el nombre del metarchivo.

La nueva lista de reproducción creada con este método no se agrega a la biblioteca. Para agregar una nueva lista de reproducción a la biblioteca, use *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **newPlaylist**. Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agrega a la biblioteca.

Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que quiera comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows Metarchivos multimedia**](windows-media-metafiles.md)
</dt> </dl>

 

 






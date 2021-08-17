---
title: IWMPMedia isMemberOf (método)
description: El método isMemberOf devuelve un valor que indica si el elemento multimedia especificado es miembro de la lista de reproducción especificada.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- Método isMemberOf Reproductor de Windows Media
- Método isMemberOf Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media , método isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485121f0ac9c4c441ff90e34b90ef5c9475c22995565b018d3f0e00dc5d94740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746020"
---
# <a name="iwmpmediaismemberof-method"></a>IWMPMedia::isMemberOf (método)

El **método isMemberOf** devuelve un valor que indica si el elemento multimedia especificado es miembro de la lista de reproducción especificada.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPlaylist* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPPlaylist.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor **System.Boolean** que indica si el elemento multimedia es miembro de la lista de reproducción.

## <a name="remarks"></a>Comentarios

Este método no puede comprobar las listas de reproducción recuperadas a través de **la interfaz IWMPMediaCollection.** Para probar si un elemento multimedia es miembro de una lista de reproducción con nombre determinada, recupere la colección de listas de reproducción con la propiedad **AxWindowsMediaPlayer.playlistCollection.** Una vez recuperada la colección, recupere la lista de reproducción individual llamando al **método IWMPPlaylistCollection.getByName.**

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa isMemberOf** para probar si el elemento multimedia actual es miembro de la lista de reproducción denominado All Música. Si no es así, el elemento multimedia actual se anexa a la lista de reproducción. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.playlistCollection (VB y C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






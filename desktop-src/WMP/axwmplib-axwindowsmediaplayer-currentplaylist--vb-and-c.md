---
title: Propiedad AxWindowsMediaPlayer. currentPlaylist
description: La propiedad currentPlaylist obtiene o establece la interfaz IWMPPlaylist actual que proporciona una manera sencilla de organizar y manipular los elementos multimedia de una lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- propiedades de currentPlaylist Media Player de Windows
- propiedad currentPlaylist Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699938"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Propiedad AxWindowsMediaPlayer. currentPlaylist

La propiedad currentPlaylist obtiene o establece la interfaz **IWMPPlaylist** actual que proporciona una manera sencilla de organizar y manipular los elementos multimedia de una lista.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valor de propiedad

La interfaz WMPLib. IWMPPlaylist que proporciona acceso a la lista de reproducción actual.

## <a name="remarks"></a>Observaciones

Si la propiedad IWMPSettings. autoStart (también tiene acceso a través de AxWindowsMediaPlayer. Settings.**autoStart**) es true, la reproducción se inicia automáticamente cada vez que se establece **currentPlaylist**.

Esta propiedad toma una interfaz IWMPPlaylist, que se puede adquirir de varias maneras, por ejemplo, obteniendo el valor de *IWMPPlaylistArray*. **Elemento** o *IWMPPlaylistCollection*. propiedades de **reproducción** . Para cargar un elemento de **lista de reproducción** con un nombre de archivo, establezca la propiedad URL o use AxWindowsMediaPlayer. **reproducción**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se recupera la primera lista de reproducción de la biblioteca y se usa la propiedad currentPlaylist para establecer la lista de reproducción recuperada como la lista de reproducción actual y se muestra su nombre. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. reproducción (VB y C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Settings (VB y C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Item (VB y C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. reproducción (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autoStart (VB y C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






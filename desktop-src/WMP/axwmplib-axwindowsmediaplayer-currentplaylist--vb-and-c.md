---
title: Propiedad AxWindowsMediaPlayer.currentPlaylist
description: La propiedad currentPlaylist obtiene o establece la interfaz IWMPPlaylist actual que proporciona una manera sencilla de organizar y manipular elementos multimedia en una lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- propiedad currentPlaylist Reproductor de Windows Media
- propiedad currentPlaylist Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad currentPlaylist
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
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765274"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>Propiedad AxWindowsMediaPlayer.currentPlaylist

La propiedad currentPlaylist obtiene o establece la interfaz **IWMPPlaylist** actual que proporciona una manera sencilla de organizar y manipular elementos multimedia en una lista.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valor de propiedad

Interfaz WMPLib.IWMPPlaylist que proporciona acceso a la lista de reproducción actual.

## <a name="remarks"></a>Comentarios

Si la propiedad IWMPSettings.autoStart (también se accede a través de AxWindowsMediaPlayer.settings).**autoStart**) es true, la reproducción comienza automáticamente cada vez que se **establece currentPlaylist.**

Esta propiedad toma una interfaz IWMPPlaylist, que se puede adquirir de varias maneras, como al obtener el valor de *IWMPPlaylistArray*. **Item** o *IWMPPlaylistCollection*. **propiedades newPlaylist.** Para cargar un elemento **de lista** de reproducción con un nombre de archivo, establezca la propiedad URL o use AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se recupera la primera lista de reproducción de la biblioteca y se usa la propiedad currentPlaylist para establecer la lista de reproducción recuperada como la lista de reproducción actual y mostrar su nombre. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


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



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.newPlaylist (VB y C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer.settings (VB y C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.Item (VB y C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB y C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






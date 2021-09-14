---
title: Evento PlaylistCollectionPlaylist Agregado del objeto AxWindowsMediaPlayer
description: El evento PlaylistCollectionPlaylistAdded tiene lugar cuando se agrega una lista de reproducción a la colección de listas de reproducción. | Evento PlaylistCollectionPlaylist Agregado del objeto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- PlaylistCollectionPlaylist Evento agregado del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889628"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylist Agregado del objeto AxWindowsMediaPlayer

El evento PlaylistCollectionPlaylistAdded tiene lugar cuando se agrega una lista de reproducción a la colección de listas de reproducción.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad             | Descripción                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | System.String Especifica el nombre de la lista de reproducción que se agregó.<br/> |



 

## <a name="remarks"></a>Observaciones

El nombre de la lista de reproducción que se agregó se puede usar para recuperar la lista de reproducción correspondiente mediante IWMPPlaylistCollection. **Método getByName.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer
description: El evento PlaylistCollectionPlaylistSetAsDeleted está reservado para su uso futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889620"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistSetAsDeleted del objeto AxWindowsMediaPlayer

El evento PlaylistCollectionPlaylistSetAsDeleted está reservado para su uso futuro.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad         | Descripción                                 |
|------------------|---------------------------------------------|
| bstrPlaylistName | **System.String** No se admite.<br/>  |
| varfIsDeleted    | **System.Boolean** No se admite.<br/> |



 

## <a name="remarks"></a>Observaciones

Este evento está reservado para su uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer
description: El evento CurrentPlaylistItemAvailable tiene lugar cuando la lista de reproducción actual está disponible. | Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e80eac2720d7035d68fa3e94efcaf3205287cd04795a6ccf99c36106d797a8a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098789"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentPlaylistItemAvailable del objeto AxWindowsMediaPlayer

El evento CurrentPlaylistItemAvailable tiene lugar cuando la lista de reproducción actual está disponible.

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad         | Descripción                                                    |
|------------------|----------------------------------------------------------------|
| **bstrItemName** | System.StringEl nombre del elemento de lista de reproducción actual.<br/> |



 

## <a name="remarks"></a>Comentarios

El nombre de la lista de reproducción actual se puede usar para recuperar la interfaz **IWMPPlaylist correspondiente** de la interfaz IWMPPlaylistArray que se devuelve del método IWMPPlaylistCollection.getByName.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






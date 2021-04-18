---
title: Evento PlaylistChange del objeto AxWindowsMediaPlayer
description: El evento PlaylistChange se produce cuando cambia una lista de reproducción. | Evento PlaylistChange del objeto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700223"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistChange del objeto AxWindowsMediaPlayer

El evento PlaylistChange se produce cuando cambia una lista de reproducción.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad     | Descripción                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **automáticas** | Objeto System. ObjectThe que cambió. Puede convertirlo en una interfaz IWMPPlaylist para tener acceso a él.<br/>                |
| **change**   | Valor de enumeración WMPLib. WMPPlaylistChangeEventTypeAn que indica el tipo de cambio que se produjo en la lista de reproducción.<br/> |



 

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

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 






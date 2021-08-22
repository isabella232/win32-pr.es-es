---
title: Evento PlaylistChange del objeto AxWindowsMediaPlayer
description: El evento PlaylistChange tiene lugar cuando cambia una lista de reproducción. | Evento PlaylistChange del objeto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
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
ms.openlocfilehash: 994c16ef79ad308e363e8cad4586cdbf0cca90a168d9bcb59ae6f943d108b74d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841224"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistChange del objeto AxWindowsMediaPlayer

El evento PlaylistChange tiene lugar cuando cambia una lista de reproducción.

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
| **Reproducción** | System.ObjectEl objeto que ha cambiado. Puede convertir esto en una interfaz IWMPPlaylist para acceder a ella.<br/>                |
| **change**   | WMPLib.WMPPlaylistChangeEventTypeAn valor de enumeración que indica el tipo de cambio que se produjo en la lista de reproducción.<br/> |



 

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

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 






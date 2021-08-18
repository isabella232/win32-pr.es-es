---
title: Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer
description: El evento OpenPlaylistSwitch tiene lugar cuando un título de un DVD comienza a reproducirse. | Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57341488c385b159ce294626a79b7e22287bff83864f7273b0f4432c1db95ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764705"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>Evento OpenPlaylistSwitch del objeto AxWindowsMediaPlayer

El evento OpenPlaylistSwitch tiene lugar cuando un título de un DVD comienza a reproducirse.

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad  | Descripción                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pItem** | System.ObjectObject que representa el título. Puede convertir esto en una interfaz IWMPPlaylist para acceder a ella.<br/> |



 

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
</dt> </dl>

 

 






---
title: Evento LibraryDisconnect del objeto AxWindowsMediaPlayer
description: El evento LibraryDisconnect tiene lugar cuando una biblioteca ya no está disponible.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a032dc95a68430768b0f2aa109a56dae80cdaecb14b67eb5dbf6b2657cdd5107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136008"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento LibraryDisconnect del objeto AxWindowsMediaPlayer

El evento LibraryDisconnect tiene lugar cuando una biblioteca ya no está disponible.

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ Biblioteca \_ WMPOCXEventsDisconnectEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** Interfaz que representa la biblioteca desconectada.<br/> |



 

## <a name="remarks"></a>Comentarios

Este evento no se produce para la biblioteca local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                         |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 






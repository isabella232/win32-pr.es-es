---
title: Evento LibraryDisconnect del objeto AxWindowsMediaPlayer
description: El evento LibraryDisconnect se produce cuando una biblioteca ya no está disponible.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700161"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento LibraryDisconnect del objeto AxWindowsMediaPlayer

El evento LibraryDisconnect se produce cuando una biblioteca ya no está disponible.

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

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib. IWMPLibrary** La interfaz que representa la biblioteca que se ha desconectado.<br/> |



 

## <a name="remarks"></a>Observaciones

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

 

 






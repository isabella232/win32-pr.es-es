---
title: Evento Disconnect del objeto AxWindowsMediaPlayer
description: El evento Disconnect está reservado para su uso futuro.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Evento Disconnect del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0554de8fe71ae13e510733ed2204ff4ed79d575a40f23a1769a5fb36eeb560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902705"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento Disconnect del objeto AxWindowsMediaPlayer

El evento Disconnect está reservado para su uso futuro.

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                               |
|----------|-------------------------------------------|
| resultado   | **System.Int32** No se admite.<br/> |



 

## <a name="remarks"></a>Comentarios

Este evento está reservado para su uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






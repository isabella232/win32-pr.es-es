---
title: Evento DurationUnitChange del objeto AxWindowsMediaPlayer
description: El evento DurationUnitChange se reserva para uso futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698556"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DurationUnitChange del objeto AxWindowsMediaPlayer

El evento DurationUnitChange se reserva para uso futuro.

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad        | Descripción                               |
|-----------------|-------------------------------------------|
| newDurationUnit | **System. Int32** No compatible.<br/> |



 

## <a name="remarks"></a>Observaciones

Este evento se reserva para uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






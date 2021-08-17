---
title: Evento DurationUnitChange del objeto AxWindowsMediaPlayer
description: El evento DurationUnitChange está reservado para su uso futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
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
ms.openlocfilehash: 1efa872389ad88a236808de64ed299dd3afc123cee59f39f1215f7a16bcb589f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136048"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DurationUnitChange del objeto AxWindowsMediaPlayer

El evento DurationUnitChange está reservado para su uso futuro.

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
| newDurationUnit | **System.Int32** No se admite.<br/> |



 

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

 

 






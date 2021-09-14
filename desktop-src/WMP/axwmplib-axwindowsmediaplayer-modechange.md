---
title: Evento ModeChange del objeto AxWindowsMediaPlayer
description: El evento ModeChange tiene lugar cuando se cambia Reproductor de Windows Media modo de cambio. | Evento ModeChange del objeto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889692"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Evento ModeChange del objeto AxWindowsMediaPlayer

El evento ModeChange tiene lugar cuando se cambia Reproductor de Windows Media modo de cambio.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad | Descripción                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | System.StringIndica el modo que se cambió. Para ver los valores posibles, vea Comentarios.<br/> |
| newValue | System.BooleanIndica el nuevo estado del modo especificado.<br/>                        |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran los valores posibles para la propiedad modeName.



| String  | Descripción                                         |
|---------|-----------------------------------------------------|
| shuffle | Las pistas se reproducen en orden aleatorio.                  |
| bucle    | Toda la secuencia de pistas se reproduce repetidamente. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.getMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 






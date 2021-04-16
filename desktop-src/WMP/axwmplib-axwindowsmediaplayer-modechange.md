---
title: Evento ModeChange del objeto AxWindowsMediaPlayer
description: El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows. | Evento ModeChange del objeto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699907"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Evento ModeChange del objeto AxWindowsMediaPlayer

El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows.

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
| modeName | System. StringIndicates el modo que se cambió. Para ver los valores posibles, vea la sección Comentarios.<br/> |
| newValue | System. BooleanIndicates el nuevo estado del modo especificado.<br/>                        |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran los posibles valores para la propiedad modeName.



| String  | Descripción                                         |
|---------|-----------------------------------------------------|
| shuffle | Las pistas se reproducen en orden aleatorio.                  |
| bucle    | Toda la secuencia de pistas se reproduce varias veces. |



 

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

[**IWMPSettings. getMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 






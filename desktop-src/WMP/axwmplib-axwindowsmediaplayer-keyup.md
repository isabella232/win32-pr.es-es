---
title: Evento KeyUp del objeto AxWindowsMediaPlayer
description: El evento KeyUp se produce cuando se suelta una tecla. | Evento KeyUp del objeto AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Evento KeyUp del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699909"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyUp del objeto AxWindowsMediaPlayer

El evento KeyUp se produce cuando se suelta una tecla.

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies Qué tecla física está presionada. Para ver los valores posibles, vea la sección Comentarios del evento KeyDown.<br/>                                                                                                                                                                                                                                                   |
| nShiftState | El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.<br/> |



 

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

 

 






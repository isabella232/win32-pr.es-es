---
title: Evento MouseMove del objeto AxWindowsMediaPlayer
description: El evento MouseMove tiene lugar cuando se mueve el puntero del mouse. | Evento MouseMove del objeto AxWindowsMediaPlayer
ms.assetid: abf20c86-3bae-4677-8901-0af030a53286
keywords:
- Evento MouseMove del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MouseMove Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608dea9e69135f0f473b9dfba175dc6e9353afe0bc7e23368c144e2a0ea1a7f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902465"
---
# <a name="mousemove-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseMove del objeto AxWindowsMediaPlayer

El evento MouseMove tiene lugar cuando se mueve el puntero del mouse.

``` syntax
[C#]
private void player_MouseMoveEvent(
  object sender,
  _WMPOCXEvents_MouseMoveEvent e
)

[Visual Basic]
Private Sub player_MouseMoveEvent(
  sender As Object,
  e As _WMPOCXEvents_MouseMoveEvent
) Handles player.MouseMoveEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | Campo de bits System.Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que produjo el evento.<br/>                                                |
| nShiftState | Campo de bits System.Int16A con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.<br/> |
| Fx          | System.Int32La coordenada x del puntero del mouse con respecto a la esquina superior izquierda del control.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32La coordenada y del puntero del mouse con respecto a la esquina superior izquierda del control.<br/>                                                                                                                                                                                                                 |



 

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

 

 






---
title: Evento MouseDown del objeto AxWindowsMediaPlayer
description: El evento MouseDown tiene lugar cuando el usuario presiona un botón del mouse. | Evento MouseDown del objeto AxWindowsMediaPlayer
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- Evento MouseDown del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73259fab6ffd268e1c9a581a4b7ba18fdfba6c1647b57ef12bcae1c3ab8c04a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509455"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseDown del objeto AxWindowsMediaPlayer

El evento MouseDown tiene lugar cuando el usuario presiona un botón del mouse.

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEvent**, que contiene las siguientes propiedades relacionadas con este evento.



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

 

 






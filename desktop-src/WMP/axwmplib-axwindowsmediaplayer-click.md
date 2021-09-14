---
title: Hacer clic en Evento del objeto AxWindowsMediaPlayer
description: El evento Click tiene lugar cuando el usuario hace clic en un botón del mouse en un control Reproductor de Windows Media control.
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- Haga clic en Evento del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889785"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a>Hacer clic en Evento del objeto AxWindowsMediaPlayer

El evento Click tiene lugar cuando el usuario hace clic en un botón del mouse en un control Reproductor de Windows Media control.

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ ClickEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ ClickEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | Campo de bits System.Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que produjo el evento.<br/>                                                |
| nShiftState | Campo de bits System.Int16A con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.<br/> |
| Fx          | System.Int32La coordenada x del puntero del mouse con respecto a la esquina superior izquierda del control.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






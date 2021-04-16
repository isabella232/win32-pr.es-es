---
title: Evento DoubleClick del objeto AxWindowsMediaPlayer
description: El evento DoubleClick se produce cuando el usuario hace doble clic en un botón del mouse en un control de Media Player de Windows.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699626"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>Evento DoubleClick del objeto AxWindowsMediaPlayer

El evento DoubleClick se produce cuando el usuario hace doble clic en un botón del mouse en un control de Media Player de Windows.

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nbotón     | Campo de bits System. Int16A con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, que indica el botón que causó el evento.<br/>                                                |
| nShiftState | El campo de bits System. Int16A con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.<br/> |
| Efectos          | System. Int32el coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.<br/>                                                                                                                                                                                                                 |
| fY          | Coordenada y de System. Int32el del puntero del mouse con respecto a la esquina superior izquierda del control.<br/>                                                                                                                                                                                                                 |



 

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

 

 






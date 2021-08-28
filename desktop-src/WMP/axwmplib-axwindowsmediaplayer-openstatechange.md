---
title: Evento OpenStateChange del objeto AxWindowsMediaPlayer
description: El evento OpenStateChange tiene lugar cuando la propiedad openState cambia de valor. | Evento OpenStateChange del objeto AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Evento OpenStateChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccf7619e86268fe6b465d2a64ca00d650a7a7051b3aa4f44e2a73a98929be13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003985"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento OpenStateChange del objeto AxWindowsMediaPlayer

El evento OpenStateChange tiene lugar cuando la **propiedad openState** cambia de valor.

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NewState | System.Int32Especifica el nuevo estado abierto. Para obtener una tabla de valores, [vea openState.](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)<br/> |



 

## <a name="remarks"></a>Comentarios

Reproductor de Windows Media puede pasar por varios estados abiertos mientras intenta abrir un archivo de red, como buscar el servidor, conectarse al servidor y, por último, abrir el archivo. Este evento se desencadena cada vez que cambia el estado de apertura.

Reproductor de Windows Media se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.openState (VB y C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 






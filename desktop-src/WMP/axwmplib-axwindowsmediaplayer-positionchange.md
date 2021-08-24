---
title: Evento PositionChange del objeto AxWindowsMediaPlayer
description: El evento PositionChange tiene lugar cuando se ha cambiado la posición de reproducción actual dentro del elemento multimedia.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269d83c92687b5debda8b70fb4d6710b55eebd5476153759ebad36e5d17657d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764685"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PositionChange del objeto AxWindowsMediaPlayer

El evento PositionChange tiene lugar cuando se ha cambiado la posición de reproducción actual dentro del elemento multimedia.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System.DoubleEspecifica la posición anterior.<br/> |
| newPosition | System.DoubleEspecifica la nueva posición.<br/> |



 

## <a name="remarks"></a>Comentarios

Este evento no se genera rutinariamente durante la reproducción. Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia de reproducción, como cuando el usuario mueve el identificador de búsqueda o cuando se ejecuta código que especifica un valor para IWMPControls. **currentPosition**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPosition (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento MediaError del objeto AxWindowsMediaPlayer
description: El evento MediaError tiene lugar cuando un objeto multimedia tiene una condición de error.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento MediaError del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83dc6bceb188ff443bfdcab904242e91b30fba80c4bae4f03cfa388cf15642b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902615"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaError del objeto AxWindowsMediaPlayer

El evento MediaError tiene lugar cuando un objeto multimedia tiene una condición de error.

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad     | Descripción                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| pMediaObject | System.ObjectObject que tiene una condición de error. Puede convertir esto en una interfaz IWMPMedia para acceder a ella.<br/> |



 

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






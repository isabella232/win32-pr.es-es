---
title: Evento MarkerHit del objeto AxWindowsMediaPlayer
description: El evento MarkerHit tiene lugar cuando se alcanza un marcador. | Evento MarkerHit del objeto AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Evento MarkerHit del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b51d1eb580937aba40fb3b8318450578cad5b2154539275701239aea27f6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841214"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a>Evento MarkerHit del objeto AxWindowsMediaPlayer

El evento MarkerHit tiene lugar cuando se alcanza un marcador.

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad      | Descripción                                                             |
|---------------|-------------------------------------------------------------------------|
| **MarkerNum** | System.Int32Indica el número del marcador que se ha alcanzado.<br/> |



 

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

 

 






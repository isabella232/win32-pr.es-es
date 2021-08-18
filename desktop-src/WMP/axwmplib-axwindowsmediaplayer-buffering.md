---
title: Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer
description: El evento de almacenamiento en búfer se produce cuando el control Reproductor de Windows Media o finaliza el almacenamiento en búfer o la descarga. | Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30cca5d7ebe91859162bd729cc32cc03f36f9e3c59ba4474d41311befcce1d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765255"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Evento de almacenamiento en búfer del objeto AxWindowsMediaPlayer

El evento de almacenamiento en búfer se produce cuando el control Reproductor de Windows Media o finaliza el almacenamiento en búfer o la descarga.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Start    | System.Boolean Especifica si el almacenamiento en búfer ha comenzado o finalizado. Un valor de true indica que ha comenzado; Un valor de false indica que ha finalizado.<br/> |



 

## <a name="remarks"></a>Comentarios

Use este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga. Puede usar el mismo bloque de eventos para ambos casos y probar *IWMPNetwork*. **bufferingProgress** e *IWMPNetwork*. **downloadProgress para** determinar si Reproductor de Windows Media almacena en búfer o descarga contenido.

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

[**IWMPNetwork.bufferingProgress (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.downloadProgress (VB y C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 






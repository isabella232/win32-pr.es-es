---
title: Evento CdromRipMediaError del objeto AxWindowsMediaPlayer
description: El evento CdromRipMediaError se produce cuando se produce un error mientras se establece una pista individual desde un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Evento CdromRipMediaError del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2be1f777c4af3385e41939743bb91a20d3d7094f1a38917b3e79686b2a2863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136197"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromRipMediaError del objeto AxWindowsMediaPlayer

El evento CdromRipMediaError se produce cuando se produce un error mientras se establece una pista individual desde un CD.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad  | Descripción                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromRip | WMPLib.IWMPCdromRipLa interfaz que representa la operación de control que produjo el error.<br/>                |
| pMedia    | System.ObjectEl elemento multimedia que produjo el error. Puede convertir esto en una interfaz IWMPMedia para acceder a ella.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                         |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromRip (VB y C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






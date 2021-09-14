---
title: Evento CdromErrorMediaError del objeto AxWindowsMediaPlayer
description: El evento CdromErrorMediaError se produce cuando se produce un error al grabar un elemento multimedia individual en un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromErrorMediaError del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889796"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromErrorMediaError del objeto AxWindowsMediaPlayer

El evento CdromErrorMediaError se produce cuando se produce un error al grabar un elemento multimedia individual en un CD.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorMediaErrorEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad   | Descripción                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromRomRom | WMPLib.IWMPCdromRomThe interfaz que representa la operación de grabación que produjo el error.<br/>               |
| pMedia     | System.ObjectEl elemento multimedia que produjo el error. Puede convertir esto en una interfaz IWMPMedia para acceder a ella.<br/> |



 

## <a name="remarks"></a>Observaciones

Para capturar errores genéricos, controle AxWMPLib. \_ Evento \_ CdromError de WMPOCXEvents.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                         |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.CdromError (VB y C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






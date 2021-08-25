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
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765275"
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



 

## <a name="remarks"></a>Comentarios

Para capturar errores genéricos, controle AxWMPLib. \_ Evento \_ CdromError de WMPOCXEvents.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                         |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.CdromError (VB y C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento de advertencia del objeto AxWindowsMediaPlayer
description: El evento Warning está reservado para su uso futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento de advertencia del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243303"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Evento de advertencia del objeto AxWindowsMediaPlayer

El evento Warning está reservado para su uso futuro.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                |
|-------------|--------------------------------------------|
| warningType | **System.Int32** No se admite.<br/>  |
| param       | **System.Int32** No se admite.<br/>  |
| description | **System.String** No se admite.<br/> |



 

## <a name="remarks"></a>Observaciones

Este evento está reservado para su uso futuro.

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

 

 






---
title: Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer
description: El evento CdromBurnMediaError tiene lugar cuando se produce un error mientras se graba un elemento multimedia individual en un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698482"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnMediaError del objeto AxWindowsMediaPlayer

El evento CdromBurnMediaError tiene lugar cuando se produce un error mientras se graba un elemento multimedia individual en un CD.

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

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad   | Descripción                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromBurn | Interfaz WMPLib. IWMPCdromBurnThe que representa la operación de grabación que provocó el error.<br/>               |
| pMedia     | Elemento multimedia System. ObjectThe que generó el error. Puede convertirlo en una interfaz IWMPMedia para tener acceso a él.<br/> |



 

## <a name="remarks"></a>Observaciones

Para capturar errores genéricos, controle el AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnError.

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

[**Evento AxWindowsMediaPlayer. CdromBurnError (VB y C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






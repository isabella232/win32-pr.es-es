---
title: Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionAttributeStringChanged tiene lugar cuando se cambia un valor de atributo en la biblioteca. | Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dcc755d1a183525923b91ce2de7937860582c3cf795d13cbf4a8c22d7c9c37f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618785"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionAttributeStringChanged del objeto AxWindowsMediaPlayer

El evento MediaCollectionAttributeStringChanged tiene lugar cuando se cambia un valor de atributo en la biblioteca.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad         | Descripción                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bstrAttribName   | System.String Especifica el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea referencia [de atributos](attribute-reference.md).<br/> |
| bstrOldAttribVal | System.String Especifica el valor anterior del atributo.<br/>                                                                                                                            |
| bstrNewAttribVal | System.String Especifica el nuevo valor del atributo.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Comentarios

Cuando un usuario modifica los metadatos de la biblioteca, la colección multimedia se actualiza y este evento se desanualizó para cada atributo cambiado.

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

[**AxWindowsMediaPlayer.mediaCollection (VB y C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






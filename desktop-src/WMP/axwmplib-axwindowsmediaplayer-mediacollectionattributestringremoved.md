---
title: Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer
description: El evento MediaCollectionAttributeStringRemoved tiene lugar cuando se quita un valor de atributo de la biblioteca. | Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56a6e997ada3296a0ec1df841797c1495ccde0864495dcf77a0a0634ccde5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582081"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionAttributeStringRemoved del objeto AxWindowsMediaPlayer

El evento MediaCollectionAttributeStringRemoved tiene lugar cuando se quita un valor de atributo de la biblioteca.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad           | Descripción                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System.String Especifica el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).<br/> |
| bstrAttribVal      | System.String Especifica el valor del atributo.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Comentarios

Cuando se quita un elemento multimedia de la biblioteca, sus metadatos se quitan de **MediaCollection** y este evento se desencadena para cada atributo quitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB y C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






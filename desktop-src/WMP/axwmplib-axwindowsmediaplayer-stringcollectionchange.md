---
title: Evento StringCollectionChange del objeto AxWindowsMediaPlayer
description: El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas. | Evento StringCollectionChange del objeto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceeba7942be4180d02a44ff19d63c10f9bc9df0bba745fdf69bcf10e97c3052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764665"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>Evento StringCollectionChange del objeto AxWindowsMediaPlayer

El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas.

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad              | Descripción                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | System.ObjectElemento de colección de cadenas que ha cambiado. Puede convertir esto en una interfaz IWMPStringCollection para acceder a ella.<br/> |
| lCollectionIndex      | System.Int32El índice del elemento de colección de cadenas que ha cambiado.<br/>                                                          |
| cambiar                | WMPLib.WMPStringCollectionChangeEventTypeAn valor de enumeración que indica el tipo de cambio que se produjo.<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 






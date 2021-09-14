---
title: Evento KeyPress del objeto AxWindowsMediaPlayer
description: El evento KeyPress tiene lugar cuando se presiona y se libera una tecla. | Evento KeyPress del objeto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889764"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyPress del objeto AxWindowsMediaPlayer

El evento KeyPress tiene lugar cuando se presiona y se libera una tecla.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad      | Descripción                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System.Int16 Especifica el código ANSI numérico estándar para el carácter.<br/> |



 

## <a name="remarks"></a>Observaciones

Este evento se produce cuando la pulsación de tecla da como resultado cualquier carácter de teclado imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de algunos caracteres especiales, y la tecla ENTRAR o RETROCESO.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






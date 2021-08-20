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
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618795"
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



 

## <a name="remarks"></a>Comentarios

Este evento se produce cuando la pulsación de tecla da como resultado cualquier carácter de teclado imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de algunos caracteres especiales, y la tecla ENTRAR o RETROCESO.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






---
title: Evento KeyDown del objeto AxWindowsMediaPlayer
description: El evento KeyDown tiene lugar cuando se presiona una tecla. | Evento KeyDown del objeto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054736007219021dbc0a4c1c968f61e1bbdb285fa416aae5f3c92c3880fb55de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469725"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyDown del objeto AxWindowsMediaPlayer

El evento KeyDown tiene lugar cuando se presiona una tecla.

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad    | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System.Int16 Especifica qué tecla física se presiona. Para ver los valores posibles, vea Comentarios.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | Campo de bits System.Int16A con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.<br/> |



 

## <a name="remarks"></a>Comentarios

La **propiedad nKeyCode** especifica una clave física. En las tablas siguientes se muestran los valores posibles de las teclas principales en un teclado estándar.

Valores de las claves principales.



| Clave                     | Valor   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Bloq Mayús               | 20      |
| MAYÚS (izquierda o derecha)   | 16      |
| CTRL (izquierda o derecha)    | 17      |
| ALT (izquierda o derecha)     | 18      |
| SPACE                   | 32      |
| RETROCESO               | 8       |
| ENTRAR                   | 13      |
| Windows de logotipo, izquierda  | 91      |
| Windows de logotipo, derecha | 92      |
| Clave de la aplicación         | 93      |



 

Valores de las teclas de panel numérico.



| Clave               | Valor  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOQUEO NUM          | 144    |
| DIVIDE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SUBTRACT (-)      | 109    |
| ADD (+)           | 107    |
| SEPARATOR (Entrar) | 108    |
| DECIMAL (.)       | 110    |



 

Valores de las teclas de navegación.



| Clave         | Valor |
|-------------|-------|
| INSERT      | 45    |
| Delete      | 46    |
| INICIO        | 36    |
| FIN         | 35    |
| RE PÁG     | 33    |
| AV PÁG   | 34    |
| FLECHA ARRIBA    | 38    |
| FLECHA ABAJO  | 40    |
| FLECHA IZQUIERDA  | 37    |
| FLECHA DERECHA | 39    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 






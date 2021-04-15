---
title: Player. playState
description: La propiedad playState recupera un valor que indica el estado de la operación de Media Player de Windows.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Media Player de Windows Player. playState
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708821"
---
# <a name="playerplaystate"></a>Player. playState

La propiedad **playState** recupera un valor que indica el estado de la operación de Media Player de Windows.

## <a name="syntax"></a>Sintaxis

*reproductor* . **playState**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**). La constante de enumeración de estilo C se puede derivar prefijando el valor de estado con "wmpps". Por ejemplo, la constante para el estado Playing es **wmppsPlaying**.



| Value | Estado         | Descripción                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | No definido     | Windows Media Player está en un estado indefinido.                                                                              |
| 1     | Detenido       | La reproducción del elemento multimedia actual está detenida.                                                                              |
| 2     | En pausa        | La reproducción del elemento multimedia actual está en pausa. Cuando se pausa un elemento multimedia, reanudar la reproducción comienza en la misma ubicación. |
| 3     | Reproduciendo       | El elemento multimedia actual se está reproduciendo.                                                                                          |
| 4     | ScanForward   | El elemento multimedia actual es el reenvío rápido.                                                                                  |
| 5     | ScanReverse   | El elemento multimedia actual es un rebobinado rápido.                                                                                   |
| 6     | de respuesta     | El elemento multimedia actual está obteniendo datos adicionales del servidor.                                                          |
| 7     | En espera       | Se establece la conexión, pero el servidor no envía datos. Esperando a que se inicie la sesión.                                |
| 8     | MediaEnded    | El elemento multimedia ha finalizado la reproducción.                                                                                          |
| 9     | En transición | Preparando nuevo elemento multimedia.                                                                                                   |
| 10    | Ready         | Listo para comenzar la reproducción.                                                                                                     |
| 11    | Reconexión  | Volver a conectar a la secuencia.                                                                                                     |



 

## <a name="remarks"></a>Observaciones

No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado. Además, no todos los Estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de los Estados.

## <a name="examples"></a>Ejemplos

El siguiente código JScript muestra el uso del *reproductor*. propiedad **playState** . Un elemento de texto HTML, denominado "mi texto", muestra el estado actual. El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 






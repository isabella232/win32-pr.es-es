---
title: Player.playState
description: La propiedad playState recupera un valor que indica el estado de la Reproductor de Windows Media operación.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player.playState Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070966"
---
# <a name="playerplaystate"></a>Player.playState

La **propiedad playState** recupera un valor que indica el estado de la Reproductor de Windows Media operación.

## <a name="syntax"></a>Sintaxis

*player* . **playState**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**). La constante de enumeración de estilo C se puede derivar prefindo el valor de estado con "wmpps". Por ejemplo, la constante para el estado Playing es **wmppsPlaying**.



| Value | Estado         | Descripción                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | No definido     | Reproductor de Windows Media está en un estado indefinido.                                                                              |
| 1     | Detenido       | Se detiene la reproducción del elemento multimedia actual.                                                                              |
| 2     | En pausa        | La reproducción del elemento multimedia actual está en pausa. Cuando un elemento multimedia está en pausa, la reanudación de la reproducción comienza desde la misma ubicación. |
| 3     | Reproduciendo       | Se está reproduciendo el elemento multimedia actual.                                                                                          |
| 4     | ScanForward   | El elemento multimedia actual es de reenvío rápido.                                                                                  |
| 5     | ScanReverse   | El elemento multimedia actual está rebobinando rápidamente.                                                                                   |
| 6     | de respuesta     | El elemento multimedia actual está obteniendo datos adicionales del servidor.                                                          |
| 7     | En espera       | Se establece la conexión, pero el servidor no envía datos. Esperando a que comience la sesión.                                |
| 8     | MediaEnded    | El elemento multimedia ha completado la reproducción.                                                                                          |
| 9     | En transición | Preparar un nuevo elemento multimedia.                                                                                                   |
| 10    | Ready         | Listo para empezar a reproducir.                                                                                                     |
| 11    | Reconectar  | Volver a conectarse al flujo.                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Reproductor de Windows Media no se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se muestra el uso del *reproductor*. **Propiedad playState.** Un elemento de texto HTML, denominado "myText", muestra el estado actual. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player.PlayStateChange**](player-player-playstatechange.md)
</dt> </dl>

 

 






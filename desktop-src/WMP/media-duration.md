---
title: Media. Duration
description: La propiedad duration recupera la duración del elemento multimedia actual en segundos.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media Player de Windows Media. Duration
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709098"
---
# <a name="mediaduration"></a>Media. Duration

La propiedad **Duration** recupera la duración del elemento multimedia actual en segundos.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. **duración** de

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura ( **Double**).

## <a name="remarks"></a>Observaciones

Si esta propiedad se utiliza con un elemento multimedia distinto del especificado en el *reproductor*. **currentMedia**, puede que no contenga un valor válido.

Para recuperar la duración de los archivos que no están en la biblioteca del usuario, debe esperar a que Windows Media Player Abra el archivo; es decir, el OpenState actual debe ser igual a MediaOpen. Para comprobarlo, controle el *reproductor*. Evento **OpenStateChange** o comprobando periódicamente el valor de *Player*. **openState**.

En las listas de reproducción, la duración de cada elemento multimedia se puede recuperar cuando se abre el elemento multimedia individual, en lugar de cuando se abre la lista de reproducción.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

En el siguiente ejemplo de JScript se utiliza el *medio*. **duración** para mostrar el tiempo restante en el elemento multimedia actual. Un elemento HTML DIV denominado RemTime muestra la información. Un temporizador HTML actualiza el texto del elemento DIV cada segundo.

El siguiente código JScript inicia el temporizador:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



El siguiente código JScript detiene el temporizador:


```JScript
window.clearInterval(idTmr);
```



Use el *reproductor*. Evento **PlayStateChange** con una instrucción **Switch** para determinar cuándo iniciar y detener el temporizador.

El siguiente código JScript se ejecuta cada vez que el temporizador llama a la función de actualización:


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






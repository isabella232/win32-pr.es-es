---
title: Player. fullScreen
description: La propiedad fullScreen especifica o recupera un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698671"
---
# <a name="playerfullscreen"></a>Player. fullScreen

La propiedad **Fullscreen** especifica o recupera un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.

## <a name="syntax"></a>Sintaxis

*reproductor* . **pantalla completa**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                    |
|-------|----------------------------------------------------------------|
| true  | El contenido de vídeo se reproduce en el modo de pantalla completa.              |
| false | Predeterminada. El contenido de vídeo no se reproduce en el modo de pantalla completa. |



 

## <a name="remarks"></a>Observaciones

Para que el modo de pantalla completa funcione correctamente al insertar el control Media Player de Windows, el área de presentación del vídeo debe tener un alto y un ancho de al menos un píxel. Si **uiMode** se establece en "mini" o "Full", el alto del propio control debe ser 65 o superior para dar cabida al área de presentación de vídeo además de la interfaz de usuario.

Si **uiMode** se establece en "invisible", al establecer esta propiedad en true se genera un error y no se ve afectado el comportamiento del control.

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse. Después de un breve intervalo de ausencia de movimiento del mouse, se ocultan los controles de transporte. Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.

**Note**

Para mostrar los controles de transporte en modo de pantalla completa, se requiere el sistema operativo Windows XP.

Si los controles de transporte no se muestran en el modo de pantalla completa, Windows Media Player sale automáticamente del modo de pantalla completa cuando se detiene la reproducción.

**Note**

Asegúrese siempre de informar al usuario de cómo volver del modo de pantalla completa.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón de entrada HTML que usa *Player*. **pantalla** completa: cambiar un objeto reproductor incrustado al modo de pantalla completa. El objeto **Player** se creó con ID = "Player".


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 






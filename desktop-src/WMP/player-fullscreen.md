---
title: Player.fullScreen
description: La propiedad fullScreen especifica o recupera un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player.fullScreen Reproductor de Windows Media
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
ms.openlocfilehash: f380dcbcaeedddd23c5e6ff42f9750ea8bcd2f552942e19ba7b847e725edc3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054383"
---
# <a name="playerfullscreen"></a>Player.fullScreen

La **propiedad fullScreen** especifica o recupera un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.

## <a name="syntax"></a>Syntax

*player* . **fullScreen**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Valor | Descripción                                                    |
|-------|----------------------------------------------------------------|
| true  | El contenido del vídeo se reproduce en modo de pantalla completa.              |
| false | Predeterminada. El contenido de vídeo no se reproduce en modo de pantalla completa. |



 

## <a name="remarks"></a>Comentarios

Para que el modo de pantalla completa funcione correctamente al insertar el control Reproductor de Windows Media, el área de visualización del vídeo debe tener un alto y un ancho de al menos un píxel. Si **uiMode** se establece en "mini" o "full", el alto del propio control debe ser 65 o superior para alojar el área de presentación del vídeo además de la interfaz de usuario.

Si **uiMode** se establece en "invisible", establecer esta propiedad en true genera un error y no afecta al comportamiento del control.

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

Si **uiMode** se establece en "full" o "mini", Reproductor de Windows Media controles de transporte en modo de pantalla completa cuando se mueve el cursor del mouse. Después de un breve intervalo sin movimiento del mouse, se ocultan los controles de transporte. Si **uiMode** está establecido en "none", no se muestra ningún control en modo de pantalla completa.

**Nota**

La visualización de controles de transporte en modo de pantalla completa requiere el Windows operativo XP.

Si los controles de transporte no se muestran en modo de pantalla completa, Reproductor de Windows Media automáticamente sale del modo de pantalla completa cuando se detiene la reproducción.

**Nota**

Asegúrese siempre de informar al usuario de cómo volver desde el modo de pantalla completa.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón de entrada HTML que usa *Player*. **fullScreen** para cambiar un objeto de reproductor incrustado al modo de pantalla completa. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 






---
title: Método Controls.play
description: El método de reproducción hace que el elemento multimedia actual empiece a reproducirse o reanuda la reproducción de un elemento en pausa.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- método play Reproductor de Windows Media
- método play Reproductor de Windows Media , clase Controls
- Controla la clase Reproductor de Windows Media método , play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997455"
---
# <a name="controlsplay-method"></a>Método Controls.play

El **método de** reproducción hace que el elemento multimedia actual empiece a reproducirse o reanuda la reproducción de un elemento en pausa.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.play()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si se llama a este método durante el reenvío rápido o la rebobinado, el valor de *Configuración*. **rate** se establece en 1,0.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **play** para reproducir el elemento multimedia actual. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





